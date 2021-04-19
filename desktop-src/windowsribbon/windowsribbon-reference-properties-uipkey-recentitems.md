---
title: UI_PKEY_RecentItems
description: Gibt die Eigenschaft "Eigenschaft für Benutzeroberflächen- \_ pkey" an \_ .
ms.assetid: 54e7ad1f-86b3-45e0-a0f4-5ee0d08e9d4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a07410d3152fb49b55460ec15c6914c53f3b6850
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341943"
---
# <a name="ui_pkey_recentitems"></a><span data-ttu-id="35388-103">Benutzeroberflächen- \_ pkey- \_ entitems</span><span class="sxs-lookup"><span data-stu-id="35388-103">UI\_PKEY\_RecentItems</span></span>

<span data-ttu-id="35388-104">Gibt die Eigenschaft "Eigenschaft für Benutzeroberflächen- \_ pkey" an \_ .</span><span class="sxs-lookup"><span data-stu-id="35388-104">Identifies the UI\_PKEY\_RecentItems property.</span></span>

```
propertyDescription
   name = UI_PKEY_RecentItems
   shellPKey = UI_PKEY_RecentItems
   formatID = 00000350-7363-696e-8441798acf5aebb7
   propID = 350
   typeInfo
      type = VT_ARRAY | VT_UNKNOWN
```

## <a name="remarks"></a><span data-ttu-id="35388-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="35388-105">Remarks</span></span>

<span data-ttu-id="35388-106">[Benutzeroberfläche \_ Pkey \_ fixiert](windowsribbon-reference-properties-uipkey-pinned.md) wird von einer Anwendung verwendet, um das Array von Elementen in der zuletzt verwendeten (MRU) Items-Auflistung des [Anwendungs Menüs](windowsribbon-controls-applicationmenu.md)abzufragen.</span><span class="sxs-lookup"><span data-stu-id="35388-106">[UI\_PKEY\_Pinned](windowsribbon-reference-properties-uipkey-pinned.md) is used by an application to query the array of items in the most recently used (MRU) items collection of the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span> <span data-ttu-id="35388-107">Die Informationen für die einzelnen MRU-Elemente werden in einem [**iuisimplepropertyset**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) -Objekt gekapselt und enthalten die folgenden drei Eigenschafts Schlüssel:</span><span class="sxs-lookup"><span data-stu-id="35388-107">The information for each MRU item is encapsulated in an [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) object and includes the following three property keys:</span></span>

-   [<span data-ttu-id="35388-108">UI- \_ pkey- \_ Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="35388-108">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)
-   [<span data-ttu-id="35388-109">UI \_ pkey \_ labeldescription</span><span class="sxs-lookup"><span data-stu-id="35388-109">UI\_PKEY\_LabelDescription</span></span>](windowsribbon-reference-properties-uipkey-labeldescription.md)
-   [<span data-ttu-id="35388-110">UI- \_ pkey \_ fixiert</span><span class="sxs-lookup"><span data-stu-id="35388-110">UI\_PKEY\_Pinned</span></span>](windowsribbon-reference-properties-uipkey-pinned.md)

<span data-ttu-id="35388-111">Die Liste der MRU-Elemente wird als **SAFEARRAY** der [**iuisimplepropertyset**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) -Zeiger auf die entsprechenden Implementierungen in der Host Anwendung an die Menüband-Host Anwendung übergeben.</span><span class="sxs-lookup"><span data-stu-id="35388-111">The list of MRU items is passed to the Ribbon host application as a **SAFEARRAY** of [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) pointers to respective implementations in the host application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="35388-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="35388-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35388-113">Zustands Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="35388-113">State Properties</span></span>](windowsribbon-reference-properties-state.md)
</dt> </dl>

 

 