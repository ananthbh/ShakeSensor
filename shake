

import UIKit
import AVFoundation

class ViewController: UIViewController {
    
    var player:AVAudioPlayer = AVAudioPlayer()
    var sounds = ["bean", "belch", "giggle", "pew", "pig", "snore", "snore", "uuu"]

    override func viewDidLoad() {
        super.viewDidLoad()
        // Do any additional setup after loading the view, typically from a nib.
    }
    
    override func motionEnded(motion: UIEventSubtype, withEvent event: UIEvent?) {
        if event?.subtype == UIEventSubtype.MotionShake {
            
            print("motion shake detected")
            
            var random = Int(arc4random_uniform(UInt32(sounds.count)))
            
            print(random)
            
            let audiopath = NSBundle.mainBundle().pathForResource(sounds[random], ofType: "mp3")
            
            do{
                
            
            try player = AVAudioPlayer(contentsOfURL: NSURL(fileURLWithPath: audiopath!))
                player.play()
            
            } catch {
                //error
            }
            
            
        }
    }
