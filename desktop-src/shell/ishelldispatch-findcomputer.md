---
<span data-ttu-id="0cab1-101">description: IShellDispatch.FindComputer-Methode: Zeigt das Dialogfeld Suchergebnisse: Computer an.</span><span class="sxs-lookup"><span data-stu-id="0cab1-101">description: IShellDispatch.FindComputer method - 'Displays the Search Results: Computers dialog box.</span></span> <span data-ttu-id="0cab1-102">Im Dialogfeld wird das Ergebnis der Suche nach einem angegebenen Computer angezeigt."</span><span class="sxs-lookup"><span data-stu-id="0cab1-102">The dialog box shows the result of the search for a specified computer.'</span></span>
<span data-ttu-id="0cab1-103">ms.assetid: 9B687A8A-BB29-49a0-8AE3-11A75FAF3257 title: IShellDispatch.FindComputer method (Shldisp.h) ms.topic: reference ms.date: 05/31/2018 topic_type:</span><span class="sxs-lookup"><span data-stu-id="0cab1-103">ms.assetid: 9B687A8A-BB29-49a0-8AE3-11A75FAF3257 title: IShellDispatch.FindComputer method (Shldisp.h) ms.topic: reference ms.date: 05/31/2018 topic_type:</span></span> 
- <span data-ttu-id="0cab1-104">APIRef</span><span class="sxs-lookup"><span data-stu-id="0cab1-104">APIRef</span></span>
- <span data-ttu-id="0cab1-105">kbSyntax api_name:</span><span class="sxs-lookup"><span data-stu-id="0cab1-105">kbSyntax api_name:</span></span> 
- <span data-ttu-id="0cab1-106">IShellDispatch.FindComputer api_type:</span><span class="sxs-lookup"><span data-stu-id="0cab1-106">IShellDispatch.FindComputer api_type:</span></span> 
- <span data-ttu-id="0cab1-107">COM-api_location:</span><span class="sxs-lookup"><span data-stu-id="0cab1-107">COM api_location:</span></span> 
- <span data-ttu-id="0cab1-108">Shell32.dll</span><span class="sxs-lookup"><span data-stu-id="0cab1-108">Shell32.dll</span></span>
---

# <a name="ishelldispatchfindcomputer-method"></a><span data-ttu-id="0cab1-109">IShellDispatch.FindComputer-Methode</span><span class="sxs-lookup"><span data-stu-id="0cab1-109">IShellDispatch.FindComputer method</span></span>

<span data-ttu-id="0cab1-110">Zeigt das **Dialogfeld Suchergebnisse: Computer** an.</span><span class="sxs-lookup"><span data-stu-id="0cab1-110">Displays the **Search Results: Computers** dialog box.</span></span> <span data-ttu-id="0cab1-111">Im Dialogfeld wird das Ergebnis der Suche nach einem angegebenen Computer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0cab1-111">The dialog box shows the result of the search for a specified computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cab1-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="0cab1-112">Syntax</span></span>


```JScript
IShellDispatch.FindComputer()
```


```VB

IShellDispatch.FindComputer()
```





## <a name="parameters"></a><span data-ttu-id="0cab1-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="0cab1-113">Parameters</span></span>

<span data-ttu-id="0cab1-114">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="0cab1-114">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0cab1-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0cab1-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="0cab1-116">JScript</span><span class="sxs-lookup"><span data-stu-id="0cab1-116">JScript</span></span>

<span data-ttu-id="0cab1-117">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="0cab1-117">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="0cab1-118">VB</span><span class="sxs-lookup"><span data-stu-id="0cab1-118">VB</span></span>

<span data-ttu-id="0cab1-119">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="0cab1-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0cab1-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0cab1-120">Remarks</span></span>

<span data-ttu-id="0cab1-121">Diese Methode wird implementiert und über die [**Shell.FindComputer-Methode**](shell-findcomputer.md) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="0cab1-121">This method is implemented and accessed through the [**Shell.FindComputer**](shell-findcomputer.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="0cab1-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0cab1-122">Examples</span></span>

<span data-ttu-id="0cab1-123">Die folgenden Beispiele zeigen die Verwendung von **FindComputer** in JScript, VBScript und Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="0cab1-123">The following examples show the use of **FindComputer** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="0cab1-124">Jscript:</span><span class="sxs-lookup"><span data-stu-id="0cab1-124">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.FindComputer();
    }
</script>
```



<span data-ttu-id="0cab1-125">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="0cab1-125">VBScript:</span></span>


```VB
 <script language="VBScript">
    function fnShellFindComputerVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objshell.FindComputer

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="0cab1-126">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="0cab1-126">Visual Basic:</span></span>


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.FindComputer

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="0cab1-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0cab1-127">Requirements</span></span>



| <span data-ttu-id="0cab1-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0cab1-128">Requirement</span></span> | <span data-ttu-id="0cab1-129">Wert</span><span class="sxs-lookup"><span data-stu-id="0cab1-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cab1-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0cab1-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0cab1-131">Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0cab1-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0cab1-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0cab1-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0cab1-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0cab1-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0cab1-134">Header</span><span class="sxs-lookup"><span data-stu-id="0cab1-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cab1-135"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="0cab1-135"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="0cab1-136">Idl</span><span class="sxs-lookup"><span data-stu-id="0cab1-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0cab1-137"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="0cab1-137"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="0cab1-138">DLL</span><span class="sxs-lookup"><span data-stu-id="0cab1-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0cab1-139"><dt>Shell32.dll (Version 4.71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="0cab1-139"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




