# SLplayer
# SLVoicePlayer
###SLVoicePlayer 是一个多功能的音乐播放器，持播放语音队列，播放单个音频，播放，暂停，上一首，下一首，快进，快退，缓存音频，下载音频等功能
```object-c
@protocol SLPlayerDelegate <NSObject>

@optional
/**
 *  代理，获取当前播放的index
 */
- (void)SLPlayerWillChangedAtIndex:(NSUInteger)index;


/**
 *  代理，获取当前播放的item
 */
- (void)SLPlayerCurrentItemChanged:(AVPlayerItem *)item;


/**
 *  代理，当前播放状态
 */
- (void)SLPlayerRateChanged:(BOOL)isPlaying;

/**
 *  代理，当前播放结束
 */
- (void)SLPlayerDidReachEnd;

/**
 *  代理，播放预加载时间
 */

- (void)SLPlayerCurrentItemPreloaded:(CMTime)time;
/**
 *  代理，播放失败的状态及原因
 */
- (void)SLPlayerDidFailed:(SLPlayerFailed)identifier error:(NSError *)error;



@protocol SLPlayerDataSource <NSObject>

@optional

/**
 *  DataSource，return 播放器播放多少item
 */
- (NSUInteger)SLPlayerNumberOfItems;


/**
 *  DataSource，return 播放器播放item的url
 */
- (NSURL *)SLPlayerURLForItemAtIndex:(NSUInteger)index preBuffer:(BOOL)preBuffer;


- (void)SLPlayerAsyncSetUrlForItemAtIndex:(NSUInteger)index preBuffer:(BOOL)preBuffer;

@end

```


## contact me  
1.[博客](http://christmascat.lofter.com)<br />  
2.[微博](http://weibo.com/3388333772/profile?topnav=1&wvr=6)<br />  
