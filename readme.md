# //custom error handler

```
app.all('*', (req: Request, res: Response) => {
    res.status(400).json({
        success: false,
        message: "Something went wrong"
    })
})
```


# //global error handler

```
app.use((error: any, req: Request, res: Response, next: NextFunction) => {
    if (error) {
        res.status(400).json({
            success: false,
            message: "Something went wrong"
        })
    }
})
```
## প্রতিটি crud operation এ অবশ্যই try-catch statement ব্যববহা করতে হবে ।
##  crud operation এর শেষে বসবে ।
