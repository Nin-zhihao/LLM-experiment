


## Model Details


- **Base Model:** Qwen2.5-7B-Instruct




## Training Details

### Training Data
[hon9kon9ize/yue-alpaca](https://huggingface.co/datasets/hon9kon9ize/yue-alpaca)

[Nin8520/words](https://huggingface.co/datasets/Nin8520/words)




#### Training Setting

 ```
 args = dict(
  stage="sft",                                               
  do_train=True,
  model_name_or_path="Qwen/Qwen2.5-7B-Instruct", 
  dataset="yue_1,yue_2",          
  template="alpaca",                                         
  finetuning_type="lora",                                    
  lora_target="all",                                         
  output_dir="Qwen2.5_lora",                                 
  per_device_train_batch_size=2,                             
  gradient_accumulation_steps=4,                             
  lr_scheduler_type="cosine",                                
  logging_steps=5,                                           
  warmup_ratio=0.1,                                          
  save_steps=1000,                                           
  learning_rate=5e-5,                                        
  num_train_epochs=1.0,                                      
  max_samples=300,                                           
  max_grad_norm=1.0,                                         
  loraplus_lr_ratio=16.0,                                    
  fp16=True,                                                 
  report_to="none",                                          
) 
 ```


## Evaluation
Not done
<!-- This section describes the evaluation protocols and provides the results. -->
