---
title: Wiedergabeliste. AttributeCount
description: Die AttributeCount-Eigenschaft ruft die Anzahl der Attribute ab, die der Wiedergabeliste zugeordnet sind.
ms.assetid: 92063131-0118-4458-9122-0539628a9821
keywords:
- Wiedergabeliste. AttributeCount Windows Media Player
topic_type:
- apiref
api_name:
- Playlist.attributeCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e42d72e029f232bb6dabc074b412406a1bb64c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368594"
---
# <a name="playlistattributecount"></a><span data-ttu-id="ea79e-104">Wiedergabeliste. AttributeCount</span><span class="sxs-lookup"><span data-stu-id="ea79e-104">Playlist.attributeCount</span></span>

<span data-ttu-id="ea79e-105">Die **AttributeCount** -Eigenschaft ruft die Anzahl der Attribute ab, die der Wiedergabeliste zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ea79e-105">The **attributeCount** property retrieves the number of attributes associated with the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea79e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea79e-106">Syntax</span></span>

<span data-ttu-id="ea79e-107">*Player*. *currentwiedergabe*. **AttributeCount**</span><span class="sxs-lookup"><span data-stu-id="ea79e-107">*player*.*currentPlaylist*.**attributeCount**</span></span>

## <a name="possible-values"></a><span data-ttu-id="ea79e-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="ea79e-108">Possible Values</span></span>

<span data-ttu-id="ea79e-109">Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="ea79e-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="ea79e-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ea79e-110">Remarks</span></span>

<span data-ttu-id="ea79e-111">Da Wiedergabelisten aus vielen verschiedenen Quellen stammen können, können Sie mehrere verschiedene Gruppen von Eigenschaften haben.</span><span class="sxs-lookup"><span data-stu-id="ea79e-111">Because playlists can come from many different sources, they can have several different sets of properties.</span></span> <span data-ttu-id="ea79e-112">Diese Methode ruft die Gesamtzahl der verfügbaren Eigenschaften ab, sodass die anderen Methoden des **Wiedergabe** Listen Objekts darauf zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="ea79e-112">This method retrieves the total number of properties available so that the other methods of the **Playlist** object can access them.</span></span>

<span data-ttu-id="ea79e-113">Zum Abrufen des Werts dieser Eigenschaft ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ea79e-113">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="ea79e-114">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="ea79e-114">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="ea79e-115">Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Referenz](attribute-reference.md)zu Windows Media Player-Attributen.</span><span class="sxs-lookup"><span data-stu-id="ea79e-115">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ea79e-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ea79e-116">Examples</span></span>

<span data-ttu-id="ea79e-117">Im folgenden JScript-Beispiel wird veranschaulicht, wie verschiedene Eigenschaften und Methoden der **Wiedergabeliste** und der **Medien** Objekte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ea79e-117">The following JScript example illustrates how various properties and methods of the **Playlist** and **Media** objects are used.</span></span>


```JScript
function onLoad() {
    var display;
    var pl = player.currentPlaylist;

    pl.setItemInfo("custom playlist attribute", "changed");
    pl.item(0).setItemInfo("new custom attribute", "5");

    display = pl.attributeCount + " Playlist Attributes:\r\r";

    for (var i = 0; i < pl.attributeCount; ++i) {
        display = display + pl.attributeName(i) + ": ";
        display = display + pl.getItemInfo(pl.attributeName(i)) + "\r";
    }

    for (var j = 0; j < pl.count; ++j) {
        display = display + "\rTrack " + j + "\r"
        display = display + pl.item(j).attributeCount + " Attributes:\r\r";

        for (var k = 0; k < pl.item(j).attributeCount; ++k) {
            var it = pl.item(j);  // Media object
            display = display + it.getAttributeName(k) + ": ";
            display = display + it.getItemInfo(it.getAttributeName(k)) + "\r";
        }
    }

    myText.value = display;
}

```



## <a name="requirements"></a><span data-ttu-id="ea79e-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ea79e-118">Requirements</span></span>



| <span data-ttu-id="ea79e-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ea79e-119">Requirement</span></span> | <span data-ttu-id="ea79e-120">Wert</span><span class="sxs-lookup"><span data-stu-id="ea79e-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ea79e-121">Version</span><span class="sxs-lookup"><span data-stu-id="ea79e-121">Version</span></span><br/> | <span data-ttu-id="ea79e-122">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="ea79e-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="ea79e-123">DLL</span><span class="sxs-lookup"><span data-stu-id="ea79e-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="ea79e-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea79e-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea79e-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea79e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea79e-126">**Wiedergabelisten Objekt**</span><span class="sxs-lookup"><span data-stu-id="ea79e-126">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="ea79e-127">**Wiedergabeliste. AttributeName**</span><span class="sxs-lookup"><span data-stu-id="ea79e-127">**Playlist.attributeName**</span></span>](playlist-attributename.md)
</dt> <dt>

[<span data-ttu-id="ea79e-128">**Wiedergabeliste. getiteminfo**</span><span class="sxs-lookup"><span data-stu-id="ea79e-128">**Playlist.getItemInfo**</span></span>](playlist-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="ea79e-129">**Wiedergabeliste. Einstellungs Element**</span><span class="sxs-lookup"><span data-stu-id="ea79e-129">**Playlist.setItemInfo**</span></span>](playlist-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="ea79e-130">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="ea79e-130">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="ea79e-131">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="ea79e-131">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





