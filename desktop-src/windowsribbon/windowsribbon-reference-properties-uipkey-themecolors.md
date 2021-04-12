---
title: UI_PKEY_ThemeColors
description: Gibt die Benutzeroberflächen- \_ pkey- \_ Eigenschaft "mecolors" an.
ms.assetid: d539cbaa-45dc-4f9e-830e-e81fb289b4ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f5991ce5058de5a6f49ca8929de02e19657a610
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315357"
---
# <a name="ui_pkey_themecolors"></a><span data-ttu-id="6d4e3-103">UI- \_ pkey-Elemente \_</span><span class="sxs-lookup"><span data-stu-id="6d4e3-103">UI\_PKEY\_ThemeColors</span></span>

<span data-ttu-id="6d4e3-104">Gibt die Benutzeroberflächen- \_ pkey- \_ Eigenschaft "mecolors" an.</span><span class="sxs-lookup"><span data-stu-id="6d4e3-104">Identifies the UI\_PKEY\_ThemeColors property.</span></span>

```
propertyDescription
   name = UI_PKEY_ThemeColors
   shellPKey = UI_PKEY_ThemeColors
   formatID = 00000409-7363-696e-8441798acf5aebb7
   propID = 409
   typeInfo
      type = VT_VECTOR | VT_UI4
```

## <a name="remarks"></a><span data-ttu-id="6d4e3-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d4e3-105">Remarks</span></span>

<span data-ttu-id="6d4e3-106">Die Benutzeroberflächen- \_ pkey-Datei \_ wird von einer Anwendung verwendet, um die Farbmuster Werte von [**dropdowncolorpicker**](windowsribbon-element-dropdowncolorpicker.md)abzufragen.</span><span class="sxs-lookup"><span data-stu-id="6d4e3-106">UI\_PKEY\_ThemeColors is used by an application to query the color swatch values of a [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span></span>

<span data-ttu-id="6d4e3-107">Jeder [COLORREF](../gdi/colorref.md) -Wert entspricht einem Farbmuster in einer [**dropdowncolorpicker**](windowsribbon-element-dropdowncolorpicker.md) , wobei `ThemeColors` als Wert des **colortemplate** -Attributs angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6d4e3-107">Each [COLORREF](../gdi/colorref.md) value corresponds to a color swatch in a [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) where `ThemeColors` is specified as the value of the **ColorTemplate** attribute.</span></span>

<span data-ttu-id="6d4e3-108">Der Eigenschafts Wert ist ein Array von [COLORREF](../gdi/colorref.md) -Werten.</span><span class="sxs-lookup"><span data-stu-id="6d4e3-108">The property value is an array of [COLORREF](../gdi/colorref.md) values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d4e3-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6d4e3-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d4e3-110">Farbauswahl Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6d4e3-110">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 