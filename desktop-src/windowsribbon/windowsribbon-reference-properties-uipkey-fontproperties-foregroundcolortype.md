---
title: UI_PKEY_FontProperties_ForegroundColorType
description: Identifiziert die Eigenschaft "Benutzeroberflächen- \_ pkey \_ fontproperties \_ foregroundcolortype".
ms.assetid: ab04c0b0-911f-4649-9ce8-5ecd847abf9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5589e9b21fc7ab0884a3cac51eba114ee77036b3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390574"
---
# <a name="ui_pkey_fontproperties_foregroundcolortype"></a><span data-ttu-id="8ba0c-103">UI \_ pkey \_ fontproperties \_ foregroundcolortype</span><span class="sxs-lookup"><span data-stu-id="8ba0c-103">UI\_PKEY\_FontProperties\_ForegroundColorType</span></span>

<span data-ttu-id="8ba0c-104">Identifiziert die Eigenschaft "Benutzeroberflächen- \_ pkey \_ fontproperties \_ foregroundcolortype".</span><span class="sxs-lookup"><span data-stu-id="8ba0c-104">Identifies the UI\_PKEY\_FontProperties\_ForegroundColorType property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_ForegroundColorType
   shellPKey = UI_PKEY_FontProperties_ForegroundColorType
   formatID = 00000310-7363-696e-8441798acf5aebb7
   propID = 310
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a><span data-ttu-id="8ba0c-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8ba0c-105">Remarks</span></span>

<span data-ttu-id="8ba0c-106">UI \_ pkey \_ fontproperties \_ foregroundcolortype wird von einer Anwendung verwendet, in Verbindung mit der [UI \_ pkey \_ fontproperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md), um die Einstellungen für die **Textfarbe** -Galerie abzufragen.</span><span class="sxs-lookup"><span data-stu-id="8ba0c-106">UI\_PKEY\_FontProperties\_ForegroundColorType is used by an application, in conjunction with [UI\_PKEY\_FontProperties\_ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md), to query **Text color** gallery settings.</span></span>

<span data-ttu-id="8ba0c-107">Der Eigenschafts Wert ist aus der [**UI- \_ swatchcolortype**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="8ba0c-107">The property value is from the [**UI\_SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) enumeration.</span></span>

<span data-ttu-id="8ba0c-108">Der Standardwert ist `UI_SWATCHCOLORTYPE_RGB`.</span><span class="sxs-lookup"><span data-stu-id="8ba0c-108">The default value is `UI_SWATCHCOLORTYPE_RGB`.</span></span>

<span data-ttu-id="8ba0c-109">Die folgende Tabelle enthält eine Beschreibung der Eigenschaftswerte.</span><span class="sxs-lookup"><span data-stu-id="8ba0c-109">The following table describes the property values.</span></span>



|                                |                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | <span data-ttu-id="8ba0c-110">Wird vom [**FontControl-Steuer**](windowsribbon-element-fontcontrol.md)Element nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8ba0c-110">Not supported by the [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>                                                                                                                                                                                                                                                                                                                                        |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | <span data-ttu-id="8ba0c-111">Die Anwendung sollte die entsprechende Systemmetrik für den Farbwert Abfragen, der in der Regel die aktuelle Windows-Design **Textfarbe** ist, die mit GetSysColor (Color \_ WindowText) abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="8ba0c-111">Application should query the appropriate system metric for the color value typically the current Windows theme **text color** that is retrieved with GetSysColor(COLOR\_WINDOWTEXT).</span></span>                                                                                                                                                                                                                                  |
| `UI_SWATCHCOLORTYPE_RGB`       | <span data-ttu-id="8ba0c-112">Die Anwendung sollte die Benutzeroberflächen- [ \_ pkey- \_ fontproperties- \_ Vordergrundfarbe](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) für den Farbwert Abfragen.</span><span class="sxs-lookup"><span data-stu-id="8ba0c-112">Application should query [UI\_PKEY\_FontProperties\_ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) for the color value.</span></span> <span data-ttu-id="8ba0c-113">Der Farbwert von [UI \_ pkey \_ fontproperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) wird auf der **Textfarbe** -Schaltfläche angezeigt und im **Text** Katalog ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="8ba0c-113">The color value of [UI\_PKEY\_FontProperties\_ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) is displayed on the **Text color** button and selected in the **Text color** gallery.</span></span><br/> |



 

<span data-ttu-id="8ba0c-114">UI \_ pkey \_ fontproperties \_ foregroundcolortype wird an die [**iuicommandhandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) -Rückruf Methode übergeben, wenn ein Farbmuster in einer [**FontControl**](windowsribbon-element-fontcontrol.md) - **textfarb** Galerie ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="8ba0c-114">UI\_PKEY\_FontProperties\_ForegroundColorType is passed to the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) callback method when a color swatch is selected in a [**FontControl**](windowsribbon-element-fontcontrol.md) **Text color** gallery.</span></span>

> [!Note]  
> <span data-ttu-id="8ba0c-115">Es wird dringend empfohlen, dass die Anwendung nur einen anfänglichen **textfarbwert** festlegen und diesen Wert nicht erneut festlegen, wenn der Cursor innerhalb eines Dokuments neu positioniert wird.</span><span class="sxs-lookup"><span data-stu-id="8ba0c-115">It is highly recommended that the application only set an initial **Text color** value and not re-set this value when the cursor is repositioned within a document.</span></span> <span data-ttu-id="8ba0c-116">Die letzte Auswahl sollte beibehalten werden, um zu vermeiden, dass die gewünschte Farbe erneut ausgewählt werden muss.</span><span class="sxs-lookup"><span data-stu-id="8ba0c-116">The last selection should be maintained to avoid the need to re-select the desired color.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8ba0c-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8ba0c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ba0c-118">Schriftart Steuerelement-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8ba0c-118">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="8ba0c-119">**UI- \_ swatchcolortype**</span><span class="sxs-lookup"><span data-stu-id="8ba0c-119">**UI\_SWATCHCOLORTYPE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[<span data-ttu-id="8ba0c-120">Schriftart-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="8ba0c-120">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

