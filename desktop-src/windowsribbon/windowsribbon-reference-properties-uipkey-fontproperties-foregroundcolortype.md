---
title: UI_PKEY_FontProperties_ForegroundColorType
description: Identifiziert die \_ PKEY \_ FontProperties \_ ForegroundColorType-Eigenschaft der Benutzeroberfläche.
ms.assetid: ab04c0b0-911f-4649-9ce8-5ecd847abf9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f261256a36ee7a387c6c3a695d8c1182898690c2
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444351"
---
# <a name="ui_pkey_fontproperties_foregroundcolortype"></a><span data-ttu-id="223be-103">UI \_ PKEY \_ FontProperties \_ ForegroundColorType</span><span class="sxs-lookup"><span data-stu-id="223be-103">UI\_PKEY\_FontProperties\_ForegroundColorType</span></span>

<span data-ttu-id="223be-104">Identifiziert die \_ PKEY \_ FontProperties \_ ForegroundColorType-Eigenschaft der Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="223be-104">Identifies the UI\_PKEY\_FontProperties\_ForegroundColorType property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_ForegroundColorType
   shellPKey = UI_PKEY_FontProperties_ForegroundColorType
   formatID = 00000310-7363-696e-8441798acf5aebb7
   propID = 310
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a><span data-ttu-id="223be-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="223be-105">Remarks</span></span>

<span data-ttu-id="223be-106">Ui \_ PKEY \_ FontProperties \_ ForegroundColorType wird von einer Anwendung in Verbindung mit [der Benutzeroberfläche \_ PKEY \_ FontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md)verwendet, um Einstellungen des **Textfarbkatalogs** abzufragen.</span><span class="sxs-lookup"><span data-stu-id="223be-106">UI\_PKEY\_FontProperties\_ForegroundColorType is used by an application, in conjunction with [UI\_PKEY\_FontProperties\_ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md), to query **Text color** gallery settings.</span></span>

<span data-ttu-id="223be-107">Der Eigenschaftswert stammt aus der [**\_ SWATCHCOLORTYPE-Enumeration der Benutzeroberfläche.**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)</span><span class="sxs-lookup"><span data-stu-id="223be-107">The property value is from the [**UI\_SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) enumeration.</span></span>

<span data-ttu-id="223be-108">Standardwert: `UI_SWATCHCOLORTYPE_RGB`.</span><span class="sxs-lookup"><span data-stu-id="223be-108">The default value is `UI_SWATCHCOLORTYPE_RGB`.</span></span>

<span data-ttu-id="223be-109">Die folgende Tabelle enthält eine Beschreibung der Eigenschaftswerte.</span><span class="sxs-lookup"><span data-stu-id="223be-109">The following table describes the property values.</span></span>



|     <span data-ttu-id="223be-110">Wert</span><span class="sxs-lookup"><span data-stu-id="223be-110">Value</span></span>                           |     <span data-ttu-id="223be-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="223be-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | <span data-ttu-id="223be-112">Wird von [**FontControl**](windowsribbon-element-fontcontrol.md)nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="223be-112">Not supported by the [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>                                                                                                                                                                                                                                                                                                                                        |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | <span data-ttu-id="223be-113">Die Anwendung sollte die entsprechende Systemmetrik für den Farbwert abfragen, in der Regel die aktuelle **Windows-Designtextfarbe,** die mit GetSysColor(COLOR \_ WINDOWTEXT) abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="223be-113">Application should query the appropriate system metric for the color value typically the current Windows theme **text color** that is retrieved with GetSysColor(COLOR\_WINDOWTEXT).</span></span>                                                                                                                                                                                                                                  |
| `UI_SWATCHCOLORTYPE_RGB`       | <span data-ttu-id="223be-114">Die Anwendung sollte [die \_ Ui-PKEY \_ FontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) nach dem Farbwert abfragen.</span><span class="sxs-lookup"><span data-stu-id="223be-114">Application should query [UI\_PKEY\_FontProperties\_ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) for the color value.</span></span> <span data-ttu-id="223be-115">Der Farbwert von [ \_ UI PKEY \_ FontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) wird auf der Schaltfläche **Textfarbe** angezeigt und im **Textfarbkatalog** ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="223be-115">The color value of [UI\_PKEY\_FontProperties\_ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) is displayed on the **Text color** button and selected in the **Text color** gallery.</span></span><br/> |



 

<span data-ttu-id="223be-116">Ui \_ PKEY \_ FontProperties \_ ForegroundColorType wird an die [**IUICommandHandler::Execute-Rückrufmethode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) übergeben, wenn eine Farbwatch in einem [**FontControl**](windowsribbon-element-fontcontrol.md) **Text-Farbkatalog** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="223be-116">UI\_PKEY\_FontProperties\_ForegroundColorType is passed to the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) callback method when a color swatch is selected in a [**FontControl**](windowsribbon-element-fontcontrol.md) **Text color** gallery.</span></span>

> [!Note]  
> <span data-ttu-id="223be-117">Es wird dringend empfohlen, dass die Anwendung nur einen anfänglichen **Textfarbwert** und diesen Wert nicht neu festlegen soll, wenn der Cursor innerhalb eines Dokuments neu positioniert wird.</span><span class="sxs-lookup"><span data-stu-id="223be-117">It is highly recommended that the application only set an initial **Text color** value and not re-set this value when the cursor is repositioned within a document.</span></span> <span data-ttu-id="223be-118">Die letzte Auswahl sollte beibehalten werden, um zu vermeiden, dass die gewünschte Farbe erneut ausgewählt werden muss.</span><span class="sxs-lookup"><span data-stu-id="223be-118">The last selection should be maintained to avoid the need to re-select the desired color.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="223be-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="223be-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="223be-120">Eigenschaften des Schriftartsteuerelements</span><span class="sxs-lookup"><span data-stu-id="223be-120">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="223be-121">**UI \_ SWATCHCOLORTYPE**</span><span class="sxs-lookup"><span data-stu-id="223be-121">**UI\_SWATCHCOLORTYPE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[<span data-ttu-id="223be-122">Schriftartsteuerelement</span><span class="sxs-lookup"><span data-stu-id="223be-122">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

