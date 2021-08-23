---
title: UI_PKEY_RecentItems
description: Identifiziert die \_ PKEY \_ RecentItems-Eigenschaft der Benutzeroberfläche.
ms.assetid: 54e7ad1f-86b3-45e0-a0f4-5ee0d08e9d4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c04e18400f297edae1f9a1eda54bccbcd6c31c9f1d9b40408e243b6c275a83ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437956"
---
# <a name="ui_pkey_recentitems"></a>UI \_ PKEY \_ RecentItems

Identifiziert die \_ PKEY \_ RecentItems-Eigenschaft der Benutzeroberfläche.

```
propertyDescription
   name = UI_PKEY_RecentItems
   shellPKey = UI_PKEY_RecentItems
   formatID = 00000350-7363-696e-8441798acf5aebb7
   propID = 350
   typeInfo
      type = VT_ARRAY | VT_UNKNOWN
```

## <a name="remarks"></a>Hinweise

[Benutzeroberfläche \_ PKEY \_ Pinned](windowsribbon-reference-properties-uipkey-pinned.md) wird von einer Anwendung verwendet, um das Array von Elementen in der sammlung zuletzt verwendeter Elemente (MRU) des [Anwendungsmenüs](windowsribbon-controls-applicationmenu.md)abzufragen. Die Informationen für jedes MRU-Element sind in einem [**IUISimplePropertySet-Objekt**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) gekapselt und enthalten die folgenden drei Eigenschaftsschlüssel:

-   [\_ \_ UI-PKEY-Bezeichnung](windowsribbon-reference-properties-uipkey-label.md)
-   [UI \_ PKEY \_ LabelDescription](windowsribbon-reference-properties-uipkey-labeldescription.md)
-   [\_ \_ PKEY-Benutzeroberfläche angeheftet](windowsribbon-reference-properties-uipkey-pinned.md)

Die Liste der MRU-Elemente wird als **SAFEARRAY** von [**IUISimplePropertySet-Zeigern**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) auf die entsprechenden Implementierungen in der Hostanwendung an die Menübandhostanwendung übergeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zustandseigenschaften](windowsribbon-reference-properties-state.md)
</dt> </dl>

 

 