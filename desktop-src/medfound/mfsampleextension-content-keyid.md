---
description: Legt die Schlüssel-ID für das Beispiel fest.
ms.assetid: 75339350-05AA-486E-9C28-11070C0DA61D
title: MFSampleExtension_Content_KeyID-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b40d698dbb2d64e9744027b3cd8a3bb2dceec226
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368232"
---
# <a name="mfsampleextension_content_keyid-attribute"></a><span data-ttu-id="5737d-103">MF Sample Extension- \_ Content \_ keyid-Attribut</span><span class="sxs-lookup"><span data-stu-id="5737d-103">MFSampleExtension\_Content\_KeyID attribute</span></span>

<span data-ttu-id="5737d-104">Legt die Schlüssel-ID für das Beispiel fest.</span><span class="sxs-lookup"><span data-stu-id="5737d-104">Sets the Key ID for the sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="5737d-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5737d-105">Data type</span></span>

<span data-ttu-id="5737d-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="5737d-106">**GUID**</span></span>

## <a name="examples"></a><span data-ttu-id="5737d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5737d-107">Examples</span></span>

<span data-ttu-id="5737d-108">Im folgenden Beispiel wird gezeigt, wie die Schlüssel-ID für das Beispiel festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="5737d-108">The following example shows how to set the Key ID for the sample.</span></span>


```C++
// m_spSample is a IMFSample
// guidKID is a GUID

m_spSample->SetGUID( MFSampleExtension_Content_KeyID, guidKID );
```



## <a name="requirements"></a><span data-ttu-id="5737d-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5737d-109">Requirements</span></span>



| <span data-ttu-id="5737d-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5737d-110">Requirement</span></span> | <span data-ttu-id="5737d-111">Wert</span><span class="sxs-lookup"><span data-stu-id="5737d-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5737d-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5737d-112">Minimum supported client</span></span><br/> | <span data-ttu-id="5737d-113">Windows 8.1 \[ Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="5737d-113">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="5737d-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5737d-114">Minimum supported server</span></span><br/> | <span data-ttu-id="5737d-115">Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="5737d-115">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="5737d-116">Header</span><span class="sxs-lookup"><span data-stu-id="5737d-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="5737d-117"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5737d-117"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5737d-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5737d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5737d-119">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="5737d-119">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5737d-120">**IMF Sample**</span><span class="sxs-lookup"><span data-stu-id="5737d-120">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[<span data-ttu-id="5737d-121">MF SampleExtension \_ Encryption \_ subsamplemappingsplit</span><span class="sxs-lookup"><span data-stu-id="5737d-121">MFSampleExtension\_Encryption\_SubSampleMappingSplit</span></span>](mfsampleextension-encryption-subsamplemappingsplit.md)
</dt> </dl>

 

 




