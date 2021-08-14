---
title: UI_PKEY_ItemsSource
description: Identifiziert die \_ PKEY \_ ItemsSource-Eigenschaft der Benutzeroberfläche.
ms.assetid: f5e99d2a-f50a-4932-ae77-581037cb9ac8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 017a3fc8f05c24c8d1996202b1db08a459f1a3747e3f787b521a70e6e3a25df0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118201570"
---
# <a name="ui_pkey_itemssource"></a>UI \_ PKEY \_ ItemsSource

Identifiziert die \_ PKEY \_ ItemsSource-Eigenschaft der Benutzeroberfläche.

```
propertyDescription
   name = UI_PKEY_ItemsSource
   shellPKey = UI_PKEY_ItemsSource
   formatID = 00000101-7363-696e-8441798acf5aebb7
   propID = 101
   typeInfo
      type = IUICollection
```

## <a name="remarks"></a>Hinweise

Ui \_ PKEY \_ ItemsSource wird von einer Anwendung verwendet, um die Sammlung von Elementen in einem Katalogsteuerelement abzufragen, z. B. die Schnellzugriffssymbolleiste (Quick Access Toolbar, QAT).

Der Eigenschaftswert ist ein [**IUICollection-Objekt.**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)

Jedes Element in dieser [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) muss [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) implementieren, um die schreibgeschützten Eigenschaften verfügbar zu machen, die dem Element zugeordnet sind, z. B. die Bezeichnung oder das Bild.

Verwenden Sie zum Hinzufügen oder Löschen von Elementen in einem Katalogsteuerelement zur Laufzeit die [**IUICollection-Methoden.**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)

Der folgende Screenshot veranschaulicht eine Auflistung von Elementen in einem [**SplitButtonGallery-Menü.**](windowsribbon-element-splitbuttongallery.md)

![Screenshot: Kategorien in einem Menübandkatalog](images/markup/splitbutton-gallery-control.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sammlungseigenschaften](windowsribbon-reference-properties-collection.md)
</dt> </dl>

 

 