---
title: UI_PKEY_ItemsSource
description: Identifiziert die \_ \_ ItemsSource-Eigenschaft der UI pkey.
ms.assetid: f5e99d2a-f50a-4932-ae77-581037cb9ac8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67bdc52a7688648f59be74c22516ee790d109dd2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729472"
---
# <a name="ui_pkey_itemssource"></a>UI- \_ pkey \_ ItemsSource

Identifiziert die \_ \_ ItemsSource-Eigenschaft der UI pkey.

```
propertyDescription
   name = UI_PKEY_ItemsSource
   shellPKey = UI_PKEY_ItemsSource
   formatID = 00000101-7363-696e-8441798acf5aebb7
   propID = 101
   typeInfo
      type = IUICollection
```

## <a name="remarks"></a>Bemerkungen

UI \_ pkey \_ ItemsSource wird von einer Anwendung verwendet, um die Auflistung von Elementen in einem Katalog-Steuerelement abzufragen, z. b. die Symbolleiste für den schnell Zugriff (QAT).

Der Eigenschafts Wert ist ein [**iuicollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) -Objekt.

Jedes Element in dieser [**iuicollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) muss [**iuisimplepropertyset**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) implementieren, um die schreibgeschützten Eigenschaften, die dem Element zugeordnet sind, wie z. b. die Bezeichnung oder das Bild verfügbar zu machen.

Um Elemente in einem Katalog-Steuerelement zur Laufzeit hinzuzufügen oder zu löschen, verwenden Sie die [**iuicollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) -Methoden.

Der folgende Screenshot veranschaulicht eine Sammlung von Elementen in einem [**splitbuttongallery**](windowsribbon-element-splitbuttongallery.md) -Menü.

![Screenshot mit Kategorien in einem Menüband-Katalog](images/markup/splitbutton-gallery-control.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sammlungs Eigenschaften](windowsribbon-reference-properties-collection.md)
</dt> </dl>

 

 