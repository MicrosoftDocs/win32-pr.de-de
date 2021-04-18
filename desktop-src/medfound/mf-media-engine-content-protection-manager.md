---
description: Ermöglicht der Medien-Engine, geschützte Inhalte wiederzugeben.
ms.assetid: F6F17EC7-6553-4127-B691-C20C945DD4D8
title: MF_MEDIA_ENGINE_CONTENT_PROTECTION_MANAGER-Attribut (MF mediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afb99d1df36c9b9adbf1c099d619df60e1144b87
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106361120"
---
# <a name="mf_media_engine_content_protection_manager-attribute"></a><span data-ttu-id="ba387-103">MF \_ Media \_ Engine \_ Content \_ Protection \_ Manager-Attribut</span><span class="sxs-lookup"><span data-stu-id="ba387-103">MF\_MEDIA\_ENGINE\_CONTENT\_PROTECTION\_MANAGER attribute</span></span>

<span data-ttu-id="ba387-104">Ermöglicht der Medien-Engine, geschützte Inhalte wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="ba387-104">Enables the Media Engine to play protected content.</span></span>

## <a name="data-type"></a><span data-ttu-id="ba387-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="ba387-105">Data type</span></span>

<span data-ttu-id="ba387-106">**IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="ba387-106">**IUnknown\***</span></span>

## <a name="remarks"></a><span data-ttu-id="ba387-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ba387-107">Remarks</span></span>

<span data-ttu-id="ba387-108">Der Wert dieses Attributs ist ein Zeiger auf die [**imfcontentschutzmanager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ba387-108">The value of this attribute is a pointer to the [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) interface.</span></span> <span data-ttu-id="ba387-109">Der Aufrufer muss die-Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="ba387-109">The caller must implement the interface.</span></span>

<span data-ttu-id="ba387-110">Dieses Attribut kann eines der Attribute sein, die an [**imfmediaengineclassfactory:: kreateinstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="ba387-110">This attribute can be one of the attributes passed to [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance).</span></span> <span data-ttu-id="ba387-111">Dies ist erforderlich, wenn geschützter Inhalt wiedergegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="ba387-111">It is required if protected content is to be played.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba387-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ba387-112">Requirements</span></span>



| <span data-ttu-id="ba387-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ba387-113">Requirement</span></span> | <span data-ttu-id="ba387-114">Wert</span><span class="sxs-lookup"><span data-stu-id="ba387-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba387-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ba387-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ba387-116">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="ba387-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="ba387-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ba387-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ba387-118">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="ba387-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="ba387-119">Header</span><span class="sxs-lookup"><span data-stu-id="ba387-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba387-120"><dt>MF mediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba387-120"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba387-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba387-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba387-122">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="ba387-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ba387-123">**IMF mediaengineclassfactory:: "forateinstance"**</span><span class="sxs-lookup"><span data-stu-id="ba387-123">**IMFMediaEngineClassFactory::CreateInstance**</span></span>](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




