---
description: 'Shell.FindPrinter-Methode: Zeigt das Dialogfeld Drucker suchen an.'
ms.assetid: 61C700CF-623B-4c99-A211-AC26A1E4AE85
title: Shell.FindPrinter-Methode (Shldisp.h)
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
ms.openlocfilehash: 17d04b60de2b52ca3d2f17fbdccf7de93ac095b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104308"
---
# <a name="shellfindprinter-method"></a><span data-ttu-id="ba19c-103">Shell.FindPrinter-Methode</span><span class="sxs-lookup"><span data-stu-id="ba19c-103">Shell.FindPrinter method</span></span>

<span data-ttu-id="ba19c-104">Zeigt das **Dialogfeld Drucker suchen** an.</span><span class="sxs-lookup"><span data-stu-id="ba19c-104">Displays the **Find Printer** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba19c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba19c-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="ba19c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba19c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba19c-107">*sName* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="ba19c-107">*sName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ba19c-108">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="ba19c-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="ba19c-109">Eine **Zeichenfolge,** die den Druckernamen enthält.</span><span class="sxs-lookup"><span data-stu-id="ba19c-109">A **String** that contains the printer name.</span></span>

</dd> <dt>

<span data-ttu-id="ba19c-110">*sLocation* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="ba19c-110">*sLocation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ba19c-111">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="ba19c-111">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="ba19c-112">Eine **Zeichenfolge,** die den Druckerspeicherort enthält.</span><span class="sxs-lookup"><span data-stu-id="ba19c-112">A **String** that contains the printer location.</span></span>

</dd> <dt>

<span data-ttu-id="ba19c-113">*sModel* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="ba19c-113">*sModel* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ba19c-114">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="ba19c-114">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="ba19c-115">Eine **Zeichenfolge,** die das Druckermodell enthält.</span><span class="sxs-lookup"><span data-stu-id="ba19c-115">A **String** that contains the printer model.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ba19c-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ba19c-116">Remarks</span></span>

<span data-ttu-id="ba19c-117">Wenn Sie einem oder mehrere der optionalen Parameter Zeichenfolgen zuweisen, werden sie  als Standardwerte im zugeordneten Bearbeitungssteuerfeld angezeigt, wenn das Dialogfeld Drucker suchen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ba19c-117">If you assign strings to one or more of the optional parameters, they are displayed as default values in the associated edit control when the **Find Printer** dialog box is displayed.</span></span> <span data-ttu-id="ba19c-118">Der Benutzer kann diese Werte entweder akzeptieren oder überschreiben.</span><span class="sxs-lookup"><span data-stu-id="ba19c-118">The user can either accept or override these values.</span></span> <span data-ttu-id="ba19c-119">Wenn einem Parameter kein Wert zugewiesen wird, ist das zugeordnete Bearbeitungsfeld leer, und der Benutzer muss einen Wert eingeben.</span><span class="sxs-lookup"><span data-stu-id="ba19c-119">If no value is assigned to a parameter, the associated edit box is empty and the user must enter a value.</span></span>

<span data-ttu-id="ba19c-120">Diese Methode ist derzeit in Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ba19c-120">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="ba19c-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ba19c-121">Examples</span></span>

<span data-ttu-id="ba19c-122">In den folgenden Beispielen wird die Verwendung **von FindPrinter** zum Anzeigen **des** Dialogfelds Drucker suchen für eine bestimmte Anwendung gezeigt.</span><span class="sxs-lookup"><span data-stu-id="ba19c-122">The following examples show the use of **FindPrinter** to display the **Find Printer** dialog box for a particular application.</span></span> <span data-ttu-id="ba19c-123">Die Verwendung wird für JScript, VBScript und Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ba19c-123">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="ba19c-124">Jscript:</span><span class="sxs-lookup"><span data-stu-id="ba19c-124">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFindPrinterJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindPrinter();
    }
</script>
```



<span data-ttu-id="ba19c-125">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="ba19c-125">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="ba19c-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ba19c-126">Requirements</span></span>



| <span data-ttu-id="ba19c-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ba19c-127">Requirement</span></span> | <span data-ttu-id="ba19c-128">Wert</span><span class="sxs-lookup"><span data-stu-id="ba19c-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba19c-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ba19c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ba19c-130">Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ba19c-130">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ba19c-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ba19c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ba19c-132">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ba19c-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ba19c-133">Header</span><span class="sxs-lookup"><span data-stu-id="ba19c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba19c-134"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="ba19c-134"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="ba19c-135">Idl</span><span class="sxs-lookup"><span data-stu-id="ba19c-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ba19c-136"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="ba19c-136"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="ba19c-137">DLL</span><span class="sxs-lookup"><span data-stu-id="ba19c-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba19c-138"><dt>Shell32.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="ba19c-138"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
