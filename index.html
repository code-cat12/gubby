import React, { useState, useEffect, useRef } from 'react';
import { Map, Lock, Star, TrendingUp, TrendingDown, Swords, ShieldCheck, ShieldAlert, ArrowRight } from 'lucide-react';

const App = () => {
    const [clicks, setClicks] = useState(0);
    const [totalClicksSession, setTotalClicksSession] = useState(0); 
    const [gold, setGold] = useState(0);
    const [activeBuff, setActiveBuff] = useState(null);
    const [theme, setTheme] = useState('plains');
    const [showTravelModal, setShowTravelModal] = useState(false);
    const [inventory, setInventory] = useState({ 
        rainbow: 0, mega: 0, omega: 0, godly: 0, warp: 0,
        legendary: 0, mythic: 0, divine: 0, celestial: 0, void: 0,
        titan: 0, eternal: 0, infinite: 0, oracle: 0
    });
    const [textParticles, setTextParticles] = useState([]);
    const [notification, setNotification] = useState(null);
    const [isSquishing, setIsSquishing] = useState(false);
    const [autoclickers, setAutoclickers] = useState(0);
    const [autoclickerCost, setAutoclickerCost] = useState(150);
    const [prestigeLevel, setPrestigeLevel] = useState(0);
    const [peaceTreatyActive, setPeaceTreatyActive] = useState(false);
    
    const [marketMultiplier, setMarketMultiplier] = useState(1);
    const [marketTrend, setMarketTrend] = useState('stable'); 

    const [isBattleActive, setIsBattleActive] = useState(false);
    const [battleType, setBattleType] = useState('normal'); 
    const [battleHP, setBattleHP] = useState(0);
    const [maxBattleHP, setMaxBattleHP] = useState(0);
    const [battleTimer, setBattleTimer] = useState(0);
    const [normalBossCount, setNormalBossCount] = useState(0);
    const [megaBossCount, setMegaBossCount] = useState(0);

    const [marketCategory, setMarketCategory] = useState(null);

    const gubbyImgUrl = "https://static.wikia.nocookie.net/parasprunki-fanon/images/1/1e/Gubby.webp";
    const goldCoinUrl = "https://cdn3d.iconscout.com/3d/premium/thumb/star-coin-3d-icon-png-download-11254734.png";
    const friendImgUrl = "https://static.vecteezy.com/system/resources/thumbnails/012/026/493/small/add-new-friend-user-group-icon-3d-render-png.png";

    const DESTINATIONS = [
        { id: 'plains', name: 'Gubby Plains', req: 0, mult: 1, color: 'bg-emerald-50', themeColor: '#f0fdf4', img: 'https://cdn3d.iconscout.com/3d/premium/thumb/grass-3d-icon-png-download-9405100.png' },
        { id: 'hawaii', name: 'Hawaii', req: 5, mult: 5, color: 'bg-green-100', themeColor: '#dcfce7', img: 'https://cdn3d.iconscout.com/3d/premium/thumb/beach-3d-icon-png-download-9708027.png' },
        { id: 'starlight', name: 'Starlight Sky', req: 10, mult: 15, color: 'bg-purple-100', themeColor: '#f5f3ff', img: 'https://icons.iconarchive.com/icons/microsoft/fluentui-emoji-3d/512/Glowing-Star-3d-icon.png' },
        { id: 'void', name: 'The Void', req: 15, mult: 30, color: 'bg-blue-100', themeColor: '#eff6ff', img: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSGvH6kq36pZZrLLJ5kpnZx25JAewEp4g_H4Q&s' }
    ];

    const currentWorld = DESTINATIONS.find(d => d.id === theme);
    const currentWorldMult = currentWorld ? currentWorld.mult : 1;

    const SHOP_ITEMS = [
        { id: 'rainbow', name: 'Rainbow', category: 'small', cost: 250, power: 10, duration: 15, img: 'https://cdn3d.iconscout.com/3d/premium/thumb/rainbow-3d-icon-png-download-4659629.png' },
        { id: 'mega', name: 'Mega', category: 'small', cost: 800, power: 25, duration: 12, img: 'https://icons.iconarchive.com/icons/microsoft/fluentui-emoji-3d/512/Glowing-Star-3d-icon.png' },
        { id: 'omega', name: 'Omega', category: 'small', cost: 2000, power: 120, duration: 10, img: 'https://cdn3d.iconscout.com/3d/premium/thumb/diamond-3d-icon-png-download-8249311.png' },
        { id: 'oracle', name: 'Oracle', category: 'small', cost: 5000, power: 0, duration: 25, img: 'https://static.vecteezy.com/system/resources/thumbnails/041/644/156/small/3d-stock-market-ticker-with-upward-trend-arrow-icon-png.png' },
        { id: 'godly', name: 'Godly', category: 'medium', cost: 7500, power: 400, duration: 20, img: 'https://cdn3d.iconscout.com/3d/premium/thumb/king-crown-3d-icon-png-download-10707831.png' },
        { id: 'warp', name: 'Time Warp', category: 'medium', cost: 12000, power: 1, duration: 1, description: '+30s Battle', img: 'https://cdn3d.iconscout.com/3d/premium/thumb/time-machine-3d-icon-png-download-8786172.png' },
        { id: 'legendary', name: 'Legendary', category: 'medium', cost: 25000, power: 1000, duration: 9, img: 'https://cdn3d.iconscout.com/3d/premium/thumb/gold-medal-3d-icon-png-download-11613166.png' },
        { id: 'mythic', name: 'Mythic', category: 'large', cost: 100000, power: 5000, duration: 9, img: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSghOJb2-ZD1lymQCT1S_dYisQmoX1dIDYzdg&s' },
        { id: 'divine', name: 'Divine', category: 'large', cost: 500000, power: 25000, duration: 9, img: 'https://cdn3d.iconscout.com/3d/premium/thumb/compass-astrology-3d-icon-png-download-13124447.png' },
        { id: 'celestial', name: 'Celestial', category: 'large', cost: 2500000, power: 100000, duration: 8, img: 'https://cdn3d.iconscout.com/3d/premium/thumb/planets-3d-icon-png-download-11683976.png' },
        { id: 'void', name: 'Void', category: 'large', cost: 10000000, power: 500000, duration: 7, img: 'https://cdn3d.iconscout.com/3d/premium/thumb/space-station-3d-icon-png-download-6308159.png' },
        { id: 'titan', name: 'Titan', category: 'op', cost: 100000000, power: 5000000, duration: 10, img: 'https://cdn3d.iconscout.com/3d/premium/thumb/robot-3d-icon-png-download-7577797.png?f=webp' },
        { id: 'eternal', name: 'Eternal', category: 'op', cost: 500000000, power: 50000000, duration: 12, img: 'https://cdn3d.iconscout.com/3d/premium/thumb/atom-3d-icon-png-download-5522651.png' },
        { id: 'infinite', name: 'Infinite', category: 'op', cost: 1000000000, power: 250000000, duration: 15, img: 'https://icons.iconarchive.com/icons/microsoft/fluentui-emoji-3d/512/Infinity-3d-icon.png' }
    ];

    const currentPrestigeCost = Math.floor(10000 * Math.pow(2.5, prestigeLevel));
    const [marketQueue, setMarketQueue] = useState([1.1, 0.8, 1.4]);
    const [showOracle, setShowOracle] = useState(false);

    useEffect(() => {
        document.body.style.backgroundColor = currentWorld?.themeColor || '#f0fdf4';
    }, [theme, currentWorld]);

    useEffect(() => {
        const interval = setInterval(() => {
            setMarketMultiplier(prev => {
                const nextRate = marketQueue[0];
                setMarketTrend(nextRate > prev ? 'up' : 'down');
                setMarketQueue(q => [...q.slice(1), 0.5 + (Math.random() * 1.5)]);
                return nextRate;
            });
        }, 7000);
        return () => clearInterval(interval);
    }, [marketQueue]);

    useEffect(() => {
        const interval = setInterval(() => {
            const prestigeMult = (prestigeLevel + 1);
            if (autoclickers > 0) {
                const gain = autoclickers * prestigeMult;
                setClicks(prev => prev + gain);
                setTotalClicksSession(prev => prev + gain);
            }
        }, 1000);
        return () => clearInterval(interval);
    }, [autoclickers, prestigeLevel]);

    useEffect(() => {
        if (totalClicksSession > 0 && !isBattleActive && !peaceTreatyActive) {
            const lastProcessedMega = window._lastMegaTriggered || 0;
            const lastProcessedNormal = window._lastNormalTriggered || 0;

            if (totalClicksSession >= lastProcessedMega + 750) {
                triggerBattle('mega');
                window._lastMegaTriggered = Math.floor(totalClicksSession / 750) * 750;
                window._lastNormalTriggered = totalClicksSession;
            } 
            else if (totalClicksSession >= lastProcessedNormal + 250) {
                triggerBattle('normal');
                window._lastNormalTriggered = Math.floor(totalClicksSession / 250) * 250;
            }
        }
    }, [totalClicksSession, isBattleActive, peaceTreatyActive]);

    const triggerBattle = (type) => {
        const isMega = type === 'mega';
        let hp = isMega ? 45 + (megaBossCount * 10) : 20 + (normalBossCount * 10);
        setBattleType(type);
        setBattleHP(hp);
        setMaxBattleHP(hp);
        const baseTime = isMega ? 45 : 30;
        setBattleTimer(baseTime + (isMega ? (megaBossCount * 8) : (normalBossCount * 5)));
        setIsBattleActive(true);
    };

    const endBattle = (won) => {
        setIsBattleActive(false);
        if (won) {
            const reward = maxBattleHP * (battleType === 'mega' ? 6 : 3) * currentWorldMult;
            if (battleType === 'mega') setMegaBossCount(c => c + 1);
            else setNormalBossCount(c => c + 1);
            setGold(prev => prev + reward);
            setNotification({ title: "VICTORY!", message: `Reward: ${reward.toFixed(2)} Gold (including World Multi).`, type: "success" });
        } else {
            setNotification({ title: "BATTLE FAILED!", message: `The boss escaped!`, type: "error" });
        }
    };

    useEffect(() => {
        const interval = setInterval(() => {
            if (activeBuff) {
                setActiveBuff(prev => {
                    if (!prev || prev.timeLeft <= 1) {
                        if (prev?.id === 'oracle') setShowOracle(false);
                        return null;
                    }
                    return { ...prev, timeLeft: prev.timeLeft - 1 };
                });
            }
            if (isBattleActive) {
                setBattleTimer(prev => {
                    if (prev <= 1) { endBattle(false); return 0; }
                    return prev - 1;
                });
            }
        }, 1000);
        return () => clearInterval(interval);
    }, [activeBuff, isBattleActive]);

    const sellClicks = () => {
        if (!isBattleActive && clicks > 0) {
            const totalGoldEarned = clicks * marketMultiplier * currentWorldMult;
            setGold(g => g + totalGoldEarned);
            setClicks(0);
            setNotification({ 
                title: "MARKET SOLD!", 
                message: `Sold at ${marketMultiplier.toFixed(2)}x for ${totalGoldEarned.toFixed(2)} gold! (World: ${currentWorldMult}x)`, 
                type: "success" 
            });
        }
    };

    const ascend = () => {
        if (gold >= currentPrestigeCost) {
            setPrestigeLevel(p => p + 1);
            setGold(0); setClicks(0); setTotalClicksSession(0);
            setInventory({ rainbow: 0, mega: 0, omega: 0, oracle: 0, godly: 0, warp: 0, legendary: 0, mythic: 0, divine: 0, celestial: 0, void: 0, titan: 0, eternal: 0, infinite: 0 });
            window._lastMegaTriggered = 0; window._lastNormalTriggered = 0;
            setActiveBuff(null); setShowOracle(false);
            setNotification({ title: "ASCENDED!", message: `Prestige ${prestigeLevel + 1} reached!`, type: "success" });
        }
    };

    const handleMainClick = (e) => {
        const currentPower = (prestigeLevel + 1) * (activeBuff && !['warp', 'oracle'].includes(activeBuff.id) ? activeBuff.power : 1);
        const rect = e.currentTarget.getBoundingClientRect();
        const clickX = e.clientX - rect.left - rect.width / 2;
        const clickY = e.clientY - rect.top - rect.height / 2;
        setIsSquishing(true);
        setTimeout(() => setIsSquishing(false), 200);
        setTotalClicksSession(prev => prev + 1);

        if (isBattleActive) {
            setBattleHP(prev => {
                const next = prev - currentPower;
                if (next <= 0) { setTimeout(() => endBattle(true), 10); return 0; }
                return next;
            });
            spawnParticle(clickX, clickY, "HIT!", "text-red-600 font-black");
        } else {
            setClicks(prev => prev + currentPower);
            spawnParticle(clickX, clickY, `+${currentPower}`, "text-black font-black");
        }
    };

    const useItem = (item) => {
        if (inventory[item.id] > 0 && !activeBuff) {
            if (item.id === 'warp') {
                if (isBattleActive) {
                    setBattleTimer(prev => prev + 30);
                    setInventory(inv => ({ ...inv, [item.id]: inv[item.id] - 1 }));
                } else {
                    setNotification({ title: "WARP FAILED", message: "Only use during battles!", type: "warning" });
                }
            } else if (item.id === 'oracle') {
                setInventory(inv => ({ ...inv, [item.id]: inv[item.id] - 1 }));
                setActiveBuff({ ...item, timeLeft: item.duration });
                setShowOracle(true);
            } else {
                setInventory(inv => ({ ...inv, [item.id]: inv[item.id] - 1 }));
                setActiveBuff({ ...item, timeLeft: item.duration });
            }
        }
    };

    const spawnParticle = (x, y, text, colorClass) => {
        const textId = Date.now() + Math.random();
        setTextParticles(prev => [...prev, { id: textId, x: x, y: y, popX: (Math.random() - 0.5) * 40, value: text, color: colorClass }]);
        setTimeout(() => setTextParticles(prev => prev.filter(p => p.id !== textId)), 800);
    };

    const formatCost = (cost) => {
        if (cost >= 1000000000) return (cost / 1000000000).toFixed(1) + 'B';
        if (cost >= 1000000) return (cost / 1000000).toFixed(1) + 'M';
        if (cost >= 1000) return (cost / 1000).toFixed(1) + 'k';
        return cost.toLocaleString();
    }

    const renderMarketContent = () => {
        const catBtnBase = "w-full bg-white border p-6 rounded-2xl flex justify-between items-center hover:bg-slate-50 transition-all group shadow-sm active:scale-[0.98]";
        if (!marketCategory) {
            return (
                <div className="flex flex-col gap-4">
                    <button onClick={() => setMarketCategory('small')} className={`${catBtnBase} border-blue-500/20`}>
                        <span className="font-black text-sm uppercase tracking-widest text-blue-600">Small Boosts</span>
                        <ArrowRight size={20} className="text-blue-400 group-hover:translate-x-1 transition-transform" />
                    </button>
                    <button onClick={() => setMarketCategory('medium')} className={`${catBtnBase} border-purple-500/20`}>
                        <span className="font-black text-sm uppercase tracking-widest text-purple-600">Medium Boosts</span>
                        <ArrowRight size={20} className="text-purple-400 group-hover:translate-x-1 transition-transform" />
                    </button>
                    <button onClick={() => setMarketCategory('large')} className={`${catBtnBase} border-orange-500/20`}>
                        <span className="font-black text-sm uppercase tracking-widest text-orange-600">Large Boosts</span>
                        <ArrowRight size={20} className="text-orange-400 group-hover:translate-x-1 transition-transform" />
                    </button>
                    <button onClick={() => setMarketCategory('op')} className={`${catBtnBase} border-red-500/20`}>
                        <span className="font-black text-sm uppercase tracking-widest text-red-600">OP BOOSTS</span>
                        <ArrowRight size={20} className="text-red-400 group-hover:translate-x-1 transition-transform" />
                    </button>
                </div>
            );
        }
        const itemsToShow = SHOP_ITEMS.filter(i => i.category === marketCategory);
        return (
            <div className="flex flex-col gap-3">
                <button onClick={() => setMarketCategory(null)} className="w-full text-left text-[10px] font-black uppercase text-slate-400 mb-2 flex items-center gap-1 hover:text-slate-600">← Back to groups</button>
                {marketCategory === 'small' && (
                     <button onClick={() => { if (gold >= autoclickerCost) { setGold(g => g - autoclickerCost); setAutoclickers(a => a + 1); setAutoclickerCost(c => Math.floor(c * 1.5)); }}} className="flex items-center justify-between p-4 rounded-2xl bg-white hover:bg-slate-50 transition-all shadow-sm">
                        <div className="flex items-center gap-4"><img src={friendImgUrl} className="w-10 h-10 object-contain"/><p className="font-black text-[10px] uppercase text-slate-900">Gubby Friend</p></div>
                        <span className="bg-slate-900 text-white px-3 py-1.5 rounded-lg text-[10px] font-black">{formatCost(autoclickerCost)}</span>
                    </button>
                )}
                {itemsToShow.map(item => (
                    <button key={item.id} onClick={() => { if (gold >= item.cost) { setGold(g => g - item.cost); setInventory(inv => ({ ...inv, [item.id]: inv[item.id] + 1 })); } }} className="flex items-center justify-between p-4 rounded-2xl bg-white hover:bg-slate-50 transition-all shadow-sm">
                        <div className="flex items-center gap-4">
                            <img src={item.img} className="w-10 h-10 object-contain"/>
                            <div>
                                <p className="font-black text-[10px] uppercase text-slate-900">{item.name}</p>
                                {item.description && <p className="text-[8px] font-medium text-slate-400 uppercase mt-1">{item.description}</p>}
                            </div>
                        </div>
                        <span className="bg-slate-900 text-white px-3 py-1.5 rounded-lg text-[10px] font-black">{formatCost(item.cost)}</span>
                    </button>
                ))}
            </div>
        );
    }

    return (
        <div className="min-h-screen flex flex-col items-center px-4 py-2 select-none overflow-x-hidden pb-12 transition-colors duration-500">
            {notification && (
                <div className="fixed inset-0 z-[100] flex items-center justify-center p-4 bg-slate-900/40 backdrop-blur-sm">
                    <div className="bg-white p-8 rounded-[2.5rem] shadow-2xl max-w-sm w-full">
                        <h4 className="font-black text-2xl text-center mb-2 uppercase text-slate-900">{notification.title}</h4>
                        <p className="text-slate-500 text-center mb-6 font-medium leading-snug">{notification.message}</p>
                        <button onClick={() => setNotification(null)} className="w-full bg-slate-900 text-white py-4 rounded-2xl font-black uppercase">Okay</button>
                    </div>
                </div>
            )}

            {showTravelModal && (
                <div className="fixed inset-0 z-[90] flex items-center justify-center p-4 bg-slate-900/60 backdrop-blur-md">
                    <div className="bg-white p-8 rounded-[3rem] shadow-2xl max-w-3xl w-full">
                        <h4 className="font-black text-2xl text-center mb-8 uppercase text-slate-900 tracking-tighter">Choose Destination</h4>
                        <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-4">
                            {DESTINATIONS.map(dest => {
                                const isLocked = prestigeLevel < dest.req;
                                return (
                                    <button 
                                        key={dest.id} 
                                        disabled={isLocked}
                                        onClick={() => { setTheme(dest.id); setShowTravelModal(false); }}
                                        className={`p-6 rounded-[2rem] flex flex-col items-center gap-2 transition-all group relative overflow-hidden ${isLocked ? 'opacity-40 grayscale cursor-not-allowed bg-slate-100' : `${dest.color} hover:scale-105 border-4 ${theme === dest.id ? 'border-indigo-500' : 'border-transparent'}`}`}
                                    >
                                        <img src={dest.img} className="w-16 h-16 object-contain mb-2" />
                                        <span className="font-black text-[10px] uppercase text-slate-900 tracking-widest">{dest.name}</span>
                                        <div className="flex flex-col items-center">
                                            <span className="text-[12px] font-black text-indigo-600">x{dest.mult} Multi</span>
                                            <span className={`text-[8px] font-bold uppercase mt-1 ${isLocked ? 'text-red-500' : 'text-slate-400'}`}>
                                                {isLocked ? `Req: Prestige ${dest.req}` : `Unlocked`}
                                            </span>
                                        </div>
                                        {isLocked && <div className="absolute inset-0 flex items-center justify-center bg-slate-900/10"><Lock size={24} className="text-slate-400" /></div>}
                                    </button>
                                );
                            })}
                        </div>
                        <button onClick={() => setShowTravelModal(false)} className="w-full mt-8 text-slate-400 font-black uppercase text-[10px] tracking-widest">Close Map</button>
                    </div>
                </div>
            )}

            <header className="z-20 w-full max-w-5xl flex flex-col items-center gap-3 mt-4 mb-2">
                <div className="flex flex-col items-center gap-2">
                    <h1 className="text-4xl font-black tracking-tighter uppercase text-center text-slate-900">Gubby Clicker</h1>
                    <div className="flex gap-2">
                        <span className="bg-indigo-600 text-white px-3 py-1 rounded-full text-[10px] font-black uppercase">Prestige {prestigeLevel}</span>
                        <span className="bg-amber-500 text-white px-3 py-1 rounded-full text-[10px] font-black uppercase">{currentWorld?.name} (x{currentWorldMult} Multi)</span>
                        {peaceTreatyActive ? (
                            <span className="bg-emerald-600 text-white px-3 py-1 rounded-full text-[10px] font-black uppercase flex items-center gap-1 shadow-sm"><ShieldCheck size={10} /> Peaceful</span>
                        ) : (
                            <span className="bg-red-50/80 border border-red-200 text-red-500 px-3 py-1 rounded-full text-[10px] font-black uppercase flex items-center gap-1"><ShieldAlert size={10} /> Peace (Locked)</span>
                        )}
                    </div>
                </div>
                
                <div className="w-full bg-white px-8 py-5 rounded-[2.5rem] shadow-sm flex flex-wrap items-center justify-between gap-4">
                    <div className="flex items-center gap-4 sm:gap-10 flex-1 flex-wrap justify-center sm:justify-start">
                        <div><p className="text-[9px] font-black text-slate-400 uppercase mb-1">Clicks</p><span className="text-xl font-black tracking-tight text-slate-900">{clicks.toLocaleString(undefined, {maximumFractionDigits: 0})}</span></div>
                        <div><p className="text-[9px] font-black text-slate-400 uppercase mb-1">Total Clicks</p><span className="text-xl font-black tracking-tight text-slate-900">{totalClicksSession.toLocaleString(undefined, {maximumFractionDigits: 0})}</span></div>
                        <div><p className="text-[9px] font-black text-slate-400 uppercase mb-1">Market Rate</p>
                            <div className="flex items-center gap-1.5"><span className={`text-xl font-black ${marketMultiplier >= 1.2 ? 'text-emerald-500' : marketMultiplier <= 0.8 ? 'text-red-500' : 'text-slate-900'}`}>{marketMultiplier.toFixed(2)}x</span><span className="text-[10px] font-black uppercase text-slate-900">{marketTrend === 'up' ? <TrendingUp size={14} /> : <TrendingDown size={14} />}</span></div>
                        </div>
                        <div><p className="text-[9px] font-black text-slate-400 uppercase mb-1">Gold</p><div className="flex items-center gap-1"><img src={goldCoinUrl} className="w-4 h-4"/><span className="text-xl font-black text-slate-900">{gold.toLocaleString(undefined, {minimumFractionDigits: 2, maximumFractionDigits: 2})}</span></div></div>
                    </div>
                    <div className="flex items-center gap-3">
                        <button onClick={() => setShowTravelModal(true)} className="p-3 bg-white border-2 border-slate-100 text-slate-900 rounded-2xl shadow-sm hover:border-indigo-200 transition-colors flex items-center gap-2 px-4" title="Travel">
                            <Map size={18} className="text-indigo-500" />
                            <span className="text-[10px] font-black uppercase tracking-widest">Travel</span>
                        </button>
                        <button onClick={ascend} disabled={gold < currentPrestigeCost || isBattleActive} className={`px-5 py-3 rounded-2xl font-black uppercase text-[10px] tracking-widest transition-all ${gold >= currentPrestigeCost ? 'bg-indigo-600 text-white shadow-md' : 'bg-slate-100 text-slate-300'}`}>Ascend ({formatCost(currentPrestigeCost)})</button>
                        <button onClick={sellClicks} disabled={isBattleActive} className={`px-6 py-3 rounded-2xl font-black uppercase text-[10px] tracking-widest transition-all hover:brightness-105 shadow-md ${marketMultiplier >= 1.2 ? 'bg-emerald-400 text-white animate-pulse' : 'bg-yellow-400 text-slate-900'}`}>Sell</button>
                    </div>
                </div>
            </header>

            <main className="z-10 relative flex flex-col items-center justify-center w-full min-h-[400px]">
                <div className="h-20 mb-4 flex flex-col items-center justify-center">
                    {showOracle && (
                        <div className="flex gap-2 mb-2">
                            {marketQueue.map((rate, idx) => (
                                <div key={idx} className="bg-slate-900 text-white px-3 py-1 rounded-lg flex flex-col items-center border border-indigo-400">
                                    <span className="text-[7px] font-bold uppercase opacity-60">Future {idx + 1}</span>
                                    <span className={`text-xs font-black ${rate >= 1.2 ? 'text-emerald-400' : rate <= 0.8 ? 'text-red-400' : 'text-white'}`}>{rate.toFixed(2)}x</span>
                                </div>
                            ))}
                        </div>
                    )}
                    {isBattleActive ? (
                        <div className="flex flex-col items-center w-64">
                            <div className="flex justify-between w-full mb-1">
                                <span className="text-[10px] font-black uppercase text-red-600 tracking-widest flex items-center gap-1">
                                    <Swords size={12} /> {battleType === 'mega' ? 'MEGA BOSS' : 'BOSS'} {battleTimer}s
                                </span>
                            </div>
                            <div className="w-full h-3 bg-slate-200 rounded-full overflow-hidden shadow-inner"><div className="h-full bg-red-600 transition-all duration-300" style={{ width: `${(battleHP / maxBattleHP) * 100}%` }} /></div>
                        </div>
                    ) : activeBuff && (
                        <div className="bg-white px-8 py-3 rounded-full shadow-lg animate-bounce text-center border-2 border-indigo-100">
                            <span className="text-xs font-black uppercase text-indigo-600 tracking-widest block">{activeBuff.name}</span>
                            <span className="text-[10px] font-bold text-slate-400">{activeBuff.timeLeft}s</span>
                        </div>
                    )}
                </div>

                <div className="relative">
                    <div className="absolute inset-0 pointer-events-none z-40">
                        {textParticles.map(p => (
                            <span key={p.id} className={`absolute text-4xl font-black ${p.color}`} style={{ 
                                left: `calc(50% + ${p.x}px)`, 
                                top: `calc(50% + ${p.y}px)`, 
                                transform: `translateX(${p.popX}px) translateY(-50px)`,
                                transition: 'all 0.8s ease-out',
                                opacity: 0
                            }}>{p.value}</span>
                        ))}
                    </div>
                    <button 
                        onClick={handleMainClick} 
                        className={`relative active:scale-95 w-64 h-64 transition-transform duration-100 ${isBattleActive ? 'animate-pulse' : ''} ${isSquishing ? 'scale-x-110 scale-y-90' : ''}`}
                    >
                        <img 
                            src={gubbyImgUrl} 
                            className={`w-full h-full object-contain drop-shadow-2xl transition-all duration-500 ${isBattleActive && battleType === 'mega' ? 'hue-rotate-[280deg] saturate-200 scale-110' : ''}`} 
                        />
                    </button>
                </div>
            </main>

            <div className="z-20 w-full max-w-6xl flex flex-col lg:flex-row gap-6 mt-8">
                <section className="bg-white p-8 rounded-[3rem] shadow-sm flex-1">
                    <div className="flex justify-between items-center mb-8 px-2">
                        <h3 className="text-[10px] font-black uppercase tracking-[0.3em] text-slate-400">Marketplace</h3>
                        {!peaceTreatyActive && (
                            <button onClick={() => { if (gold >= 1000000) { setGold(g => g - 1000000); setPeaceTreatyActive(true); setNotification({ title: "WORLD PEACE", message: "No more bosses will ever appear.", type: "success" }); } }} className={`text-[8px] font-black uppercase px-4 py-2 rounded-xl transition-all ${gold >= 1000000 ? 'bg-emerald-500 text-white' : 'bg-slate-100 text-slate-300'}`}>Peace (1M)</button>
                        )}
                    </div>
                    {renderMarketContent()}
                </section>

                <section className="bg-white p-8 rounded-[3rem] shadow-sm flex-1">
                    <h3 className="text-[10px] font-black uppercase tracking-[0.3em] text-slate-400 mb-8 px-2">Storage</h3>
                    <div className="grid grid-cols-4 gap-4">
                        {SHOP_ITEMS.map(item => (
                            <button key={`inv-${item.id}`} onClick={() => useItem(item)} disabled={inventory[item.id] === 0 || (activeBuff !== null && item.id !== 'warp')} className={`flex flex-col items-center p-4 rounded-[2rem] transition-all relative ${inventory[item.id] > 0 ? 'bg-slate-50 hover:bg-slate-100 active:scale-95' : 'opacity-20 grayscale'}`}>
                                <img src={item.img} className="w-10 h-10 mb-2 object-contain"/>
                                <span className="absolute -top-1 -right-1 bg-slate-900 text-white text-[8px] font-black w-5 h-5 flex items-center justify-center rounded-full border-2 border-white">{inventory[item.id]}</span>
                                <p className="text-[8px] font-black uppercase leading-tight text-slate-900 text-center">{item.name}</p>
                            </button>
                        ))}
                    </div>
                </section>
            </div>
        </div>
    );
};

export default App;
