---
title: UI_PKEY_FontProperties_BackgroundColorType
description: Identifiziert die \_ Ui-Eigenschaft PKEY \_ FontProperties \_ BackgroundColorType.
ms.assetid: d93f4d9f-3d35-4066-be94-f6b6b4302bff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45bbd2056087d584663c8ca716c4021554098dfa
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443821"
---
# <a name="ui_pkey_fontproperties_backgroundcolortype"></a><span data-ttu-id="738ed-103">UI \_ PKEY \_ FontProperties \_ BackgroundColorType</span><span class="sxs-lookup"><span data-stu-id="738ed-103">UI\_PKEY\_FontProperties\_BackgroundColorType</span></span>

<span data-ttu-id="738ed-104">Identifiziert die \_ Ui-Eigenschaft PKEY \_ FontProperties \_ BackgroundColorType.</span><span class="sxs-lookup"><span data-stu-id="738ed-104">Identifies the UI\_PKEY\_FontProperties\_BackgroundColorType property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_BackgroundColorType
   shellPKey = UI_PKEY_FontProperties_BackgroundColorType
   formatID = 00000311-7363-696e-8441798acf5aebb7
   propID = 311
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a><span data-ttu-id="738ed-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="738ed-105">Remarks</span></span>

<span data-ttu-id="738ed-106">Ui \_ PKEY \_ FontProperties \_ BackgroundColorType wird von einer Anwendung in Verbindung mit [der Benutzeroberfläche \_ PKEY \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor)verwendet, um Einstellungen des **Textmarkerfarbkatalogs** abzufragen.</span><span class="sxs-lookup"><span data-stu-id="738ed-106">UI\_PKEY\_FontProperties\_BackgroundColorType is used by an application, in conjunction with [UI\_PKEY\_FontProperties\_BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor), to query **Text highlight color** gallery settings.</span></span>

<span data-ttu-id="738ed-107">Der Eigenschaftswert stammt aus der [**\_ SWATCHCOLORTYPE-Enumeration der Benutzeroberfläche.**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)</span><span class="sxs-lookup"><span data-stu-id="738ed-107">The property value is from the [**UI\_SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) enumeration.</span></span>

<span data-ttu-id="738ed-108">Standardwert: `UI_SWATCHCOLORTYPE_RGB`.</span><span class="sxs-lookup"><span data-stu-id="738ed-108">The default value is `UI_SWATCHCOLORTYPE_RGB`.</span></span>

<span data-ttu-id="738ed-109">Die folgende Tabelle enthält eine Beschreibung der Eigenschaftswerte.</span><span class="sxs-lookup"><span data-stu-id="738ed-109">The following table describes the property values.</span></span>



|   <span data-ttu-id="738ed-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="738ed-110">Property</span></span>                             |   <span data-ttu-id="738ed-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="738ed-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | <span data-ttu-id="738ed-112">Die Anwendung sollte die entsprechende Systemmetrik für den Farbwert abfragen, in der Regel die aktuelle **Hintergrundfarbe** des Windows-Designfensters, die mit GetSysColor(COLOR WINDOW) abgerufen \_ wird.</span><span class="sxs-lookup"><span data-stu-id="738ed-112">Application should query the appropriate system metric for the color value typically the current Windows theme **window background color** that is retrieved with GetSysColor(COLOR\_WINDOW).</span></span>                                                                                                                                                                                                                                                                 |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | <span data-ttu-id="738ed-113">Wird von [**FontControl**](windowsribbon-element-fontcontrol.md)nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="738ed-113">Not supported by the [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                |
| `UI_SWATCHCOLORTYPE_RGB`       | <span data-ttu-id="738ed-114">Die Anwendung sollte [die Benutzeroberfläche \_ PKEY \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) nach dem Farbwert abfragen.</span><span class="sxs-lookup"><span data-stu-id="738ed-114">Application should query [UI\_PKEY\_FontProperties\_BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) for the color value.</span></span> <span data-ttu-id="738ed-115">Der Farbwert von [ \_ UI-PKEY \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) wird auf der Schaltfläche **Text highlight color (Text hervorhebungsfarbe)** angezeigt und im **Farbkatalog textmarkiert** ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="738ed-115">The color value of [UI\_PKEY\_FontProperties\_BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) is displayed on the **Text highlight color** button and selected in the **Text highlight color** gallery.</span></span><br/> |



 

<span data-ttu-id="738ed-116">Ui \_ PKEY \_ FontProperties \_ BackgroundColorType wird an die [**IUICommandHandler::Execute-Rückrufmethode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) übergeben, wenn in einem [**FontControl**](windowsribbon-element-fontcontrol.md) **Text Highlight** Color Gallery eine Farbuhr ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="738ed-116">UI\_PKEY\_FontProperties\_BackgroundColorType is passed to the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) callback method when a color swatch is selected in a [**FontControl**](windowsribbon-element-fontcontrol.md) **Text highlight color** gallery.</span></span>

> [!Note]  
> <span data-ttu-id="738ed-117">Es wird dringend empfohlen, dass die Anwendung nur einen anfänglichen **Textmarkierungsfarbwert** und diesen Wert nicht neu festlegen soll, wenn der Cursor innerhalb eines Dokuments neu positioniert wird.</span><span class="sxs-lookup"><span data-stu-id="738ed-117">It is highly recommended that the application only set an initial **Text highlight color** value and not re-set this value when the cursor is repositioned within a document.</span></span> <span data-ttu-id="738ed-118">Die letzte Auswahl sollte beibehalten werden, um zu vermeiden, dass die gewünschte Farbe erneut ausgewählt werden muss.</span><span class="sxs-lookup"><span data-stu-id="738ed-118">The last selection should be maintained to avoid the need to re-select the desired color.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="738ed-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="738ed-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="738ed-120">Eigenschaften des Schriftartsteuerelements</span><span class="sxs-lookup"><span data-stu-id="738ed-120">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="738ed-121">**UI \_ SWATCHCOLORTYPE**</span><span class="sxs-lookup"><span data-stu-id="738ed-121">**UI\_SWATCHCOLORTYPE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[<span data-ttu-id="738ed-122">Schriftartsteuerelement</span><span class="sxs-lookup"><span data-stu-id="738ed-122">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

