---
title: UI_PKEY_FontProperties_VerticalPositioning
description: Bezeichnet die \_ verticalpositionierungs-Eigenschaft der UI-pkey- \_ fontproperties \_ .
ms.assetid: a92f845e-b0fc-4e23-9d06-ca16d2becf0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88b67e2a099b7ce02b3c94f7c9d799fcdda5e881
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039458"
---
# <a name="ui_pkey_fontproperties_verticalpositioning"></a><span data-ttu-id="e59c9-103">Benutzeroberflächen- \_ pkey \_ fontproperties \_ verticalpositionierung</span><span class="sxs-lookup"><span data-stu-id="e59c9-103">UI\_PKEY\_FontProperties\_VerticalPositioning</span></span>

<span data-ttu-id="e59c9-104">Bezeichnet die \_ verticalpositionierungs-Eigenschaft der UI-pkey- \_ fontproperties \_ .</span><span class="sxs-lookup"><span data-stu-id="e59c9-104">Identifies the UI\_PKEY\_FontProperties\_VerticalPositioning property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_VerticalPositioning
   shellPKey = UI_PKEY_FontProperties_VerticalPositioning
   formatID = 00000307-7363-696e-8441798acf5aebb7
   propID = 307
   typeInfo
      type = UI_FONTVERTICALPOSITION
```

## <a name="remarks"></a><span data-ttu-id="e59c9-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e59c9-105">Remarks</span></span>

<span data-ttu-id="e59c9-106">Benutzeroberflächen \_ -pkey \_ fontproperties \_ verticalpositionierung wird von einer Anwendung verwendet, um den Wert der **SuperScript** -und Index Steuerelemente abzufragen. </span><span class="sxs-lookup"><span data-stu-id="e59c9-106">UI\_PKEY\_FontProperties\_VerticalPositioning is used by an application to query the value of the **Superscript** and **Subscript** controls.</span></span>

<span data-ttu-id="e59c9-107">Der Eigenschafts Wert ist aus der [**UI \_ fontverticalposition**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="e59c9-107">The property value is from the [**UI\_FONTVERTICALPOSITION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition) enumeration.</span></span>

<span data-ttu-id="e59c9-108">Der Standardwert ist `UI_FONTVERTICALPOSITION_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="e59c9-108">The default value is `UI_FONTVERTICALPOSITION_NOTSET`.</span></span>

<span data-ttu-id="e59c9-109">Der folgende Screenshot zeigt die Schaltflächen **SuperScript** **und Index** des Menübands [**FontControl**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="e59c9-109">The following screen shot shows the **Superscript** and **Subscript** buttons of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![Screenshot des FontControl-Elements, bei dem das richfont-Attribut auf "true" festgelegt ist.](images/markup/fontcontrol-subsuper.png)

<span data-ttu-id="e59c9-111">In der folgenden Tabelle werden die Eigenschaften und das Benutzeroberflächen Ergebnis beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e59c9-111">The following table describes the properties and the UI result.</span></span>



|                                        |                                                                                                |
|----------------------------------------|------------------------------------------------------------------------------------------------|
| `UI_FONTVERTICALPOSITION_NOTAVAILABLE` | <span data-ttu-id="e59c9-112">**SuperScript** -und Index **-Schaltflächen sind deaktiviert und können** nur von der Anwendung festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e59c9-112">**Superscript** and **Subscript** buttons are disabled and can only be set by the application.</span></span> |
| `UI_FONTVERTICALPOSITION_NOTSET`       | <span data-ttu-id="e59c9-113">Die **Schaltflächen** **SuperScript** und Index werden nicht ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="e59c9-113">**Superscript** and **Subscript** buttons are not selected.</span></span>                                    |
| `UI_FONTVERTICALPOSITION_SUPERSCRIPT`  | <span data-ttu-id="e59c9-114">Die Schaltfläche **SuperScript** ist ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="e59c9-114">**Superscript** button is selected.</span></span>                                                            |
| `UI_FONTVERTICALPOSITION_SUBSCRIPT`    | <span data-ttu-id="e59c9-115">Die Schaltfläche " **Abonnement** " ist ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="e59c9-115">**Subscript** button is selected.</span></span>                                                              |



 

> [!Note]  
> <span data-ttu-id="e59c9-116">Die **Schaltflächen** " **SuperScript** " und "index" können nicht gleichzeitig ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="e59c9-116">The **Superscript** and **Subscript** buttons cannot both be selected.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e59c9-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e59c9-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e59c9-118">Schriftart Steuerelement-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e59c9-118">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="e59c9-119">**UI \_ fontverticalposition**</span><span class="sxs-lookup"><span data-stu-id="e59c9-119">**UI\_FONTVERTICALPOSITION**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition)
</dt> <dt>

[<span data-ttu-id="e59c9-120">Schriftart-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="e59c9-120">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 