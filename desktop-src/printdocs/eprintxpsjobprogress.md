---
description: Gibt an, wie der Spooler gerade ausgeführt wird, während er einen XPS-Druckauftrag verarbeitet.
ms.assetid: 4fa5b749-e4f9-4f08-97b5-e58f82d0b485
title: Eprintxpsjobprogress-Enumeration (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EPrintXPSJobProgress
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 2a09b55ed72a6276a1a9d224cc08e03546f887d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529543"
---
# <a name="eprintxpsjobprogress-enumeration"></a><span data-ttu-id="e28e6-103">Eprintxpsjobprogress-Enumeration</span><span class="sxs-lookup"><span data-stu-id="e28e6-103">EPrintXPSJobProgress enumeration</span></span>

<span data-ttu-id="e28e6-104">Gibt an, wie der Spooler gerade ausgeführt wird, während er einen XPS-Druckauftrag verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="e28e6-104">Specifies what the spooler is currently doing as it processes an XPS print job.</span></span>

## <a name="syntax"></a><span data-ttu-id="e28e6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e28e6-105">Syntax</span></span>


```C++
typedef enum tagEPrintXPSJobProgress { 
  kAddingDocumentSequence,
  kDocumentSequenceAdded,
  kAddingFixedDocument,
  kFixedDocumentAdded,
  kAddingFixedPage,
  kFixedPageAdded,
  kResourceAdded,
  kFontAdded,
  kImageAdded,
  kXpsDocumentCommitted
} EPrintXPSJobProgress;
```



## <a name="constants"></a><span data-ttu-id="e28e6-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="e28e6-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e28e6-107"><span id="kAddingDocumentSequence"></span><span id="kaddingdocumentsequence"></span><span id="KADDINGDOCUMENTSEQUENCE"></span>**kaddingdocumentsequence**</span><span class="sxs-lookup"><span data-stu-id="e28e6-107"><span id="kAddingDocumentSequence"></span><span id="kaddingdocumentsequence"></span><span id="KADDINGDOCUMENTSEQUENCE"></span>**kAddingDocumentSequence**</span></span>
</dt> <dd>

<span data-ttu-id="e28e6-108">Eine Dokument Sequenz wird dem XPS-Auftrag hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e28e6-108">A document sequence is about to be added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="e28e6-109"><span id="kDocumentSequenceAdded"></span><span id="kdocumentsequenceadded"></span><span id="KDOCUMENTSEQUENCEADDED"></span>**kdocumentsequenceadded**</span><span class="sxs-lookup"><span data-stu-id="e28e6-109"><span id="kDocumentSequenceAdded"></span><span id="kdocumentsequenceadded"></span><span id="KDOCUMENTSEQUENCEADDED"></span>**kDocumentSequenceAdded**</span></span>
</dt> <dd>

<span data-ttu-id="e28e6-110">Eine Dokument Sequenz wurde dem XPS-Auftrag hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e28e6-110">A document sequence has been added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="e28e6-111"><span id="kAddingFixedDocument"></span><span id="kaddingfixeddocument"></span><span id="KADDINGFIXEDDOCUMENT"></span>**kaddingfixeddocument**</span><span class="sxs-lookup"><span data-stu-id="e28e6-111"><span id="kAddingFixedDocument"></span><span id="kaddingfixeddocument"></span><span id="KADDINGFIXEDDOCUMENT"></span>**kAddingFixedDocument**</span></span>
</dt> <dd>

<span data-ttu-id="e28e6-112">Ein festes Dokument wird dem XPS-Auftrag hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e28e6-112">A fixed document is about to be added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="e28e6-113"><span id="kFixedDocumentAdded"></span><span id="kfixeddocumentadded"></span><span id="KFIXEDDOCUMENTADDED"></span>**kfixeddocumentadded**</span><span class="sxs-lookup"><span data-stu-id="e28e6-113"><span id="kFixedDocumentAdded"></span><span id="kfixeddocumentadded"></span><span id="KFIXEDDOCUMENTADDED"></span>**kFixedDocumentAdded**</span></span>
</dt> <dd>

<span data-ttu-id="e28e6-114">Dem XPS-Auftrag wurde ein festes Dokument hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e28e6-114">A fixed document has been added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="e28e6-115"><span id="kAddingFixedPage"></span><span id="kaddingfixedpage"></span><span id="KADDINGFIXEDPAGE"></span>**kaddingfixedpage**</span><span class="sxs-lookup"><span data-stu-id="e28e6-115"><span id="kAddingFixedPage"></span><span id="kaddingfixedpage"></span><span id="KADDINGFIXEDPAGE"></span>**kAddingFixedPage**</span></span>
</dt> <dd>

<span data-ttu-id="e28e6-116">Eine Seite wird dem XPS-Auftrag hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e28e6-116">A page is about to be added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="e28e6-117"><span id="kFixedPageAdded"></span><span id="kfixedpageadded"></span><span id="KFIXEDPAGEADDED"></span>**kfixedpageadded**</span><span class="sxs-lookup"><span data-stu-id="e28e6-117"><span id="kFixedPageAdded"></span><span id="kfixedpageadded"></span><span id="KFIXEDPAGEADDED"></span>**kFixedPageAdded**</span></span>
</dt> <dd>

<span data-ttu-id="e28e6-118">Dem XPS-Auftrag wurde eine Seite hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e28e6-118">A page has been added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="e28e6-119"><span id="kResourceAdded"></span><span id="kresourceadded"></span><span id="KRESOURCEADDED"></span>**kresourceadded**</span><span class="sxs-lookup"><span data-stu-id="e28e6-119"><span id="kResourceAdded"></span><span id="kresourceadded"></span><span id="KRESOURCEADDED"></span>**kResourceAdded**</span></span>
</dt> <dd>

<span data-ttu-id="e28e6-120">Dem XPS-Auftrag wurde eine Ressource hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e28e6-120">A resource had been added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="e28e6-121"><span id="kFontAdded"></span><span id="kfontadded"></span><span id="KFONTADDED"></span>**kfontadded**</span><span class="sxs-lookup"><span data-stu-id="e28e6-121"><span id="kFontAdded"></span><span id="kfontadded"></span><span id="KFONTADDED"></span>**kFontAdded**</span></span>
</dt> <dd>

<span data-ttu-id="e28e6-122">Dem XPS-Auftrag wurde eine Schriftart hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e28e6-122">A font has been added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="e28e6-123"><span id="kImageAdded"></span><span id="kimageadded"></span><span id="KIMAGEADDED"></span>**kimageadded**</span><span class="sxs-lookup"><span data-stu-id="e28e6-123"><span id="kImageAdded"></span><span id="kimageadded"></span><span id="KIMAGEADDED"></span>**kImageAdded**</span></span>
</dt> <dd>

<span data-ttu-id="e28e6-124">Dem XPS-Auftrag wurde ein Bild hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e28e6-124">An image has been added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="e28e6-125"><span id="kXpsDocumentCommitted"></span><span id="kxpsdocumentcommitted"></span><span id="KXPSDOCUMENTCOMMITTED"></span>**kxpsdocumentcommit**</span><span class="sxs-lookup"><span data-stu-id="e28e6-125"><span id="kXpsDocumentCommitted"></span><span id="kxpsdocumentcommitted"></span><span id="KXPSDOCUMENTCOMMITTED"></span>**kXpsDocumentCommitted**</span></span>
</dt> <dd>

<span data-ttu-id="e28e6-126">Für die Daten für den XPS-Auftrag wurde ein Commit ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e28e6-126">The data for the XPS job has been committed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e28e6-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e28e6-127">Remarks</span></span>

<span data-ttu-id="e28e6-128">Diese Enumeration wird primär als Parameter für die [**reportjobprocessingprogress**](reportjobprocessingprogress.md) -Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="e28e6-128">This enumeration is primarily used as a parameter for the [**ReportJobProcessingProgress**](reportjobprocessingprogress.md) function.</span></span>

<span data-ttu-id="e28e6-129">Diese Werte können entweder auf die spoolingphase oder die Renderingphase eines Druckauftrags verweisen.</span><span class="sxs-lookup"><span data-stu-id="e28e6-129">These values can refer to either the spooling or the rendering phase of a print job.</span></span>

## <a name="requirements"></a><span data-ttu-id="e28e6-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e28e6-130">Requirements</span></span>



| <span data-ttu-id="e28e6-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e28e6-131">Requirement</span></span> | <span data-ttu-id="e28e6-132">Wert</span><span class="sxs-lookup"><span data-stu-id="e28e6-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e28e6-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e28e6-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e28e6-134">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e28e6-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="e28e6-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e28e6-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e28e6-136">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e28e6-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e28e6-137">Header</span><span class="sxs-lookup"><span data-stu-id="e28e6-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="e28e6-138"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e28e6-138"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



 

 




