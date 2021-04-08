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
# <a name="ui_pkey_itemssource"></a><span data-ttu-id="99425-103">UI- \_ pkey \_ ItemsSource</span><span class="sxs-lookup"><span data-stu-id="99425-103">UI\_PKEY\_ItemsSource</span></span>

<span data-ttu-id="99425-104">Identifiziert die \_ \_ ItemsSource-Eigenschaft der UI pkey.</span><span class="sxs-lookup"><span data-stu-id="99425-104">Identifies the UI\_PKEY\_ItemsSource property.</span></span>

```
propertyDescription
   name = UI_PKEY_ItemsSource
   shellPKey = UI_PKEY_ItemsSource
   formatID = 00000101-7363-696e-8441798acf5aebb7
   propID = 101
   typeInfo
      type = IUICollection
```

## <a name="remarks"></a><span data-ttu-id="99425-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="99425-105">Remarks</span></span>

<span data-ttu-id="99425-106">UI \_ pkey \_ ItemsSource wird von einer Anwendung verwendet, um die Auflistung von Elementen in einem Katalog-Steuerelement abzufragen, z. b. die Symbolleiste für den schnell Zugriff (QAT).</span><span class="sxs-lookup"><span data-stu-id="99425-106">UI\_PKEY\_ItemsSource is used by an application to query the collection of items in a gallery control, such as the Quick Access Toolbar (QAT).</span></span>

<span data-ttu-id="99425-107">Der Eigenschafts Wert ist ein [**iuicollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="99425-107">The property value is an [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object.</span></span>

<span data-ttu-id="99425-108">Jedes Element in dieser [**iuicollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) muss [**iuisimplepropertyset**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) implementieren, um die schreibgeschützten Eigenschaften, die dem Element zugeordnet sind, wie z. b. die Bezeichnung oder das Bild verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="99425-108">Each item in this [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) must implement [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) to expose the read-only properties associated with the item, such as the label or image.</span></span>

<span data-ttu-id="99425-109">Um Elemente in einem Katalog-Steuerelement zur Laufzeit hinzuzufügen oder zu löschen, verwenden Sie die [**iuicollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) -Methoden.</span><span class="sxs-lookup"><span data-stu-id="99425-109">To add or delete items in a gallery control at run time, use the [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) methods.</span></span>

<span data-ttu-id="99425-110">Der folgende Screenshot veranschaulicht eine Sammlung von Elementen in einem [**splitbuttongallery**](windowsribbon-element-splitbuttongallery.md) -Menü.</span><span class="sxs-lookup"><span data-stu-id="99425-110">The following screen shot illustrates a collection of items in a [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) menu.</span></span>

![Screenshot mit Kategorien in einem Menüband-Katalog](images/markup/splitbutton-gallery-control.png)

## <a name="related-topics"></a><span data-ttu-id="99425-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="99425-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99425-113">Sammlungs Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="99425-113">Collection Properties</span></span>](windowsribbon-reference-properties-collection.md)
</dt> </dl>

 

 