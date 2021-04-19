---
title: Temporäres Attribut
description: Das temporäre Attribut gibt an, ob eine Wiedergabeliste temporär ist.
ms.assetid: 0d967a70-97d1-4918-8068-fe2868ab41d2
keywords:
- Temporäres Attribut Fenster Media Player
topic_type:
- apiref
api_name:
- Temporary
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a70ae8f3ae06ae44077cce3d8fa3fdf67dc853eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354056"
---
# <a name="temporary-attribute"></a><span data-ttu-id="ee4c8-104">Temporäres Attribut</span><span class="sxs-lookup"><span data-stu-id="ee4c8-104">Temporary Attribute</span></span>

<span data-ttu-id="ee4c8-105">Das **temporäre** Attribut gibt an, ob eine Wiedergabeliste temporär ist.</span><span class="sxs-lookup"><span data-stu-id="ee4c8-105">The **Temporary** attribute specifies whether a playlist is temporary.</span></span>

<span data-ttu-id="ee4c8-106">**Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="ee4c8-106">**Remarks**</span></span>

<span data-ttu-id="ee4c8-107">Wenn Sie eine Wiedergabeliste aus der Bibliothek abgerufen haben, werden die Änderungen, die Sie an der Wiedergabeliste vornehmen, in der Bibliothek des Benutzers widergespiegelt.</span><span class="sxs-lookup"><span data-stu-id="ee4c8-107">If you retrieved a playlist from the library, changes you make to the playlist will be reflected in the user's library.</span></span> <span data-ttu-id="ee4c8-108">Um dies zu vermeiden, nennen Sie [iwmpwiedergabe:: Set Items MINFO](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-setiteminfo) , und übergeben Sie den Attributnamen "temporär" und den Wert "true".</span><span class="sxs-lookup"><span data-stu-id="ee4c8-108">To avoid this, call [IWMPPlaylist::setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-setiteminfo) passing the attribute name "Temporary" and the value "true".</span></span> <span data-ttu-id="ee4c8-109">Dadurch wird die Wiedergabelisten Instanz in eine temporäre Wiedergabeliste konvertiert, die ohne Änderung der ursprünglichen Wiedergabeliste sicher bearbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ee4c8-109">This converts your playlist instance to a temporary playlist, which is safe to edit without changing the original playlist.</span></span>

<span data-ttu-id="ee4c8-110">**Gilt für**</span><span class="sxs-lookup"><span data-stu-id="ee4c8-110">**Applies To**</span></span>

-   [<span data-ttu-id="ee4c8-111">Wiedergabelisten</span><span class="sxs-lookup"><span data-stu-id="ee4c8-111">Playlists</span></span>](playlist-attributes-ref.md)

## <a name="requirements"></a><span data-ttu-id="ee4c8-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ee4c8-112">Requirements</span></span>



| <span data-ttu-id="ee4c8-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ee4c8-113">Requirement</span></span> | <span data-ttu-id="ee4c8-114">Wert</span><span class="sxs-lookup"><span data-stu-id="ee4c8-114">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="ee4c8-115">Version</span><span class="sxs-lookup"><span data-stu-id="ee4c8-115">Version</span></span><br/> | <span data-ttu-id="ee4c8-116">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="ee4c8-116">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ee4c8-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee4c8-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee4c8-118">**Attribut Verweis**</span><span class="sxs-lookup"><span data-stu-id="ee4c8-118">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





