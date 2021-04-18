---
title: Andere vordefinierte Attribute ("tsatyd. h")
description: Die folgenden Werte identifizieren verschiedene Attribute, die mit der ITF Context getappproperty-Methode abgerufen werden. Das Datenformat und der Inhalt der einzelnen Eigenschaftentypen sind eingeschlossen.
ms.assetid: 8536938b-98a1-415b-b5f2-45b90215c270
keywords:
- Andere vordefinierte Attribute Text Dienst-Framework
topic_type:
- apiref
api_name:
- Other Predefined Attributes
api_location:
- TsAttrid.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0d0a3ff72a5ea84a6b9e5b47106012a945dbf45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339360"
---
# <a name="other-predefined-attributes"></a><span data-ttu-id="8b09b-105">Andere vordefinierte Attribute</span><span class="sxs-lookup"><span data-stu-id="8b09b-105">Other Predefined Attributes</span></span>

<span data-ttu-id="8b09b-106">Die folgenden Werte identifizieren verschiedene Attribute, die mit der [ITF context:: getappproperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) -Methode abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="8b09b-106">The following values identify miscellaneous attributes obtained with the [ITfContext::GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) method.</span></span> <span data-ttu-id="8b09b-107">Das Datenformat und der Inhalt der einzelnen Eigenschaftentypen sind eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="8b09b-107">The data format and contents of each property type are included.</span></span>

## <a name="properties"></a><span data-ttu-id="8b09b-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8b09b-108">Properties</span></span>



| <span data-ttu-id="8b09b-109">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8b09b-109">Property</span></span>                             | <span data-ttu-id="8b09b-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8b09b-110">Description</span></span>                                                                       |
|--------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="8b09b-111">**Anwendung "Tsat" \_**</span><span class="sxs-lookup"><span data-stu-id="8b09b-111">**TSATTRID\_App**</span></span>                    | <span data-ttu-id="8b09b-112">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="8b09b-112">Not used.</span></span>                                                                         |
| <span data-ttu-id="8b09b-113">**Die Anwendung "der Anwendung" ist \_ \_ inkorretgrammar.**</span><span class="sxs-lookup"><span data-stu-id="8b09b-113">**TSATTRID\_App\_IncorrectGrammar**</span></span>  | <span data-ttu-id="8b09b-114">Enthält einen Wert ungleich 0 (null), wenn der Text einen Grammatikfehler oder andernfalls 0 (null) enthält.</span><span class="sxs-lookup"><span data-stu-id="8b09b-114">Contains a nonzero value if the text contains a grammar error or zero otherwise.</span></span>  |
| <span data-ttu-id="8b09b-115">**Anwendungs Rechtschreibprüfung \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8b09b-115">**TSATTRID\_App\_IncorrectSpelling**</span></span> | <span data-ttu-id="8b09b-116">Enthält einen Wert ungleich 0 (null), wenn der Text einen Rechtschreibfehler oder andernfalls 0 (null) enthält.</span><span class="sxs-lookup"><span data-stu-id="8b09b-116">Contains a nonzero value if the text contains a spelling error or zero otherwise.</span></span> |
| <span data-ttu-id="8b09b-117">**\_andere Benutzer**</span><span class="sxs-lookup"><span data-stu-id="8b09b-117">**TSATTRID\_OTHERS**</span></span>                 | <span data-ttu-id="8b09b-118">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="8b09b-118">Not used.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="8b09b-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b09b-119">Requirements</span></span>



| <span data-ttu-id="8b09b-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b09b-120">Requirement</span></span> | <span data-ttu-id="8b09b-121">Wert</span><span class="sxs-lookup"><span data-stu-id="8b09b-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8b09b-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8b09b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8b09b-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b09b-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="8b09b-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8b09b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8b09b-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b09b-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8b09b-126">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="8b09b-126">Redistributable</span></span><br/>          | <span data-ttu-id="8b09b-127">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8b09b-127">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                       |
| <span data-ttu-id="8b09b-128">Header</span><span class="sxs-lookup"><span data-stu-id="8b09b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b09b-129"><dt>"Tsatphd. h"</dt></span><span class="sxs-lookup"><span data-stu-id="8b09b-129"><dt>TsAttrid.h</dt></span></span> </dl> |



 

