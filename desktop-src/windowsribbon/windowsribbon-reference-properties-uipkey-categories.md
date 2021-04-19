---
title: UI_PKEY_Categories
description: Bezeichnet die Eigenschaft der UI- \_ pkey- \_ Kategorien.
ms.assetid: 15f97307-ea3d-407a-a276-46b82f81bdbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7666ee9eba6639f1f39b96f012b464854191ff0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106342141"
---
# <a name="ui_pkey_categories"></a>UI- \_ pkey- \_ Kategorien

Bezeichnet die Eigenschaft der UI- \_ pkey- \_ Kategorien.

```
propertyDescription
   name = UI_PKEY_Categories
   shellPKey = UI_PKEY_Categories
   formatID = 00000102-7363-696e-8441798acf5aebb7
   propID = 102
   typeInfo
      type = IUICollection
```

## <a name="remarks"></a>Bemerkungen

UI- \_ pkey- \_ Kategorien werden von einer Anwendung verwendet, um die Kategorien abzufragen, die zum Gruppieren verwandter Elemente in einem Katalog-Steuerelement verwendet werden.

Der Eigenschafts Wert ist ein [**iuicollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) -Objekt, in dem jedes Element in der Auflistung eine Kategorie darstellt.

Jedes Element in dieser [**iuicollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) muss [**iuisimplepropertyset**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) implementieren, um die schreibgeschützten Eigenschaften, die dem Element zugeordnet sind, wie z. b. die Bezeichnung oder das Bild verfügbar zu machen.

Um Elemente in einem Katalog-Steuerelement zur Laufzeit hinzuzufügen oder zu löschen, verwenden Sie die verschiedenen Methoden von [**iuicollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection).

Der folgende Screenshot veranschaulicht die Verwendung von zwei Kategorien, **Auswahl Formen** und **Auswahl Optionen** in einem [**SplitButton**](windowsribbon-element-splitbutton.md) -Menü.

![Screenshot, der zwei Kategorien, Auswahl Formen und Auswahl Optionen in einem splitbuttongallery-Steuerelement anzeigt.](images/properties/ui-pkey-collection-categories2.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sammlungs Eigenschaften](windowsribbon-reference-properties-collection.md)
</dt> <dt>

[Benutzeroberflächen- \_ pkey \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)
</dt> </dl>

 

 