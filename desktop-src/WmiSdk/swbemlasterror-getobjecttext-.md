---
description: Die getobjecttext- \_ Methode des-Objekts von "Swap-LastError" gibt ein Text Rendering des-Objekts in einem Managed Object Format-Format (MOF) zurück.
ms.assetid: efe3f3f6-c2f2-4295-bbf3-60d5b06ef98f
ms.tgt_platform: multiple
title: SWbemLastError.GetObjectText_-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.GetObjectText_
- ISWbemLastError.GetObjectText_
- ISWbemLastError.GetObjectText_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4247b5212e453c2f4393c26cd5ad63f07992c75a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959907"
---
# <a name="swbemlasterrorgetobjecttext_-method"></a><span data-ttu-id="a3121-103">Methode ' Swap. getobjecttext ' \_</span><span class="sxs-lookup"><span data-stu-id="a3121-103">SWbemLastError.GetObjectText\_ method</span></span>

<span data-ttu-id="a3121-104">Die **getobjecttext \_** -Methode des-Objekts von " [**Swap-LastError**](swbemlasterror.md) " gibt ein Text Rendering des-Objekts in einem Managed Object Format-Format [(MOF)](managed-object-format--mof-.md) zurück.</span><span class="sxs-lookup"><span data-stu-id="a3121-104">The **GetObjectText\_** method of the [**SWbemLastError**](swbemlasterror.md) object returns a textual rendering of the object in a [Managed Object Format (MOF)](managed-object-format--mof-.md) format.</span></span> <span data-ttu-id="a3121-105">Dieses MOF-Objekt kann verwendet werden, um den Inhalt eines Objekts anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a3121-105">This MOF object can be used to display an object's contents.</span></span> <span data-ttu-id="a3121-106">Beachten Sie, dass der MOF-Text, der zurückgegeben wird, nicht alle Informationen über das Objekt enthält, sondern nur genügend Informationen für den MOF-Compiler, um das ursprüngliche Objekt neu erstellen zu können.</span><span class="sxs-lookup"><span data-stu-id="a3121-106">Notice that the MOF text that is returned does not contain all the information about the object, but only enough information for the MOF compiler to be able to re-create the original object.</span></span> <span data-ttu-id="a3121-107">Sie finden beispielsweise keine Informationen zu den weiter gegebenen Qualifizierern oder den Eigenschaften der übergeordneten Klasse.</span><span class="sxs-lookup"><span data-stu-id="a3121-107">For instance, you will not find any information about the propagated qualifiers or the parent class properties.</span></span>

<span data-ttu-id="a3121-108">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="a3121-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a3121-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3121-109">Syntax</span></span>


```VB
strMofText = .GetObjectText_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="a3121-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3121-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3121-111">*IFlags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="a3121-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a3121-112">Dieser Parameter ist reserviert und muss 0 (null) sein, wenn angegeben.</span><span class="sxs-lookup"><span data-stu-id="a3121-112">This parameter is reserved and must be 0 (zero) if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3121-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a3121-113">Return value</span></span>

<span data-ttu-id="a3121-114">Bei erfolgreicher Ausführung gibt diese Methode eine Zeichenfolge zurück, die den Ausgabetext enthält.</span><span class="sxs-lookup"><span data-stu-id="a3121-114">If successful, this method returns a string that contains the output text.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a3121-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="a3121-115">Error codes</span></span>

<span data-ttu-id="a3121-116">Nach dem Abschluss der **\_ getobjecttext** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="a3121-116">Upon the completion of the **GetObjectText\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="a3121-117">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="a3121-117">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="a3121-118">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="a3121-118">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="a3121-119">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="a3121-119">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="a3121-120">Ein angegebener Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="a3121-120">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="a3121-121">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="a3121-121">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="a3121-122">Der Arbeitsspeicher reicht nicht aus, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="a3121-122">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a3121-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a3121-123">Requirements</span></span>



| <span data-ttu-id="a3121-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a3121-124">Requirement</span></span> | <span data-ttu-id="a3121-125">Wert</span><span class="sxs-lookup"><span data-stu-id="a3121-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3121-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a3121-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a3121-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a3121-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a3121-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a3121-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a3121-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a3121-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a3121-130">Header</span><span class="sxs-lookup"><span data-stu-id="a3121-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3121-131"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3121-131"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a3121-132">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="a3121-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="a3121-133"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a3121-133"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a3121-134">DLL</span><span class="sxs-lookup"><span data-stu-id="a3121-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3121-135"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3121-135"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a3121-136">CLSID</span><span class="sxs-lookup"><span data-stu-id="a3121-136">CLSID</span></span><br/>                    | <span data-ttu-id="a3121-137">CLSID- \_ Austausch Fehler</span><span class="sxs-lookup"><span data-stu-id="a3121-137">CLSID\_SWbemLastError</span></span><br/>                                                        |
| <span data-ttu-id="a3121-138">IID</span><span class="sxs-lookup"><span data-stu-id="a3121-138">IID</span></span><br/>                      | <span data-ttu-id="a3121-139">IID \_ iswbemlasterror</span><span class="sxs-lookup"><span data-stu-id="a3121-139">IID\_ISWbemLastError</span></span><br/>                                                         |



 

 




