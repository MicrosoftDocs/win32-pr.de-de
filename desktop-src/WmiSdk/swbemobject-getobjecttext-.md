---
description: Die getobjecttext- \_ Methode des "errbemubject"-Objekts gibt ein Text Rendering des-Objekts zurück.
ms.assetid: 8b980863-14ad-4884-8897-dd076d927824
ms.tgt_platform: multiple
title: SWbemObject.GetObjectText_-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.GetObjectText_
- ISWbemObject.GetObjectText_
- ISWbemObject.GetObjectText_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2447d8361d02626e1f5ea8fae1928ffd563d52ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359988"
---
# <a name="swbemobjectgetobjecttext_-method"></a><span data-ttu-id="bc1b4-103">Errbemubject. getobjecttext- \_ Methode</span><span class="sxs-lookup"><span data-stu-id="bc1b4-103">SWbemObject.GetObjectText\_ method</span></span>

<span data-ttu-id="bc1b4-104">Die **getobjecttext \_** -Methode des " [**errbemubject**](swbemobject.md) "-Objekts gibt ein Text Rendering des-Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="bc1b4-104">The **GetObjectText\_** method of the [**SWbemObject**](swbemobject.md) object returns a textual rendering of the object.</span></span> <span data-ttu-id="bc1b4-105">Dieses Objekt kann verwendet werden, um den Inhalt eines Objekts anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="bc1b4-105">This object can be used to display an object's contents.</span></span> <span data-ttu-id="bc1b4-106">Derzeit wird nur die MOF-Syntax als Ausgabeformat unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bc1b4-106">Currently, only the MOF syntax is supported as an output format.</span></span> <span data-ttu-id="bc1b4-107">Beachten Sie, dass der zurückgegebene MOF-Text nicht alle Informationen über das Objekt enthält. der MOF-Text enthält nur genügend Informationen, damit der MOF-Compiler das ursprüngliche Objekt neu erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="bc1b4-107">Notice that the MOF text returned does not contain all the information about the object; the MOF text contains only enough information for the MOF compiler to be able to re-create the original object.</span></span> <span data-ttu-id="bc1b4-108">Beispielsweise gibt es keine Informationen zu den propagierten Qualifizierern oder den Eigenschaften der übergeordneten Klasse.</span><span class="sxs-lookup"><span data-stu-id="bc1b4-108">For instance, there is no information about the propagated qualifiers or the parent class properties.</span></span>

<span data-ttu-id="bc1b4-109">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="bc1b4-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bc1b4-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc1b4-110">Syntax</span></span>


```VB
strMofText = .GetObjectText_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="bc1b4-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc1b4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc1b4-112">*IFlags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="bc1b4-112">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bc1b4-113">Reserviert und muss 0 (null) sein, wenn angegeben.</span><span class="sxs-lookup"><span data-stu-id="bc1b4-113">Reserved and must be 0 (zero) if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc1b4-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bc1b4-114">Return value</span></span>

<span data-ttu-id="bc1b4-115">Bei erfolgreicher Ausführung gibt diese Methode eine Zeichenfolge zurück, die den Ausgabetext enthält.</span><span class="sxs-lookup"><span data-stu-id="bc1b4-115">If successful, this method returns a string that contains the output text.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bc1b4-116">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="bc1b4-116">Error codes</span></span>

<span data-ttu-id="bc1b4-117">Nach dem Abschluss der **\_ getobjecttext** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="bc1b4-117">After the completion of the **GetObjectText\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="bc1b4-118">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="bc1b4-118">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="bc1b4-119">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="bc1b4-119">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="bc1b4-120">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="bc1b4-120">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="bc1b4-121">Es wurde ein ungültiger Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="bc1b4-121">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="bc1b4-122">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="bc1b4-122">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="bc1b4-123">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="bc1b4-123">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="bc1b4-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bc1b4-124">Examples</span></span>

<span data-ttu-id="bc1b4-125">Der folgende Code, der aus der [Liste die Definition einer WMI-Klasse im MOF-Format](https://Gallery.TechNet.Microsoft.Com/6bb54091-dd6f-4d0b-87af-2431fb8c3be6) VBScript-Codebeispiel in der TechNet-Galerie stammt, ruft die Textdarstellung einer WMI-Klassen Definition in der MOF-Syntax (Managed Object Format) ab und zeigt diese an.</span><span class="sxs-lookup"><span data-stu-id="bc1b4-125">The following code, taken from the [List the Definition of a WMI Class in MOF Format](https://Gallery.TechNet.Microsoft.Com/6bb54091-dd6f-4d0b-87af-2431fb8c3be6) VBScript code sample in the TechNet Gallery, retrieves and displays the textual representation of a WMI class definition in MOF (Managed Object Format) syntax.</span></span>


```VB
strComputer = "." 
strNameSpace = "root\cimv2" 
strClass = "Win32_Service" 
  
Const wbemFlagUseAmendedQualifiers = &h20000 
  
Set objClass = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\" & strNameSpace) 
 
Set objClass = objWMIService.Get(strClass, wbemFlagUseAmendedQualifiers) 
strMOF = objClass.GetObjectText_ 
  
WScript.Echo strMOF 
```



## <a name="requirements"></a><span data-ttu-id="bc1b4-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc1b4-126">Requirements</span></span>



| <span data-ttu-id="bc1b4-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc1b4-127">Requirement</span></span> | <span data-ttu-id="bc1b4-128">Wert</span><span class="sxs-lookup"><span data-stu-id="bc1b4-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc1b4-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bc1b4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="bc1b4-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bc1b4-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bc1b4-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bc1b4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="bc1b4-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bc1b4-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bc1b4-133">Header</span><span class="sxs-lookup"><span data-stu-id="bc1b4-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc1b4-134"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc1b4-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bc1b4-135">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="bc1b4-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="bc1b4-136"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bc1b4-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bc1b4-137">DLL</span><span class="sxs-lookup"><span data-stu-id="bc1b4-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc1b4-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc1b4-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="bc1b4-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="bc1b4-139">CLSID</span></span><br/>                    | <span data-ttu-id="bc1b4-140">CLSID- \_ Austausch Objekt</span><span class="sxs-lookup"><span data-stu-id="bc1b4-140">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="bc1b4-141">IID</span><span class="sxs-lookup"><span data-stu-id="bc1b4-141">IID</span></span><br/>                      | <span data-ttu-id="bc1b4-142">IID \_ iswbemujekt</span><span class="sxs-lookup"><span data-stu-id="bc1b4-142">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




