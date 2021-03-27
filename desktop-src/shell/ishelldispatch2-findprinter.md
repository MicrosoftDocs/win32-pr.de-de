---
description: Zeigt das Dialogfeld Drucker suchen an.
ms.assetid: a3d1e810-f0cf-48ec-93da-5cc01117c5d4
title: IShellDispatch2. findprinter-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.FindPrinter
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 81124e3f0d04244b9b81e812e090bde25971c17c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214872"
---
# <a name="ishelldispatch2findprinter-method"></a><span data-ttu-id="c4ab5-103">IShellDispatch2. findprinter-Methode</span><span class="sxs-lookup"><span data-stu-id="c4ab5-103">IShellDispatch2.FindPrinter method</span></span>

<span data-ttu-id="c4ab5-104">Zeigt das Dialogfeld **Drucker suchen** an.</span><span class="sxs-lookup"><span data-stu-id="c4ab5-104">Displays the **Find Printer** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4ab5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4ab5-105">Syntax</span></span>


```JScript
iRetVal = IShellDispatch2.FindPrinter(
  [ sName ],
  [ sLocation ],
  [ sModel ]
)
```


```VB

IShellDispatch2.FindPrinter( _
  [ ByVal sName As BSTR ], _
  [ ByVal sLocation As BSTR ], _
  [ ByVal sModel As BSTR ] _
) As Integer
```





## <a name="parameters"></a><span data-ttu-id="c4ab5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4ab5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4ab5-107">*sname* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c4ab5-107">*sName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c4ab5-108">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="c4ab5-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="c4ab5-109">Eine **Zeichenfolge** , die den Drucker Namen enthält.</span><span class="sxs-lookup"><span data-stu-id="c4ab5-109">A **String** that contains the printer name.</span></span>

</dd> <dt>

<span data-ttu-id="c4ab5-110">*slotung* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c4ab5-110">*sLocation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c4ab5-111">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="c4ab5-111">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="c4ab5-112">Eine **Zeichenfolge** , die den Drucker Speicherort enthält.</span><span class="sxs-lookup"><span data-stu-id="c4ab5-112">A **String** that contains the printer location.</span></span>

</dd> <dt>

<span data-ttu-id="c4ab5-113">*smodel* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c4ab5-113">*sModel* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c4ab5-114">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="c4ab5-114">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="c4ab5-115">Eine **Zeichenfolge** , die das Drucker Modell enthält.</span><span class="sxs-lookup"><span data-stu-id="c4ab5-115">A **String** that contains the printer model.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c4ab5-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c4ab5-116">Remarks</span></span>

<span data-ttu-id="c4ab5-117">Diese Methode wird implementiert, und der Zugriff erfolgt über die [**Shell. findprinter**](./shell-findprinter.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="c4ab5-117">This method is implemented and accessed through the [**Shell.FindPrinter**](./shell-findprinter.md) method.</span></span>

<span data-ttu-id="c4ab5-118">Wenn Sie einem oder mehreren optionalen Parametern Zeichen folgen zuweisen, werden diese als Standardwerte im zugeordneten Bearbeitungs Steuerelement angezeigt, wenn das Dialogfeld " **Drucker suchen** " angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c4ab5-118">If you assign strings to one or more of the optional parameters, they are displayed as default values in the associated edit control when the **Find Printer** dialog box is displayed.</span></span> <span data-ttu-id="c4ab5-119">Der Benutzer kann diese Werte entweder annehmen oder außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="c4ab5-119">The user can either accept or override these values.</span></span> <span data-ttu-id="c4ab5-120">Wenn einem Parameter kein Wert zugewiesen wird, ist das zugehörige Bearbeitungsfeld leer, und der Benutzer muss einen Wert eingeben.</span><span class="sxs-lookup"><span data-stu-id="c4ab5-120">If no value is assigned to a parameter, the associated edit box is empty and the user must enter a value.</span></span>

<span data-ttu-id="c4ab5-121">Diese Methode ist zurzeit nicht in Microsoft Visual Basic verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c4ab5-121">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="c4ab5-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c4ab5-122">Examples</span></span>

<span data-ttu-id="c4ab5-123">In den folgenden Beispielen wird gezeigt, wie **findprinter** verwendet wird, um das Dialogfeld **Drucker** suchen für eine bestimmte Anwendung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c4ab5-123">The following examples show the use of **FindPrinter** to display the **Find Printer** dialog box for a particular application.</span></span> <span data-ttu-id="c4ab5-124">Die Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c4ab5-124">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="c4ab5-125">JScript</span><span class="sxs-lookup"><span data-stu-id="c4ab5-125">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFindPrinterJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindPrinter();
    }
</script>
```



<span data-ttu-id="c4ab5-126">VBScript</span><span class="sxs-lookup"><span data-stu-id="c4ab5-126">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFindPrinterVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")
        objShell.FindPrinter()

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="c4ab5-127">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c4ab5-127">Requirements</span></span>



| <span data-ttu-id="c4ab5-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c4ab5-128">Requirement</span></span> | <span data-ttu-id="c4ab5-129">Wert</span><span class="sxs-lookup"><span data-stu-id="c4ab5-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4ab5-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c4ab5-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c4ab5-131">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c4ab5-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c4ab5-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c4ab5-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c4ab5-133">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c4ab5-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c4ab5-134">Header</span><span class="sxs-lookup"><span data-stu-id="c4ab5-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4ab5-135"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4ab5-135"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="c4ab5-136">IDL</span><span class="sxs-lookup"><span data-stu-id="c4ab5-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c4ab5-137"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c4ab5-137"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="c4ab5-138">DLL</span><span class="sxs-lookup"><span data-stu-id="c4ab5-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4ab5-139"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="c4ab5-139"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
