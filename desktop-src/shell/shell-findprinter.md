---
description: Zeigt das Dialogfeld Drucker suchen an.
ms.assetid: 61C700CF-623B-4c99-A211-AC26A1E4AE85
title: Shell. findprinter-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.FindPrinter
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1286bb7247359ea91d29a53f8f0eaa13b55be5e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980633"
---
# <a name="shellfindprinter-method"></a><span data-ttu-id="cbc77-103">Shell. findprinter-Methode</span><span class="sxs-lookup"><span data-stu-id="cbc77-103">Shell.FindPrinter method</span></span>

<span data-ttu-id="cbc77-104">Zeigt das Dialogfeld **Drucker suchen** an.</span><span class="sxs-lookup"><span data-stu-id="cbc77-104">Displays the **Find Printer** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbc77-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cbc77-105">Syntax</span></span>


```JScript
iRetVal = Shell.FindPrinter(
  [ sName ],
  [ sLocation ],
  [ sModel ]
)
```


```VB

Shell.FindPrinter( _
  [ ByVal sName As BSTR ], _
  [ ByVal sLocation As BSTR ], _
  [ ByVal sModel As BSTR ] _
) As Integer
```





## <a name="parameters"></a><span data-ttu-id="cbc77-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cbc77-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbc77-107">*sname* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="cbc77-107">*sName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cbc77-108">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="cbc77-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="cbc77-109">Eine **Zeichenfolge** , die den Drucker Namen enthält.</span><span class="sxs-lookup"><span data-stu-id="cbc77-109">A **String** that contains the printer name.</span></span>

</dd> <dt>

<span data-ttu-id="cbc77-110">*slotung* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="cbc77-110">*sLocation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cbc77-111">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="cbc77-111">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="cbc77-112">Eine **Zeichenfolge** , die den Drucker Speicherort enthält.</span><span class="sxs-lookup"><span data-stu-id="cbc77-112">A **String** that contains the printer location.</span></span>

</dd> <dt>

<span data-ttu-id="cbc77-113">*smodel* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="cbc77-113">*sModel* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cbc77-114">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="cbc77-114">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="cbc77-115">Eine **Zeichenfolge** , die das Drucker Modell enthält.</span><span class="sxs-lookup"><span data-stu-id="cbc77-115">A **String** that contains the printer model.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cbc77-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cbc77-116">Remarks</span></span>

<span data-ttu-id="cbc77-117">Wenn Sie einem oder mehreren optionalen Parametern Zeichen folgen zuweisen, werden diese als Standardwerte im zugeordneten Bearbeitungs Steuerelement angezeigt, wenn das Dialogfeld " **Drucker suchen** " angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="cbc77-117">If you assign strings to one or more of the optional parameters, they are displayed as default values in the associated edit control when the **Find Printer** dialog box is displayed.</span></span> <span data-ttu-id="cbc77-118">Der Benutzer kann diese Werte entweder annehmen oder außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="cbc77-118">The user can either accept or override these values.</span></span> <span data-ttu-id="cbc77-119">Wenn einem Parameter kein Wert zugewiesen wird, ist das zugehörige Bearbeitungsfeld leer, und der Benutzer muss einen Wert eingeben.</span><span class="sxs-lookup"><span data-stu-id="cbc77-119">If no value is assigned to a parameter, the associated edit box is empty and the user must enter a value.</span></span>

<span data-ttu-id="cbc77-120">Diese Methode ist zurzeit nicht in Microsoft Visual Basic verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cbc77-120">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="cbc77-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cbc77-121">Examples</span></span>

<span data-ttu-id="cbc77-122">In den folgenden Beispielen wird gezeigt, wie **findprinter** verwendet wird, um das Dialogfeld **Drucker** suchen für eine bestimmte Anwendung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="cbc77-122">The following examples show the use of **FindPrinter** to display the **Find Printer** dialog box for a particular application.</span></span> <span data-ttu-id="cbc77-123">Die Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cbc77-123">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="cbc77-124">JScript</span><span class="sxs-lookup"><span data-stu-id="cbc77-124">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFindPrinterJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindPrinter();
    }
</script>
```



<span data-ttu-id="cbc77-125">VBScript</span><span class="sxs-lookup"><span data-stu-id="cbc77-125">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="cbc77-126">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="cbc77-126">Requirements</span></span>



| <span data-ttu-id="cbc77-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cbc77-127">Requirement</span></span> | <span data-ttu-id="cbc77-128">Wert</span><span class="sxs-lookup"><span data-stu-id="cbc77-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbc77-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cbc77-129">Minimum supported client</span></span><br/> | <span data-ttu-id="cbc77-130">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cbc77-130">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cbc77-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cbc77-131">Minimum supported server</span></span><br/> | <span data-ttu-id="cbc77-132">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cbc77-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="cbc77-133">Header</span><span class="sxs-lookup"><span data-stu-id="cbc77-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbc77-134"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbc77-134"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="cbc77-135">IDL</span><span class="sxs-lookup"><span data-stu-id="cbc77-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cbc77-136"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cbc77-136"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="cbc77-137">DLL</span><span class="sxs-lookup"><span data-stu-id="cbc77-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbc77-138"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="cbc77-138"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
