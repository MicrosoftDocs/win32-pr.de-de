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
# <a name="ui_pkey_categories"></a><span data-ttu-id="b3078-103">UI- \_ pkey- \_ Kategorien</span><span class="sxs-lookup"><span data-stu-id="b3078-103">UI\_PKEY\_Categories</span></span>

<span data-ttu-id="b3078-104">Bezeichnet die Eigenschaft der UI- \_ pkey- \_ Kategorien.</span><span class="sxs-lookup"><span data-stu-id="b3078-104">Identifies the UI\_PKEY\_Categories property.</span></span>

```
propertyDescription
   name = UI_PKEY_Categories
   shellPKey = UI_PKEY_Categories
   formatID = 00000102-7363-696e-8441798acf5aebb7
   propID = 102
   typeInfo
      type = IUICollection
```

## <a name="remarks"></a><span data-ttu-id="b3078-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b3078-105">Remarks</span></span>

<span data-ttu-id="b3078-106">UI- \_ pkey- \_ Kategorien werden von einer Anwendung verwendet, um die Kategorien abzufragen, die zum Gruppieren verwandter Elemente in einem Katalog-Steuerelement verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b3078-106">UI\_PKEY\_Categories is used by an application to query the categories that are used to group related items in a gallery control.</span></span>

<span data-ttu-id="b3078-107">Der Eigenschafts Wert ist ein [**iuicollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) -Objekt, in dem jedes Element in der Auflistung eine Kategorie darstellt.</span><span class="sxs-lookup"><span data-stu-id="b3078-107">The property value is an [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object where each item in the collection represents a category.</span></span>

<span data-ttu-id="b3078-108">Jedes Element in dieser [**iuicollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) muss [**iuisimplepropertyset**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) implementieren, um die schreibgeschützten Eigenschaften, die dem Element zugeordnet sind, wie z. b. die Bezeichnung oder das Bild verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="b3078-108">Each item in this [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) must implement [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) to expose the read-only properties associated with the item, such as the label or image.</span></span>

<span data-ttu-id="b3078-109">Um Elemente in einem Katalog-Steuerelement zur Laufzeit hinzuzufügen oder zu löschen, verwenden Sie die verschiedenen Methoden von [**iuicollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection).</span><span class="sxs-lookup"><span data-stu-id="b3078-109">To add or delete items in a gallery control at run time, use the various methods of [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection).</span></span>

<span data-ttu-id="b3078-110">Der folgende Screenshot veranschaulicht die Verwendung von zwei Kategorien, **Auswahl Formen** und **Auswahl Optionen** in einem [**SplitButton**](windowsribbon-element-splitbutton.md) -Menü.</span><span class="sxs-lookup"><span data-stu-id="b3078-110">The following screen shot illustrates the use of two categories, **Selection shapes** and **Selection options**, in a [**SplitButton**](windowsribbon-element-splitbutton.md) menu.</span></span>

![Screenshot, der zwei Kategorien, Auswahl Formen und Auswahl Optionen in einem splitbuttongallery-Steuerelement anzeigt.](images/properties/ui-pkey-collection-categories2.png)

## <a name="related-topics"></a><span data-ttu-id="b3078-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b3078-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3078-113">Sammlungs Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b3078-113">Collection Properties</span></span>](windowsribbon-reference-properties-collection.md)
</dt> <dt>

[<span data-ttu-id="b3078-114">Benutzeroberflächen- \_ pkey \_ CategoryID</span><span class="sxs-lookup"><span data-stu-id="b3078-114">UI\_PKEY\_CategoryId</span></span>](windowsribbon-reference-properties-uipkey-categoryid.md)
</dt> </dl>

 

 