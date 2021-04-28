---
<span data-ttu-id="c48b6-101">description: Shell.FindComputer-Methode: Zeigt das Dialogfeld Suchergebnisse: Computer an.</span><span class="sxs-lookup"><span data-stu-id="c48b6-101">description: Shell.FindComputer method - 'Displays the Search Results: Computers dialog box.</span></span> <span data-ttu-id="c48b6-102">Im Dialogfeld wird das Ergebnis der Suche nach einem angegebenen Computer angezeigt."</span><span class="sxs-lookup"><span data-stu-id="c48b6-102">The dialog box shows the result of the search for a specified computer.'</span></span>
<span data-ttu-id="c48b6-103">ms.assetid: 0304b955-afde-4de4-824a-9ec9c9530360 title: Shell.FindComputer method (Shldisp.h) ms.topic: reference ms.date: 05/31/2018 topic_type:</span><span class="sxs-lookup"><span data-stu-id="c48b6-103">ms.assetid: 0304b955-afde-4de4-824a-9ec9c9530360 title: Shell.FindComputer method (Shldisp.h) ms.topic: reference ms.date: 05/31/2018 topic_type:</span></span> 
- <span data-ttu-id="c48b6-104">APIRef</span><span class="sxs-lookup"><span data-stu-id="c48b6-104">APIRef</span></span>
- <span data-ttu-id="c48b6-105">kbSyntax api_name:</span><span class="sxs-lookup"><span data-stu-id="c48b6-105">kbSyntax api_name:</span></span> 
- <span data-ttu-id="c48b6-106">Shell.FindComputer api_type:</span><span class="sxs-lookup"><span data-stu-id="c48b6-106">Shell.FindComputer api_type:</span></span> 
- <span data-ttu-id="c48b6-107">COM-api_location:</span><span class="sxs-lookup"><span data-stu-id="c48b6-107">COM api_location:</span></span> 
- <span data-ttu-id="c48b6-108">Shell32.dll</span><span class="sxs-lookup"><span data-stu-id="c48b6-108">Shell32.dll</span></span>
---

# <a name="shellfindcomputer-method"></a><span data-ttu-id="c48b6-109">Shell.FindComputer-Methode</span><span class="sxs-lookup"><span data-stu-id="c48b6-109">Shell.FindComputer method</span></span>

<span data-ttu-id="c48b6-110">Zeigt das Dialogfeld **Suchergebnisse: Computer** an.</span><span class="sxs-lookup"><span data-stu-id="c48b6-110">Displays the **Search Results: Computers** dialog box.</span></span> <span data-ttu-id="c48b6-111">Im Dialogfeld wird das Ergebnis der Suche nach einem angegebenen Computer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c48b6-111">The dialog box shows the result of the search for a specified computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="c48b6-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="c48b6-112">Syntax</span></span>


```JScript
Shell.FindComputer()
```


```VB

Shell.FindComputer()
```





## <a name="parameters"></a><span data-ttu-id="c48b6-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c48b6-113">Parameters</span></span>

<span data-ttu-id="c48b6-114">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="c48b6-114">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c48b6-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c48b6-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="c48b6-116">JScript</span><span class="sxs-lookup"><span data-stu-id="c48b6-116">JScript</span></span>

<span data-ttu-id="c48b6-117">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c48b6-117">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="c48b6-118">VB</span><span class="sxs-lookup"><span data-stu-id="c48b6-118">VB</span></span>

<span data-ttu-id="c48b6-119">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c48b6-119">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="c48b6-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c48b6-120">Examples</span></span>

<span data-ttu-id="c48b6-121">Das folgende Beispiel zeigt die Verwendung von **FindComputer.**</span><span class="sxs-lookup"><span data-stu-id="c48b6-121">The following example shows **FindComputer** in use.</span></span> <span data-ttu-id="c48b6-122">Das Ergebnis dieses Codes entspricht dem Drücken der Schaltfläche **Start,** klicken Sie auf **Suchen**, klicken Sie auf die Option **Drucker, Computer oder Personen, und** klicken Sie dann **auf Ein Computer im Netzwerk.**</span><span class="sxs-lookup"><span data-stu-id="c48b6-122">The result of this code is the same as pressing the **Start** button, clicking **Search**, clicking the **Printers, computers, or people** option, then clicking **A computer on the network**.</span></span> <span data-ttu-id="c48b6-123">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c48b6-123">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="c48b6-124">Jscript:</span><span class="sxs-lookup"><span data-stu-id="c48b6-124">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindComputer();
    }
</script>
```



<span data-ttu-id="c48b6-125">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="c48b6-125">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellFindComputerVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objShell.FindComputer

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="c48b6-126">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="c48b6-126">Visual Basic:</span></span>


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FindComputer

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="c48b6-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c48b6-127">Requirements</span></span>



| <span data-ttu-id="c48b6-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c48b6-128">Requirement</span></span> | <span data-ttu-id="c48b6-129">Wert</span><span class="sxs-lookup"><span data-stu-id="c48b6-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c48b6-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c48b6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c48b6-131">Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c48b6-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c48b6-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c48b6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c48b6-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c48b6-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c48b6-134">Header</span><span class="sxs-lookup"><span data-stu-id="c48b6-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="c48b6-135"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="c48b6-135"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="c48b6-136">Idl</span><span class="sxs-lookup"><span data-stu-id="c48b6-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c48b6-137"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="c48b6-137"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="c48b6-138">DLL</span><span class="sxs-lookup"><span data-stu-id="c48b6-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c48b6-139"><dt>Shell32.dll (Version 4.71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="c48b6-139"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




