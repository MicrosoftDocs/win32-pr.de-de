---
description: Gibt ein Fenster an, in dem die Medien-Engine den OPM-Schutz (Output Protection Manager) anwenden soll.
ms.assetid: E5271D72-FE16-4D28-9BBA-1440C7CE0921
title: MF_MEDIA_ENGINE_OPM_HWND-Attribut (MF mediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d60dd38f4f9eaca3e4eefbf84142c1509463f9b9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961129"
---
# <a name="mf_media_engine_opm_hwnd-attribute"></a><span data-ttu-id="88418-103">\_ \_ \_ OPM- \_ HWND-Attribut der MF-Medien-Engine</span><span class="sxs-lookup"><span data-stu-id="88418-103">MF\_MEDIA\_ENGINE\_OPM\_HWND attribute</span></span>

<span data-ttu-id="88418-104">Gibt ein Fenster an, in dem die Medien-Engine den OPM-Schutz ( [Output Protection Manager](output-protection-manager.md) ) anwenden soll.</span><span class="sxs-lookup"><span data-stu-id="88418-104">Specifies a window for the Media Engine to apply [Output Protection Manager](output-protection-manager.md) (OPM) protections.</span></span>

## <a name="data-type"></a><span data-ttu-id="88418-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="88418-105">Data type</span></span>

<span data-ttu-id="88418-106">**HWND** als **UINT64** gespeichert</span><span class="sxs-lookup"><span data-stu-id="88418-106">**HWND** stored as **UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="88418-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="88418-107">Remarks</span></span>

<span data-ttu-id="88418-108">Dieses Attribut wird mit der [**imfmediaengineclassfactory:: forateinstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) -Methode verwendet, um die Medien-Engine zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="88418-108">This attribute is used with the [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) method to initialize the Media Engine.</span></span>

<span data-ttu-id="88418-109">Um den OPM-Schutz für die Videowiedergabe zu aktivieren, muss die Anwendung einen der folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="88418-109">To enable OPM protections for video playback, the application must do one of the following:</span></span>

-   <span data-ttu-id="88418-110">Legen Sie [das \_ \_ \_ \_ HWND](mf-media-engine-playback-hwnd.md) -Attribut der MF-Medien-Engine beim Erstellen der Medien-Engine fest.</span><span class="sxs-lookup"><span data-stu-id="88418-110">Set the [MF\_MEDIA\_ENGINE\_PLAYBACK\_HWND](mf-media-engine-playback-hwnd.md) attribute when creating the Media Engine.</span></span>
-   <span data-ttu-id="88418-111">Legen Sie \_ \_ \_ \_ beim Erstellen der Medien-Engine das OPM-HWND-Attribut der MF-Medien-Engine fest</span><span class="sxs-lookup"><span data-stu-id="88418-111">Set the MF\_MEDIA\_ENGINE\_OPM\_HWND attribute when creating the Media Engine.</span></span>
-   <span data-ttu-id="88418-112">Nach dem Erstellen der Medien-Engine, aber vor dem Anzeigen geschützter Inhalte, muss [**imfmediaengineprotectedcontent::**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setopmwindow) Setup-Window aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="88418-112">Call [**IMFMediaEngineProtectedContent::SetOPMWindow**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setopmwindow) at any point after creating the Media Engine, but before protected content is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="88418-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88418-113">Requirements</span></span>



| <span data-ttu-id="88418-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="88418-114">Requirement</span></span> | <span data-ttu-id="88418-115">Wert</span><span class="sxs-lookup"><span data-stu-id="88418-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="88418-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="88418-116">Minimum supported client</span></span><br/> | <span data-ttu-id="88418-117">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="88418-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="88418-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="88418-118">Minimum supported server</span></span><br/> | <span data-ttu-id="88418-119">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="88418-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="88418-120">Header</span><span class="sxs-lookup"><span data-stu-id="88418-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="88418-121"><dt>MF mediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="88418-121"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88418-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88418-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88418-123">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="88418-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="88418-124">Medien-Engine-Attribute</span><span class="sxs-lookup"><span data-stu-id="88418-124">Media Engine Attributes</span></span>](media-engine-attributes.md)
</dt> </dl>

 

 




