---
title: WSMAN. Error-Eigenschaft (WSManDisp. h)
description: Ruft zusätzliche Fehlerinformationen, die sich in einem XML-Stream befinden, für den vorhergehenden Aufrufe einer WSMAN-Methode ab, wenn Windows-Remoteverwaltung Dienst kein Sitzungs Objekt, kein ConnectionOptions-Objekt oder ResourceLocator-Objekt erstellen konnte.
ms.assetid: 72d05ef9-672c-4693-b7c9-6d689858acd4
ms.tgt_platform: multiple
keywords:
- Fehler Eigenschaft Windows-Remoteverwaltung
- Error-Eigenschaft Windows-Remoteverwaltung, WSMAN-Objekt
- WSMAN-Objekt Windows-Remoteverwaltung, Fehler Eigenschaft
topic_type:
- apiref
api_name:
- WSMan.Error
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f9e7ffd42d67807f2f7b6096a89ed91e3d95af8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103803"
---
# <a name="wsmanerror-property"></a><span data-ttu-id="35deb-106">WSMAN. Error (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="35deb-106">WSMan.Error property</span></span>

<span data-ttu-id="35deb-107">Ruft zusätzliche Fehlerinformationen, die sich in einem XML-Stream befinden, für den vorhergehenden Aufrufe einer [**WSMAN**](wsman.md) -Methode ab, wenn Windows-Remoteverwaltung Dienst kein [**Sitzungs**](session.md) Objekt, kein [**ConnectionOptions**](connectionoptions.md) -Objekt oder [**ResourceLocator**](resourcelocator.md) -Objekt erstellen konnte.</span><span class="sxs-lookup"><span data-stu-id="35deb-107">Gets additional error information, in an XML stream, for the preceding call to a [**WSMan**](wsman.md) method if Windows Remote Management service was unable to create a [**Session**](session.md) object, a [**ConnectionOptions**](connectionoptions.md) object, or a [**ResourceLocator**](resourcelocator.md) object.</span></span>

<span data-ttu-id="35deb-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="35deb-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="35deb-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="35deb-109">Syntax</span></span>


```VB
WSMan.Error As BSTR
```



## <a name="property-value"></a><span data-ttu-id="35deb-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="35deb-110">Property value</span></span>

<span data-ttu-id="35deb-111">Die XML-Darstellung der Fehlerinformationen.</span><span class="sxs-lookup"><span data-stu-id="35deb-111">The XML representation of the error information.</span></span>

## <a name="requirements"></a><span data-ttu-id="35deb-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="35deb-112">Requirements</span></span>



| <span data-ttu-id="35deb-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="35deb-113">Requirement</span></span> | <span data-ttu-id="35deb-114">Wert</span><span class="sxs-lookup"><span data-stu-id="35deb-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="35deb-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="35deb-115">Minimum supported client</span></span><br/> | <span data-ttu-id="35deb-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="35deb-116">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="35deb-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="35deb-117">Minimum supported server</span></span><br/> | <span data-ttu-id="35deb-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="35deb-118">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="35deb-119">Header</span><span class="sxs-lookup"><span data-stu-id="35deb-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="35deb-120"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="35deb-120"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="35deb-121">IDL</span><span class="sxs-lookup"><span data-stu-id="35deb-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="35deb-122"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="35deb-122"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="35deb-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="35deb-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="35deb-124"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="35deb-124"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="35deb-125">DLL</span><span class="sxs-lookup"><span data-stu-id="35deb-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35deb-126"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35deb-126"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="35deb-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="35deb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35deb-128">**WSMAN**</span><span class="sxs-lookup"><span data-stu-id="35deb-128">**WSMan**</span></span>](wsman.md)
</dt> </dl>

 

 





