---
description: Gibt einen Dateipfad an, der einen Speicherort darstellt, den das Inhalts Entschlüsselungsmodul (CDM) für die Initialisierung verwenden kann.
title: MF_CONTENTDECRYPTIONMODULE_STOREPATH (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: 8f5ae27fc8ebbdbf0d9e529f1905631b462ff959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485219"
---
# <a name="mf_contentdecryptionmodule_storepath-property"></a><span data-ttu-id="f1a79-103">StorePath-Eigenschaft des MF- \_ contentdecryptionmodule \_</span><span class="sxs-lookup"><span data-stu-id="f1a79-103">MF\_CONTENTDECRYPTIONMODULE\_STOREPATH property</span></span>

<span data-ttu-id="f1a79-104">Gibt einen Dateipfad an, der einen Speicherort darstellt, den das Inhalts Entschlüsselungsmodul (CDM) für die Initialisierung verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="f1a79-104">Specifies a file path representing a storage location the Content Decryption Module (CDM) can use for initialization.</span></span>


## <a name="data-type"></a><span data-ttu-id="f1a79-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="f1a79-105">Data type</span></span>

<span data-ttu-id="f1a79-106">**LPWSTR** (VT_LPWSTR)</span><span class="sxs-lookup"><span data-stu-id="f1a79-106">**LPWSTR** (VT_LPWSTR)</span></span>

## <a name="property-guid"></a><span data-ttu-id="f1a79-107">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="f1a79-107">Property GUID</span></span>

<span data-ttu-id="f1a79-108">**der MF- \_ contentdecryptionmodule \_ StorePath**</span><span class="sxs-lookup"><span data-stu-id="f1a79-108">**MF\_CONTENTDECRYPTIONMODULE\_STOREPATH**</span></span>

## <a name="property-value"></a><span data-ttu-id="f1a79-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f1a79-109">Property value</span></span>

<span data-ttu-id="f1a79-110">Ein Dateipfad, der einen Speicherort darstellt, den das Content entschlüsseln Module (CDM) für die Initialisierung verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="f1a79-110">A file path representing a storage location the Content Decryption Module (CDM) can use for initialization.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1a79-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f1a79-111">Remarks</span></span>

<span data-ttu-id="f1a79-112">Der mit dieser Eigenschaft angegebene Pfad wird auch für inhaltsspezifische Daten verwendet, wenn die [MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH](mf-contentdecryptionmodule-inprivatestorepath.md) -Eigenschaft nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f1a79-112">The path specified with this property will also be used for content-specific data if the [MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH](mf-contentdecryptionmodule-inprivatestorepath.md) property isn't set.</span></span>

<span data-ttu-id="f1a79-113">Um die com-Leistung zu verbessern, sollte die APP den Speicherort nicht löschen, nachdem das CDM-Objekt freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="f1a79-113">To improve COM performance, the app should not delete the store location after the CDM object has been released.</span></span>



<span data-ttu-id="f1a79-114">Legen Sie diese Eigenschaft fest, wenn Sie einen CDM durch Aufrufen von [imfcontentdecryptionmoduleaccess:: createcontentdecryptionmodule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)erstellen.</span><span class="sxs-lookup"><span data-stu-id="f1a79-114">Set this property when you create a CDM by calling [IMFContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).</span></span>

## <a name="requirements"></a><span data-ttu-id="f1a79-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f1a79-115">Requirements</span></span>



| <span data-ttu-id="f1a79-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f1a79-116">Requirement</span></span> | <span data-ttu-id="f1a79-117">Wert</span><span class="sxs-lookup"><span data-stu-id="f1a79-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f1a79-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f1a79-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f1a79-119">Windows 10 April 2020-Update</span><span class="sxs-lookup"><span data-stu-id="f1a79-119">Windows 10 April 2020 Update</span></span><br/>                                     |
| <span data-ttu-id="f1a79-120">Header</span><span class="sxs-lookup"><span data-stu-id="f1a79-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1a79-121"><dt>MF contentdecryptionmodule. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1a79-121"><dt>mfcontentdecryptionmodule.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1a79-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f1a79-122">See also</span></span>

- [<span data-ttu-id="f1a79-123">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f1a79-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
- [<span data-ttu-id="f1a79-124">Imbcontentdecryptionmoduleaccess:: kreatecontentdecryptionmodule</span><span class="sxs-lookup"><span data-stu-id="f1a79-124">IMFContentDecryptionModuleAccess::CreateContentDecryptionModule</span></span>](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)


 

 




