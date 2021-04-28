---
description: 'IShellDispatch2.FindPrinter-Methode: Zeigt das Dialogfeld Drucker suchen an.'
ms.assetid: a3d1e810-f0cf-48ec-93da-5cc01117c5d4
title: IShellDispatch2.FindPrinter-Methode (Shldisp.h)
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
ms.openlocfilehash: 64a3975039255de76b3e59432b0848cc2cb1795b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117118"
---
# <a name="ishelldispatch2findprinter-method"></a><span data-ttu-id="43ac8-103">IShellDispatch2.FindPrinter-Methode</span><span class="sxs-lookup"><span data-stu-id="43ac8-103">IShellDispatch2.FindPrinter method</span></span>

<span data-ttu-id="43ac8-104">Zeigt das Dialogfeld **Drucker suchen** an.</span><span class="sxs-lookup"><span data-stu-id="43ac8-104">Displays the **Find Printer** dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="43ac8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="43ac8-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="43ac8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="43ac8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43ac8-107">*sName* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="43ac8-107">*sName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="43ac8-108">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="43ac8-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="43ac8-109">Eine **Zeichenfolge,** die den Druckernamen enthält.</span><span class="sxs-lookup"><span data-stu-id="43ac8-109">A **String** that contains the printer name.</span></span>

</dd> <dt>

<span data-ttu-id="43ac8-110">*sLocation* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="43ac8-110">*sLocation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="43ac8-111">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="43ac8-111">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="43ac8-112">Eine **Zeichenfolge,** die den Druckerspeicherort enthält.</span><span class="sxs-lookup"><span data-stu-id="43ac8-112">A **String** that contains the printer location.</span></span>

</dd> <dt>

<span data-ttu-id="43ac8-113">*sModel* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="43ac8-113">*sModel* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="43ac8-114">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="43ac8-114">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="43ac8-115">Eine **Zeichenfolge,** die das Druckermodell enthält.</span><span class="sxs-lookup"><span data-stu-id="43ac8-115">A **String** that contains the printer model.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="43ac8-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="43ac8-116">Remarks</span></span>

<span data-ttu-id="43ac8-117">Diese Methode wird implementiert und über die [**Shell.FindPrinter-Methode**](./shell-findprinter.md) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="43ac8-117">This method is implemented and accessed through the [**Shell.FindPrinter**](./shell-findprinter.md) method.</span></span>

<span data-ttu-id="43ac8-118">Wenn Sie einem oder mehreren optionalen Parametern Zeichenfolgen zuweisen, werden diese im zugeordneten Bearbeitungssteuerelement als Standardwerte angezeigt, wenn das Dialogfeld **Drucker suchen** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="43ac8-118">If you assign strings to one or more of the optional parameters, they are displayed as default values in the associated edit control when the **Find Printer** dialog box is displayed.</span></span> <span data-ttu-id="43ac8-119">Der Benutzer kann diese Werte entweder akzeptieren oder überschreiben.</span><span class="sxs-lookup"><span data-stu-id="43ac8-119">The user can either accept or override these values.</span></span> <span data-ttu-id="43ac8-120">Wenn einem Parameter kein Wert zugewiesen ist, ist das zugeordnete Bearbeitungsfeld leer, und der Benutzer muss einen Wert eingeben.</span><span class="sxs-lookup"><span data-stu-id="43ac8-120">If no value is assigned to a parameter, the associated edit box is empty and the user must enter a value.</span></span>

<span data-ttu-id="43ac8-121">Diese Methode ist derzeit in Microsoft Visual Basic nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="43ac8-121">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="43ac8-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="43ac8-122">Examples</span></span>

<span data-ttu-id="43ac8-123">In den folgenden Beispielen wird die Verwendung von **FindPrinter** zum Anzeigen des Dialogfelds **Drucker suchen** für eine bestimmte Anwendung gezeigt.</span><span class="sxs-lookup"><span data-stu-id="43ac8-123">The following examples show the use of **FindPrinter** to display the **Find Printer** dialog box for a particular application.</span></span> <span data-ttu-id="43ac8-124">Die Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="43ac8-124">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="43ac8-125">Jscript:</span><span class="sxs-lookup"><span data-stu-id="43ac8-125">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFindPrinterJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindPrinter();
    }
</script>
```



<span data-ttu-id="43ac8-126">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="43ac8-126">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="43ac8-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43ac8-127">Requirements</span></span>



| <span data-ttu-id="43ac8-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43ac8-128">Requirement</span></span> | <span data-ttu-id="43ac8-129">Wert</span><span class="sxs-lookup"><span data-stu-id="43ac8-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43ac8-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="43ac8-130">Minimum supported client</span></span><br/> | <span data-ttu-id="43ac8-131">Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43ac8-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="43ac8-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="43ac8-132">Minimum supported server</span></span><br/> | <span data-ttu-id="43ac8-133">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43ac8-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="43ac8-134">Header</span><span class="sxs-lookup"><span data-stu-id="43ac8-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="43ac8-135"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="43ac8-135"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="43ac8-136">Idl</span><span class="sxs-lookup"><span data-stu-id="43ac8-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="43ac8-137"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="43ac8-137"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="43ac8-138">DLL</span><span class="sxs-lookup"><span data-stu-id="43ac8-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43ac8-139"><dt>Shell32.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="43ac8-139"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
