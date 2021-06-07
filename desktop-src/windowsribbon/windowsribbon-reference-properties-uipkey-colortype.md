---
title: UI_PKEY_ColorType
description: Identifiziert die \_ PKEY \_ ColorType-Eigenschaft der Benutzeroberfläche.
ms.assetid: 7eaa9d8b-0c21-487c-9093-79ddffcae131
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9240d8c816adcf2674efcc2e7428d22b765f542
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443891"
---
# <a name="ui_pkey_colortype"></a><span data-ttu-id="431d5-103">UI \_ PKEY \_ ColorType</span><span class="sxs-lookup"><span data-stu-id="431d5-103">UI\_PKEY\_ColorType</span></span>

<span data-ttu-id="431d5-104">Identifiziert die \_ PKEY \_ ColorType-Eigenschaft der Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="431d5-104">Identifies the UI\_PKEY\_ColorType property.</span></span>

```
propertyDescription
   name = UI_PKEY_ColorType
   shellPKey = UI_PKEY_ColorType
   formatID = 00000401-7363-696e-8441798acf5aebb7
   propID = 401
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a><span data-ttu-id="431d5-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="431d5-105">Remarks</span></span>

<span data-ttu-id="431d5-106">Ui \_ PKEY \_ ColorType wird von einer Anwendung zum Abfragen der Farbeinstellung des [**DropDownColorPicker-Steuerelements**](windowsribbon-element-dropdowncolorpicker.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="431d5-106">UI\_PKEY\_ColorType is used by an application to query color setting of the [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) control.</span></span>

<span data-ttu-id="431d5-107">Der Eigenschaftswert stammt aus der [**\_ SWATCHCOLORTYPE-Enumeration der Benutzeroberfläche.**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)</span><span class="sxs-lookup"><span data-stu-id="431d5-107">The property value is from the [**UI\_SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) enumeration.</span></span>



|    <span data-ttu-id="431d5-108">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="431d5-108">Property</span></span>                            |    <span data-ttu-id="431d5-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="431d5-109">Description</span></span>                                                                                                                                                                             |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="431d5-110">UI \_ SWATCHCOLORTYPE \_ NOCOLOR</span><span class="sxs-lookup"><span data-stu-id="431d5-110">UI\_SWATCHCOLORTYPE\_NOCOLOR</span></span>   | <span data-ttu-id="431d5-111">Die Anwendung sollte die Farbeinstellung als transparent behandeln.</span><span class="sxs-lookup"><span data-stu-id="431d5-111">Application should treat the color setting as transparent.</span></span> <span data-ttu-id="431d5-112">Wird in der Regel in Verbindung mit der Einstellung **Keine Farbe** verwendet.</span><span class="sxs-lookup"><span data-stu-id="431d5-112">Typically used in conjunction with the **No color** color setting.</span></span>                                                   |
| <span data-ttu-id="431d5-113">UI \_ SWATCHCOLORTYPE \_ AUTOMATIC</span><span class="sxs-lookup"><span data-stu-id="431d5-113">UI\_SWATCHCOLORTYPE\_AUTOMATIC</span></span> | <span data-ttu-id="431d5-114">Die Anwendung sollte [GetSysColor(COLOR \_ WINDOWTEXT)](/windows/win32/api/winuser/nf-winuser-getsyscolor)abfragen.</span><span class="sxs-lookup"><span data-stu-id="431d5-114">Application should query [GetSysColor(COLOR\_WINDOWTEXT)](/windows/win32/api/winuser/nf-winuser-getsyscolor).</span></span> <span data-ttu-id="431d5-115">Wird in der Regel in Verbindung mit der Farbeinstellung **Automatisch** verwendet.</span><span class="sxs-lookup"><span data-stu-id="431d5-115">Typically used in conjunction with the **Automatic** color setting.</span></span> |
| <span data-ttu-id="431d5-116">UI \_ SWATCHCOLORTYPE \_ RGB</span><span class="sxs-lookup"><span data-stu-id="431d5-116">UI\_SWATCHCOLORTYPE\_RGB</span></span>       | <span data-ttu-id="431d5-117">Die Anwendung sollte [die \_ \_ PKEY-Farbe](windowsribbon-reference-properties-uipkey-color.md) der Benutzeroberfläche für die Farbeinstellung abfragen.</span><span class="sxs-lookup"><span data-stu-id="431d5-117">Application should query [UI\_PKEY\_Color](windowsribbon-reference-properties-uipkey-color.md) for the color setting.</span></span>                                                          |



 

<span data-ttu-id="431d5-118">Ui \_ PKEY \_ ColorType wird an die [**IUICommandHandler::Execute-Rückrufmethode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) übergeben, wenn eine Farbwatch in einem [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="431d5-118">UI\_PKEY\_ColorType is passed to the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) callback method when a color swatch is selected in a [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="431d5-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="431d5-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="431d5-120">Farbwähler-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="431d5-120">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 