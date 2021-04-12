---
title: UI_PKEY_ColorType
description: Bezeichnet die Benutzeroberflächen- \_ pkey \_ ColorType-Eigenschaft.
ms.assetid: 7eaa9d8b-0c21-487c-9093-79ddffcae131
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313d2a657d889a7c582d86d8f8c9e4ebd2cfd01e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315699"
---
# <a name="ui_pkey_colortype"></a><span data-ttu-id="2daf8-103">UI \_ pkey \_ ColorType</span><span class="sxs-lookup"><span data-stu-id="2daf8-103">UI\_PKEY\_ColorType</span></span>

<span data-ttu-id="2daf8-104">Bezeichnet die Benutzeroberflächen- \_ pkey \_ ColorType-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="2daf8-104">Identifies the UI\_PKEY\_ColorType property.</span></span>

```
propertyDescription
   name = UI_PKEY_ColorType
   shellPKey = UI_PKEY_ColorType
   formatID = 00000401-7363-696e-8441798acf5aebb7
   propID = 401
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a><span data-ttu-id="2daf8-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2daf8-105">Remarks</span></span>

<span data-ttu-id="2daf8-106">UI \_ pkey \_ ColorType wird von einer Anwendung verwendet, um die Farbeinstellung des [**dropdowncolorpicker**](windowsribbon-element-dropdowncolorpicker.md) -Steuer Elements abzufragen.</span><span class="sxs-lookup"><span data-stu-id="2daf8-106">UI\_PKEY\_ColorType is used by an application to query color setting of the [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) control.</span></span>

<span data-ttu-id="2daf8-107">Der Eigenschafts Wert ist aus der [**UI- \_ swatchcolortype**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="2daf8-107">The property value is from the [**UI\_SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) enumeration.</span></span>



|                                |                                                                                                                                                                                 |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2daf8-108">UI \_ swatchcolortype \_ nocolor</span><span class="sxs-lookup"><span data-stu-id="2daf8-108">UI\_SWATCHCOLORTYPE\_NOCOLOR</span></span>   | <span data-ttu-id="2daf8-109">Die Anwendung sollte die Farbeinstellung als transparent behandeln.</span><span class="sxs-lookup"><span data-stu-id="2daf8-109">Application should treat the color setting as transparent.</span></span> <span data-ttu-id="2daf8-110">Wird in der Regel in Verbindung mit der Einstellung " **keine farbfarbe** " verwendet.</span><span class="sxs-lookup"><span data-stu-id="2daf8-110">Typically used in conjunction with the **No color** color setting.</span></span>                                                   |
| <span data-ttu-id="2daf8-111">UI \_ swatchcolortype \_ automatisch</span><span class="sxs-lookup"><span data-stu-id="2daf8-111">UI\_SWATCHCOLORTYPE\_AUTOMATIC</span></span> | <span data-ttu-id="2daf8-112">Die Anwendung sollte [GetSysColor (Color \_ WindowText)](/windows/win32/api/winuser/nf-winuser-getsyscolor)Abfragen.</span><span class="sxs-lookup"><span data-stu-id="2daf8-112">Application should query [GetSysColor(COLOR\_WINDOWTEXT)](/windows/win32/api/winuser/nf-winuser-getsyscolor).</span></span> <span data-ttu-id="2daf8-113">Wird in der Regel in Verbindung mit der **automatischen** Farbeinstellung verwendet.</span><span class="sxs-lookup"><span data-stu-id="2daf8-113">Typically used in conjunction with the **Automatic** color setting.</span></span> |
| <span data-ttu-id="2daf8-114">UI- \_ swatchcolortype \_ RGB</span><span class="sxs-lookup"><span data-stu-id="2daf8-114">UI\_SWATCHCOLORTYPE\_RGB</span></span>       | <span data-ttu-id="2daf8-115">Die Anwendung sollte die Benutzeroberflächen- [ \_ pkey- \_ Farbe](windowsribbon-reference-properties-uipkey-color.md) für die Farbeinstellung Abfragen.</span><span class="sxs-lookup"><span data-stu-id="2daf8-115">Application should query [UI\_PKEY\_Color](windowsribbon-reference-properties-uipkey-color.md) for the color setting.</span></span>                                                          |



 

<span data-ttu-id="2daf8-116">\_Der UI pkey \_ ColorType wird an die [**iuicommandhandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) -Rückruf Methode übergeben, wenn in einem [**dropdowncolorpicker**](windowsribbon-element-dropdowncolorpicker.md)ein Farbmuster ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="2daf8-116">UI\_PKEY\_ColorType is passed to the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) callback method when a color swatch is selected in a [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2daf8-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2daf8-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2daf8-118">Farbauswahl Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2daf8-118">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 