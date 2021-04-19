---
description: Gibt eine Kontext Zeichenfolge an, die von CDM-Implementierungen (Content entschlüsseln Module) verwendet wird, die mediaschutzpmpserver verwenden.
title: MF_CONTENTDECRYPTIONMODULE_PMPSTORECONTEXT (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: 49e12aeba9cce988c58fca94c33e7b4179530a56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356603"
---
# <a name="mf_contentdecryptionmodule_pmpstorecontext-property"></a><span data-ttu-id="897c6-103">Eigenschaft "MF \_ contentdecryptionmodule \_ pmpstorecontext"</span><span class="sxs-lookup"><span data-stu-id="897c6-103">MF\_CONTENTDECRYPTIONMODULE\_PMPSTORECONTEXT property</span></span>

<span data-ttu-id="897c6-104">Gibt eine Kontext Zeichenfolge an, die von CDM-Implementierungen (Content entschlüsseln Module) verwendet wird, die [mediaschutzpmpserver](/uwp/api/windows.media.protection.mediaprotectionpmpserver)verwenden.</span><span class="sxs-lookup"><span data-stu-id="897c6-104">Specifies a context string used by Content Decryption Module (CDM) implementations that use [MediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver).</span></span>


## <a name="data-type"></a><span data-ttu-id="897c6-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="897c6-105">Data type</span></span>

<span data-ttu-id="897c6-106">**LPWSTR** (VT_LPWSTR)</span><span class="sxs-lookup"><span data-stu-id="897c6-106">**LPWSTR** (VT_LPWSTR)</span></span>

## <a name="property-guid"></a><span data-ttu-id="897c6-107">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="897c6-107">Property GUID</span></span>

<span data-ttu-id="897c6-108">**MF \_ contentdecryptionmodule \_ pmpstorecontext**</span><span class="sxs-lookup"><span data-stu-id="897c6-108">**MF\_CONTENTDECRYPTIONMODULE\_PMPSTORECONTEXT**</span></span>

## <a name="property-value"></a><span data-ttu-id="897c6-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="897c6-109">Property value</span></span>

<span data-ttu-id="897c6-110">Eine Kontext Zeichenfolge, die von CDM-Implementierungen (Content entschlüsseln Module) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="897c6-110">A  a context string used by Content Decryption Module (CDM) implementations.</span></span>

## <a name="remarks"></a><span data-ttu-id="897c6-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="897c6-111">Remarks</span></span>

<span data-ttu-id="897c6-112">Der CDM-Implementierer sollte nach diesem Wert suchen und den Wert mit dem Eigenschaftsnamen "Windows. Media. Protection. pmpstorecontext" an den [mediaschutzpmpserver-Konstruktor](/uwp/api/windows.media.protection.mediaprotectionpmpserver.-ctor) übergeben.</span><span class="sxs-lookup"><span data-stu-id="897c6-112">The CDM implementer should look for this value and pass the value to the [MediaProtectionPMPServer constructor](/uwp/api/windows.media.protection.mediaprotectionpmpserver.-ctor) using the property name "Windows.Media.Protection.PMPStoreContext".</span></span>


<span data-ttu-id="897c6-113">Apps sollten diese Eigenschaft nicht erstellen, wenn Sie [imfcontentdecryptionmoduleaccess:: createcontentdecryptionmodule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="897c6-113">Apps should not create this property when calling [IMFContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).</span></span>

## <a name="requirements"></a><span data-ttu-id="897c6-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="897c6-114">Requirements</span></span>



| <span data-ttu-id="897c6-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="897c6-115">Requirement</span></span> | <span data-ttu-id="897c6-116">Wert</span><span class="sxs-lookup"><span data-stu-id="897c6-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="897c6-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="897c6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="897c6-118">Windows 10 April 2020-Update</span><span class="sxs-lookup"><span data-stu-id="897c6-118">Windows 10 April 2020 Update</span></span><br/>                                     |
| <span data-ttu-id="897c6-119">Header</span><span class="sxs-lookup"><span data-stu-id="897c6-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="897c6-120"><dt>MF contentdecryptionmodule. h</dt></span><span class="sxs-lookup"><span data-stu-id="897c6-120"><dt>mfcontentdecryptionmodule.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="897c6-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="897c6-121">See also</span></span>

- [<span data-ttu-id="897c6-122">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="897c6-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
- [<span data-ttu-id="897c6-123">Mediaschutzpmpserver</span><span class="sxs-lookup"><span data-stu-id="897c6-123">MediaProtectionPMPServer</span></span>](/uwp/api/windows.media.protection.mediaprotectionpmpserver)


 

 




