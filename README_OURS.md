
# 默认
MODEL=facebook/opt-13b TASK=SST2 MODE=ft LR=1e-7 EPS=1e-3 bash mezo.sh

# 我们的
CUDA_VISIBLE_DEVICES=0 MODEL=$model SEED=0 BS=16 STEPS=40000 LR=1e-7 EPS=1e-3 TASK=$task MODE=ft EPS=1e-3 nohup bash mezo.sh > ${output_dir}/$task/${task}_seed0_lr_1e-7.log 2>&1 &

