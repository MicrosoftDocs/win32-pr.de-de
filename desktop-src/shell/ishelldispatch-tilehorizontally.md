---
description: Kachelt alle Fenster auf dem Desktop horizontal. Diese Methode hat denselben Effekt wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von gestapeltes Fenster anzeigen.
ms.assetid: 85785510-6B75-450a-A9BB-6C3B4F6194E2
title: Ishelldispatch. tilehorizontale-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.TileHorizontally
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 06491f797de4a9fcb5c431d85cff71fbc78d605c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130092"
---
# <a name="ishelldispatchtilehorizontally-method"></a><span data-ttu-id="1b723-104">Ishelldispatch. tilehorizontdent-Methode</span><span class="sxs-lookup"><span data-stu-id="1b723-104">IShellDispatch.TileHorizontally method</span></span>

<span data-ttu-id="1b723-105">Kachelt alle Fenster auf dem Desktop horizontal.</span><span class="sxs-lookup"><span data-stu-id="1b723-105">Tiles all of the windows on the desktop horizontally.</span></span> <span data-ttu-id="1b723-106">Diese Methode hat denselben Effekt wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von **Gestapeltes Fenster anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="1b723-106">This method has the same effect as right-clicking the taskbar and selecting **Show windows stacked**.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b723-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b723-107">Syntax</span></span>


```JScript
IShellDispatch.TileHorizontally()
```


```VB

IShellDispatch.TileHorizontally()
```





## <a name="parameters"></a><span data-ttu-id="1b723-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b723-108">Parameters</span></span>

<span data-ttu-id="1b723-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="1b723-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1b723-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1b723-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="1b723-111">JScript</span><span class="sxs-lookup"><span data-stu-id="1b723-111">JScript</span></span>

<span data-ttu-id="1b723-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1b723-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="1b723-113">VB</span><span class="sxs-lookup"><span data-stu-id="1b723-113">VB</span></span>

<span data-ttu-id="1b723-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1b723-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b723-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b723-115">Remarks</span></span>

<span data-ttu-id="1b723-116">Diese Methode wird implementiert, und der Zugriff erfolgt über die [**Shell. tilehorizontale**](shell-tilehorizontally.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="1b723-116">This method is implemented and accessed through the [**Shell.TileHorizontally**](shell-tilehorizontally.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="1b723-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1b723-117">Examples</span></span>

<span data-ttu-id="1b723-118">Das folgende Beispiel zeigt die Verwendung von **tilehorizontin** JScript, VBScript und Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1b723-118">The following example shows the use of **TileHorizontally** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="1b723-119">JScript</span><span class="sxs-lookup"><span data-stu-id="1b723-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTileHorizontallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.TileHorizontally();
    }
</script>
```



<span data-ttu-id="1b723-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="1b723-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellTileHorizontallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.TileHorizontally

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="1b723-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="1b723-121">Visual Basic:</span></span>


```VB
Private Sub fnShellTileHorizontallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.TileHorizontally

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="1b723-122">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="1b723-122">Requirements</span></span>



| <span data-ttu-id="1b723-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b723-123">Requirement</span></span> | <span data-ttu-id="1b723-124">Wert</span><span class="sxs-lookup"><span data-stu-id="1b723-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b723-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1b723-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1b723-126">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b723-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1b723-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1b723-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1b723-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b723-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1b723-129">Header</span><span class="sxs-lookup"><span data-stu-id="1b723-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b723-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b723-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="1b723-131">IDL</span><span class="sxs-lookup"><span data-stu-id="1b723-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1b723-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1b723-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="1b723-133">DLL</span><span class="sxs-lookup"><span data-stu-id="1b723-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b723-134"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="1b723-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




