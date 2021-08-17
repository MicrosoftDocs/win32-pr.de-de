---
title: UI_PKEY_Categories
description: Identifiziert die \_ PKEY Categories-Eigenschaft der \_ Benutzeroberfläche.
ms.assetid: 15f97307-ea3d-407a-a276-46b82f81bdbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4aa812673f289b80b000710dd48a449656368f00d0beb51dcb489e60328e6a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086547"
---
# <a name="ui_pkey_categories"></a>\_PKEY-Kategorien der Benutzeroberfläche \_

Identifiziert die \_ PKEY Categories-Eigenschaft der \_ Benutzeroberfläche.

```
propertyDescription
   name = UI_PKEY_Categories
   shellPKey = UI_PKEY_Categories
   formatID = 00000102-7363-696e-8441798acf5aebb7
   propID = 102
   typeInfo
      type = IUICollection
```

## <a name="remarks"></a>Hinweise

\_Benutzeroberflächen-PKEY-Kategorien \_ werden von einer Anwendung verwendet, um die Kategorien abzufragen, die zum Gruppieren verwandter Elemente in einem Katalogsteuerelement verwendet werden.

Der Eigenschaftswert ist ein [**IUICollection-Objekt,**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) bei dem jedes Element in der Auflistung eine Kategorie darstellt.

Jedes Element in dieser [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) muss [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) implementieren, um die schreibgeschützten Eigenschaften verfügbar zu machen, die dem Element zugeordnet sind, z. B. die Bezeichnung oder das Bild.

Verwenden Sie zum Hinzufügen oder Löschen von Elementen in einem Katalogsteuerelement zur Laufzeit die verschiedenen Methoden von [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection).

Der folgende Screenshot veranschaulicht die Verwendung von zwei Kategorien: **Auswahlformen** und **Auswahloptionen** in einem [**SplitButton-Menü.**](windowsribbon-element-splitbutton.md)

![Screenshot mit zwei Kategorien: Auswahlformen und Auswahloptionen in einem Splitbuttongallery-Steuerelement.](images/properties/ui-pkey-collection-categories2.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sammlungseigenschaften](windowsribbon-reference-properties-collection.md)
</dt> <dt>

[\_PKEY-Kategorie-ID der Benutzeroberfläche \_](windowsribbon-reference-properties-uipkey-categoryid.md)
</dt> </dl>

 

 