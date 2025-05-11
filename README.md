### [👉👉👉♥♥点此进入♥观看入口👈👈👈](http://a.d44k.cc/jizz.html)
<br></br><br></br><br></br>
 # 添加任务按钮
        add_btn = ttk.Button(
            top_frame, 
            text="添加任务", 
            command=self.add_task
        )
        add_btn.grid(row=3, column=3, padx=5, pady=5, sticky="e")
        
        # 中间框架 - 任务列表
        center_frame = ttk.LabelFrame(self.root, text="任务列表", padding=10)
        center_frame.pack(pady=10, padx=10, fill="both", expand=True)
        
        # 创建树形视图
        self.tree = ttk.Treeview(
            center_frame, 
            columns=("id", "title", "owner", "deadline", "priority", "status"), 
            show="headings"
        )
        
        # 定义列
        self.tree.column("id", width=50, anchor="center")
        self.tree.column("title", width=200, anchor="w")
        self.tree.column("owner", width=100, anchor="w")
        self.tree.column("deadline", width=100, anchor="center")
        self.tree.column("priority", width=80, anchor="center")
        self.tree.column("status", width=100, anchor="center")
        
        # 定义表头
        self.tree.heading("id", text="ID")
        self.tree.heading("title", text="任务标题")
        self.tree.heading("owner", text="负责人")
        self.tree.heading("deadline", text="截止日期")
        self.tree.heading("priority", text="优先级")
        self.tree.heading("status", text="状态")
