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
# <a name="ui_pkey_recentitems"></a>Benutzeroberflächen- \_ pkey- \_ entitems

Gibt die Eigenschaft "Eigenschaft für Benutzeroberflächen- \_ pkey" an \_ .

```
propertyDescription
   name = UI_PKEY_RecentItems
   shellPKey = UI_PKEY_RecentItems
   formatID = 00000350-7363-696e-8441798acf5aebb7
   propID = 350
   typeInfo
      type = VT_ARRAY | VT_UNKNOWN
```

## <a name="remarks"></a>Bemerkungen

[Benutzeroberfläche \_ Pkey \_ fixiert](windowsribbon-reference-properties-uipkey-pinned.md) wird von einer Anwendung verwendet, um das Array von Elementen in der zuletzt verwendeten (MRU) Items-Auflistung des [Anwendungs Menüs](windowsribbon-controls-applicationmenu.md)abzufragen. Die Informationen für die einzelnen MRU-Elemente werden in einem [**iuisimplepropertyset**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) -Objekt gekapselt und enthalten die folgenden drei Eigenschafts Schlüssel:

-   [UI- \_ pkey- \_ Bezeichnung](windowsribbon-reference-properties-uipkey-label.md)
-   [UI \_ pkey \_ labeldescription](windowsribbon-reference-properties-uipkey-labeldescription.md)
-   [UI- \_ pkey \_ fixiert](windowsribbon-reference-properties-uipkey-pinned.md)

Die Liste der MRU-Elemente wird als **SAFEARRAY** der [**iuisimplepropertyset**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) -Zeiger auf die entsprechenden Implementierungen in der Host Anwendung an die Menüband-Host Anwendung übergeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zustands Eigenschaften](windowsribbon-reference-properties-state.md)
</dt> </dl>

 

 