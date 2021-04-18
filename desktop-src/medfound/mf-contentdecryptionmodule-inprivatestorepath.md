---
description: Gibt einen Dateipfad an, der einen Speicherort darstellt, den das Content entschlüsseln Module (CDM) für inhaltsspezifische Daten verwenden kann.
title: MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: 0d8ce394f4b7a4e952fc9d5928a80cc5500dcdd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526900"
---
# <a name="mf_contentdecryptionmodule_inprivatestorepath-property"></a><span data-ttu-id="1abaf-103">"MF \_ contentdecryptionmodule" \_ inprivatestorepath (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1abaf-103">MF\_CONTENTDECRYPTIONMODULE\_INPRIVATESTOREPATH property</span></span>

<span data-ttu-id="1abaf-104">Gibt einen Dateipfad an, der einen Speicherort darstellt, den das Content entschlüsseln Module (CDM) für inhaltsspezifische Daten verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="1abaf-104">Specifies a file path representing a storage location the Content Decryption Module (CDM) can use for content-specific data.</span></span>


## <a name="data-type"></a><span data-ttu-id="1abaf-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="1abaf-105">Data type</span></span>

<span data-ttu-id="1abaf-106">**LPWSTR** (VT_LPWSTR)</span><span class="sxs-lookup"><span data-stu-id="1abaf-106">**LPWSTR** (VT_LPWSTR)</span></span>

## <a name="property-guid"></a><span data-ttu-id="1abaf-107">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="1abaf-107">Property GUID</span></span>

<span data-ttu-id="1abaf-108">**MF \_ contentdecryptionmodule \_ inprivatestorepath**</span><span class="sxs-lookup"><span data-stu-id="1abaf-108">**MF\_CONTENTDECRYPTIONMODULE\_INPRIVATESTOREPATH**</span></span>

## <a name="property-value"></a><span data-ttu-id="1abaf-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="1abaf-109">Property value</span></span>

<span data-ttu-id="1abaf-110">Ein Dateipfad, der einen Speicherort darstellt, den das Content entschlüsseln Module (CDM) für inhaltsspezifische Daten verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="1abaf-110">A file path representing a storage location the Content Decryption Module (CDM) can use for content-specific data.</span></span>

## <a name="remarks"></a><span data-ttu-id="1abaf-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1abaf-111">Remarks</span></span>

<span data-ttu-id="1abaf-112">Die APP sollte den Speicherort löschen, nachdem das CDM-Objekt freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="1abaf-112">The app should delete the store location after the CDM object has been released.</span></span>

<span data-ttu-id="1abaf-113">Wenn diese Eigenschaft nicht festgelegt ist, verwendet das System den Pfad, der mit der [MF_CONTENTDECRYPTIONMODULE_STOREPATH](mf-contentdecryptionmodule-storepath.md) -Eigenschaft für inhaltsspezifische Daten angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1abaf-113">If this property isn't set, the system will use the path specified with the [MF_CONTENTDECRYPTIONMODULE_STOREPATH](mf-contentdecryptionmodule-storepath.md) property for content-specific data.</span></span>

<span data-ttu-id="1abaf-114">Legen Sie diese Eigenschaft fest, wenn Sie einen CDM durch Aufrufen von [imfcontentdecryptionmoduleaccess:: createcontentdecryptionmodule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)erstellen.</span><span class="sxs-lookup"><span data-stu-id="1abaf-114">Set this property when you create a CDM by calling [IMFContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).</span></span>

## <a name="requirements"></a><span data-ttu-id="1abaf-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1abaf-115">Requirements</span></span>



| <span data-ttu-id="1abaf-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1abaf-116">Requirement</span></span> | <span data-ttu-id="1abaf-117">Wert</span><span class="sxs-lookup"><span data-stu-id="1abaf-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1abaf-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1abaf-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1abaf-119">Windows 10 April 2020-Update</span><span class="sxs-lookup"><span data-stu-id="1abaf-119">Windows 10 April 2020 Update</span></span><br/>                                     |
| <span data-ttu-id="1abaf-120">Header</span><span class="sxs-lookup"><span data-stu-id="1abaf-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1abaf-121"><dt>MF contentdecryptionmodule. h</dt></span><span class="sxs-lookup"><span data-stu-id="1abaf-121"><dt>mfcontentdecryptionmodule.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1abaf-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1abaf-122">See also</span></span>

- [<span data-ttu-id="1abaf-123">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1abaf-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
- [<span data-ttu-id="1abaf-124">Imbcontentdecryptionmoduleaccess:: kreatecontentdecryptionmodule</span><span class="sxs-lookup"><span data-stu-id="1abaf-124">IMFContentDecryptionModuleAccess::CreateContentDecryptionModule</span></span>](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)


 

 




