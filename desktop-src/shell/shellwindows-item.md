---
description: Ruft ein InternetExplorer-Objekt ab, das das Shellfenster darstellt.
ms.assetid: 32390f35-f83a-45d9-a240-282da7cb2b13
title: Shellwindows. Item-Methode (Exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows.Item
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ccdb73deb1d97d9c6e1ad8c335db3c58d796a299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216417"
---
# <a name="shellwindowsitem-method"></a><span data-ttu-id="46929-103">Shellwindows. Item-Methode</span><span class="sxs-lookup"><span data-stu-id="46929-103">ShellWindows.Item method</span></span>

<span data-ttu-id="46929-104">Ruft ein [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) -Objekt ab, das das Shellfenster darstellt.</span><span class="sxs-lookup"><span data-stu-id="46929-104">Retrieves an [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) object that represents the Shell window.</span></span>

## <a name="syntax"></a><span data-ttu-id="46929-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="46929-105">Syntax</span></span>


```JScript
retVal = ShellWindows.Item(
  [ iIndex ]
)
```



## <a name="parameters"></a><span data-ttu-id="46929-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="46929-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46929-107">*iIndex* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="46929-107">*iIndex* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="46929-108">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="46929-108">Type: **Variant**</span></span>

<span data-ttu-id="46929-109">Der nullbasierte Index des abzurufenden Elements.</span><span class="sxs-lookup"><span data-stu-id="46929-109">The zero-based index of the item to retrieve.</span></span> <span data-ttu-id="46929-110">Dieser Wert muss kleiner sein als der Wert der [**count**](shellwindows-count.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="46929-110">This value must be less than the value of the [**Count**](shellwindows-count.md) property.</span></span> <span data-ttu-id="46929-111">Wenn dieser Wert weggelassen wird, wird der Standardwert 0 verwendet.</span><span class="sxs-lookup"><span data-stu-id="46929-111">If this value is omitted, a default value of 0 is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46929-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="46929-112">Return value</span></span>

<span data-ttu-id="46929-113">Typ: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="46929-113">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="46929-114">Ein Objekt Verweis auf das [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) -Objekt, das das Shellfenster darstellt.</span><span class="sxs-lookup"><span data-stu-id="46929-114">An object reference to the [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) object that represents the Shell window.</span></span>

## <a name="examples"></a><span data-ttu-id="46929-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="46929-115">Examples</span></span>

<span data-ttu-id="46929-116">Im folgenden Beispiel wird das- [**Element**](folderitemverbs-item.md) verwendet, um das [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) -Objekt abzurufen, das das erste shellfensterelement darstellt.</span><span class="sxs-lookup"><span data-stu-id="46929-116">The following example uses [**Item**](folderitemverbs-item.md) to retrieve the [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) object that represents the first Shell window item.</span></span> <span data-ttu-id="46929-117">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="46929-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="46929-118">JScript</span><span class="sxs-lookup"><span data-stu-id="46929-118">JScript:</span></span>


```JavaScript
<script language="JScript">
    function fnShellWindowsItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objShellWindows;
        
        objShellWindows = objshell.Windows();
        if (objShellWindows != null)
        {
            var objIE;
            objIE = objShellWindows.Item();

            if (objIE != null)
            {
                alert(objIE.path());
            }
        }
    }
</script>
```



<span data-ttu-id="46929-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="46929-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellWindowsItemVB()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objshell.Windows()

        if (not objShellWindows is nothing) then
            dim objIE
            set objIE = objShellWindows.Item

            if (not objIE is nothing) then
                Wscript.Echo objIE.path
            end if

            set objIE = nothing
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="46929-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="46929-120">Visual Basic:</span></span>


```VB
Private Sub fnShellWindowsItemVB()
    Dim objShell        As Shell
    Dim objShellWindows As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objshell.Windows()

    If (Not objShellWindows Is Nothing) Then
        Dim objIE As InternetExplorer
        Set objIE = objShellWindows.Item

        If (Not objIE Is Nothing) Then
            Debug.Print objIE.Path
        End If

        Set objIE = Nothing
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="46929-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="46929-121">Requirements</span></span>



| <span data-ttu-id="46929-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46929-122">Requirement</span></span> | <span data-ttu-id="46929-123">Wert</span><span class="sxs-lookup"><span data-stu-id="46929-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46929-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="46929-124">Minimum supported client</span></span><br/> | <span data-ttu-id="46929-125">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="46929-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="46929-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="46929-126">Minimum supported server</span></span><br/> | <span data-ttu-id="46929-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="46929-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="46929-128">Header</span><span class="sxs-lookup"><span data-stu-id="46929-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="46929-129"><dt>Exdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="46929-129"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="46929-130">DLL</span><span class="sxs-lookup"><span data-stu-id="46929-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46929-131"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="46929-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
