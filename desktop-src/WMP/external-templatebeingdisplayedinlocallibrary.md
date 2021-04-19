---
title: Extern. templatebingdisplayedinlocallibrary
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Extern. templatebingdisplayedinlocallibrary
ms.assetid: a1399c20-804b-4413-be9d-bcf160d75d29
keywords:
- Externe. templatebingdisplayedinlocallibrary-Fenster Media Player
topic_type:
- apiref
api_name:
- External.templateBeingDisplayedInLocalLibrary
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f1d9a93d870882a34014ea2d0d35f29b91f54d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369722"
---
# <a name="externaltemplatebeingdisplayedinlocallibrary"></a><span data-ttu-id="2239d-105">Extern. templatebingdisplayedinlocallibrary</span><span class="sxs-lookup"><span data-stu-id="2239d-105">External.templateBeingDisplayedInLocalLibrary</span></span>

> [!Note]  
> <span data-ttu-id="2239d-106">In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher</span><span class="sxs-lookup"><span data-stu-id="2239d-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="2239d-107">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2239d-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="2239d-108">Die **templatebeingdisplayedinlocallibrary** -Eigenschaft gibt an, ob der von der aktuellen Ermittlungs Seite dargestellte Feed im Strukturansicht-Steuerelement der lokalen Bibliothek angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2239d-108">The **templateBeingDisplayedInLocalLibrary** property indicates whether the feed represented by the current discovery page is being displayed in the local library tree-view control.</span></span>

## <a name="syntax"></a><span data-ttu-id="2239d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="2239d-109">Syntax</span></span>

``` syntax
window.external.templateBeingDisplayedInLocalLibrary
```

## <a name="possible-values"></a><span data-ttu-id="2239d-110">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="2239d-110">Possible Values</span></span>

<span data-ttu-id="2239d-111">Diese Eigenschaft ist ein Schreib geschützter **boolescher** Wert.</span><span class="sxs-lookup"><span data-stu-id="2239d-111">This property is a read-only **Boolean**.</span></span> <span data-ttu-id="2239d-112">**True** gibt an, dass der Feed im Strukturansicht-Steuerelement der lokalen Bibliothek angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2239d-112">**TRUE** indicates that the feed is being displayed in the local library tree-view control.</span></span>

## <a name="remarks"></a><span data-ttu-id="2239d-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2239d-113">Remarks</span></span>

<span data-ttu-id="2239d-114">Eine Ermittlungs Seite, die einen Feed für eine dynamische Wiedergabeliste darstellt, kann eine Schaltfläche anzeigen, mit der der Benutzer den Feed in seiner lokalen Bibliothek speichern kann.</span><span class="sxs-lookup"><span data-stu-id="2239d-114">A discovery page that represents a feed for a dynamic playlist can display a button that allows the user to "save" the feed in his or her local library.</span></span> <span data-ttu-id="2239d-115">Das Speichern des Feeds bedeutet in diesem Kontext, dass einige Metadaten auf dem Computer des Benutzers gespeichert werden, und der Feed wird unter dem Knoten " **Playlists** " im Strukturansicht-Steuerelement der lokalen Bibliothek aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="2239d-115">Saving the feed, in this context, means that some metadata is saved on the user's computer, and the feed is listed under the **Playlists** node in the local library tree-view control.</span></span> <span data-ttu-id="2239d-116">Das Skript auf der Ermittlungs Seite kann die Eigenschaft **templatebeingdisplayedinlocallibrary** überprüfen, um zu bestimmen, ob der Benutzer den Feed bereits in der lokalen Bibliothek gespeichert hat.</span><span class="sxs-lookup"><span data-stu-id="2239d-116">Script on the discovery page can inspect the **templateBeingDisplayedInLocalLibrary** property to determine whether the user has already saved the feed in the local library.</span></span> <span data-ttu-id="2239d-117">Wenn der Benutzer den Feed bereits gespeichert hat, sollte auf der Ermittlungs Seite die Schaltfläche Speichern nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2239d-117">If the user has already saved the feed, the discovery page should not display the save button.</span></span>

<span data-ttu-id="2239d-118">Eine Suchseite, die einen Radio Feed darstellt, sollte die Eigenschaft **templatebeingdisplayedinlocallibrary** aus demselben Grund überprüfen.</span><span class="sxs-lookup"><span data-stu-id="2239d-118">A discovery page that represents a radio feed should inspect the **templateBeingDisplayedInLocalLibrary** property for the same reason.</span></span>

## <a name="requirements"></a><span data-ttu-id="2239d-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2239d-119">Requirements</span></span>



| <span data-ttu-id="2239d-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2239d-120">Requirement</span></span> | <span data-ttu-id="2239d-121">Wert</span><span class="sxs-lookup"><span data-stu-id="2239d-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2239d-122">Version</span><span class="sxs-lookup"><span data-stu-id="2239d-122">Version</span></span><br/> | <span data-ttu-id="2239d-123">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="2239d-123">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="2239d-124">DLL</span><span class="sxs-lookup"><span data-stu-id="2239d-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="2239d-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2239d-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2239d-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2239d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2239d-127">**Externes Objekt für den Typ 1-Online Speicher**</span><span class="sxs-lookup"><span data-stu-id="2239d-127">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





