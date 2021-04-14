---
title: UI_PKEY_FontProperties_BackgroundColorType
description: Gibt die Benutzeroberflächen- \_ Eigenschaft "pkey \_ fontproperties \_ backgroundcolortype" an.
ms.assetid: d93f4d9f-3d35-4066-be94-f6b6b4302bff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 568898cb2706eb932ea708f929aa4791f0643c74
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473268"
---
# <a name="ui_pkey_fontproperties_backgroundcolortype"></a><span data-ttu-id="291e1-103">UI \_ pkey \_ fontproperties \_ backgroundcolortype</span><span class="sxs-lookup"><span data-stu-id="291e1-103">UI\_PKEY\_FontProperties\_BackgroundColorType</span></span>

<span data-ttu-id="291e1-104">Gibt die Benutzeroberflächen- \_ Eigenschaft "pkey \_ fontproperties \_ backgroundcolortype" an.</span><span class="sxs-lookup"><span data-stu-id="291e1-104">Identifies the UI\_PKEY\_FontProperties\_BackgroundColorType property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_BackgroundColorType
   shellPKey = UI_PKEY_FontProperties_BackgroundColorType
   formatID = 00000311-7363-696e-8441798acf5aebb7
   propID = 311
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a><span data-ttu-id="291e1-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="291e1-105">Remarks</span></span>

<span data-ttu-id="291e1-106">UI \_ pkey \_ fontproperties \_ backgroundcolortype wird von einer Anwendung in Verbindung mit der [UI \_ pkey \_ fontproperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor)verwendet, um Text Hervorhebungs **Farb** Galerie-Einstellungen abzufragen.</span><span class="sxs-lookup"><span data-stu-id="291e1-106">UI\_PKEY\_FontProperties\_BackgroundColorType is used by an application, in conjunction with [UI\_PKEY\_FontProperties\_BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor), to query **Text highlight color** gallery settings.</span></span>

<span data-ttu-id="291e1-107">Der Eigenschafts Wert ist aus der [**UI- \_ swatchcolortype**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="291e1-107">The property value is from the [**UI\_SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) enumeration.</span></span>

<span data-ttu-id="291e1-108">Der Standardwert ist `UI_SWATCHCOLORTYPE_RGB`.</span><span class="sxs-lookup"><span data-stu-id="291e1-108">The default value is `UI_SWATCHCOLORTYPE_RGB`.</span></span>

<span data-ttu-id="291e1-109">Die folgende Tabelle enthält eine Beschreibung der Eigenschaftswerte.</span><span class="sxs-lookup"><span data-stu-id="291e1-109">The following table describes the property values.</span></span>



|                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | <span data-ttu-id="291e1-110">Die Anwendung sollte die entsprechende Systemmetrik für den Farbwert Abfragen, der in der Regel die aktuelle **Hintergrundfarbe** des Windows-Design Fensters ist, die mit GetSysColor (Farb \_ Fenster) abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="291e1-110">Application should query the appropriate system metric for the color value typically the current Windows theme **window background color** that is retrieved with GetSysColor(COLOR\_WINDOW).</span></span>                                                                                                                                                                                                                                                                 |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | <span data-ttu-id="291e1-111">Wird vom [**FontControl-Steuer**](windowsribbon-element-fontcontrol.md)Element nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="291e1-111">Not supported by the [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                |
| `UI_SWATCHCOLORTYPE_RGB`       | <span data-ttu-id="291e1-112">Die Anwendung sollte die [UI \_ pkey \_ fontproperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) für den Farbwert Abfragen.</span><span class="sxs-lookup"><span data-stu-id="291e1-112">Application should query [UI\_PKEY\_FontProperties\_BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) for the color value.</span></span> <span data-ttu-id="291e1-113">Der Farbwert von [UI \_ pkey \_ fontproperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) wird auf der Schaltfläche Text Hervorhebungs **Farbe** angezeigt und in der **Farb Galerie Text hervorheben** ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="291e1-113">The color value of [UI\_PKEY\_FontProperties\_BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) is displayed on the **Text highlight color** button and selected in the **Text highlight color** gallery.</span></span><br/> |



 

<span data-ttu-id="291e1-114">UI \_ pkey \_ fontproperties \_ backgroundcolortype wird an die [**iuicommandhandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) -Rückruf Methode übergeben, wenn in einer [**FontControl**](windowsribbon-element-fontcontrol.md) -Text Hervorhebungs **Farb** Galerie ein Farbmuster ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="291e1-114">UI\_PKEY\_FontProperties\_BackgroundColorType is passed to the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) callback method when a color swatch is selected in a [**FontControl**](windowsribbon-element-fontcontrol.md) **Text highlight color** gallery.</span></span>

> [!Note]  
> <span data-ttu-id="291e1-115">Es wird dringend empfohlen, dass die Anwendung nur einen anfänglichen Text Hervorhebungs **Farbwert** festlegen und diesen Wert nicht neu festlegen, wenn der Cursor innerhalb eines Dokuments neu positioniert wird.</span><span class="sxs-lookup"><span data-stu-id="291e1-115">It is highly recommended that the application only set an initial **Text highlight color** value and not re-set this value when the cursor is repositioned within a document.</span></span> <span data-ttu-id="291e1-116">Die letzte Auswahl sollte beibehalten werden, um zu vermeiden, dass die gewünschte Farbe erneut ausgewählt werden muss.</span><span class="sxs-lookup"><span data-stu-id="291e1-116">The last selection should be maintained to avoid the need to re-select the desired color.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="291e1-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="291e1-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="291e1-118">Schriftart Steuerelement-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="291e1-118">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="291e1-119">**UI- \_ swatchcolortype**</span><span class="sxs-lookup"><span data-stu-id="291e1-119">**UI\_SWATCHCOLORTYPE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[<span data-ttu-id="291e1-120">Schriftart-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="291e1-120">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

