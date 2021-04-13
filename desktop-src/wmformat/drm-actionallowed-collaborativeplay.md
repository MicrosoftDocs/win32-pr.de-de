---
title: DRM_ActionAllowed_CollaborativePlay
description: Das DRM- \_ Aktions zugelassene \_ kollaborativeplay-Attribut gibt an, ob die Lizenz den Inhalt gemeinsam spielen kann.
ms.assetid: 111e8fa7-ef5a-483a-b930-8a8e5b4d120a
keywords:
- DRM_ActionAllowed_CollaborativePlay Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CollaborativePlay
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0268c9c3d70a8f51db390544bf854e5acd5b9e88
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389914"
---
# <a name="drm_actionallowed_collaborativeplay"></a><span data-ttu-id="d65e4-104">DRM- \_ Aktions zugelassene \_ kollaborativeplay</span><span class="sxs-lookup"><span data-stu-id="d65e4-104">DRM\_ActionAllowed\_CollaborativePlay</span></span>

<span data-ttu-id="d65e4-105">Das **DRM- \_ Aktions zugelassene \_ kollaborativeplay** -Attribut gibt an, ob die Lizenz den Inhalt gemeinsam spielen kann.</span><span class="sxs-lookup"><span data-stu-id="d65e4-105">The **DRM\_ActionAllowed\_CollaborativePlay** attribute indicates whether the license allows the content to be played collaboratively.</span></span>

## <a name="global-constant"></a><span data-ttu-id="d65e4-106">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="d65e4-106">Global Constant</span></span>

<span data-ttu-id="d65e4-107">g \_ wszwmdrm- \_ Aktions zulässige \_ kollaborative Zusammenspiel</span><span class="sxs-lookup"><span data-stu-id="d65e4-107">g\_wszWMDRM\_ActionAllowed\_CollaborativePlay</span></span>

## <a name="data-type"></a><span data-ttu-id="d65e4-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="d65e4-108">Data Type</span></span>

<span data-ttu-id="d65e4-109">**WMT- \_ Typ \_ bool**</span><span class="sxs-lookup"><span data-stu-id="d65e4-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="d65e4-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d65e4-110">Remarks</span></span>

<span data-ttu-id="d65e4-111">Die gemeinsame Wiedergabe Berechtigung gilt für die Wiedergabe geschützter Inhalte als Teil einer kollaborativen Sitzung mithilfe von Peer-to-Peer-Diensten.</span><span class="sxs-lookup"><span data-stu-id="d65e4-111">The collaborative play right applies to playing protected content as part of a collaborative session using peer-to-peer services.</span></span> <span data-ttu-id="d65e4-112">Beispielsweise können Benutzer von MSN Messenger 2004 geschützte Inhalte in einer MusicMix-Sitzung wiedergeben.</span><span class="sxs-lookup"><span data-stu-id="d65e4-112">For example, users of MSN Messenger 2004 can play protected content in a MusicMix session.</span></span> <span data-ttu-id="d65e4-113">Dieses Recht kann nur verwendet werden, um eine geschützte Datei gleichzeitig zu einer einzelnen Sitzung beizutragen, und alle Benutzer, die an der Sitzung teilnehmen, müssen online sein, damit der Inhalt wieder hergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="d65e4-113">This right can only be used to contribute a protected file to a single session at one time, and all users participating in the session must be online to render the content.</span></span>

<span data-ttu-id="d65e4-114">Dies ist eine schreibgeschützte Eigenschaft, die mithilfe von [**iwmdrmreader:: getdrmproperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty)abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d65e4-114">This is a read-only property that is retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

## <a name="see-also"></a><span data-ttu-id="d65e4-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d65e4-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d65e4-116">**DRM-Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="d65e4-116">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




