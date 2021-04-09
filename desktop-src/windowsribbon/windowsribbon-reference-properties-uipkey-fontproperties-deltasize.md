---
title: UI_PKEY_FontProperties_DeltaSize
description: Bezeichnet die Eigenschaft "Benutzeroberflächen- \_ pkey \_ fontproperties \_ Delta size".
ms.assetid: 021a6c79-1d3e-47d2-9601-cdaa2e66a50a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c0046edf41fa61382d45a0662119d8fda237a0f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039006"
---
# <a name="ui_pkey_fontproperties_deltasize"></a><span data-ttu-id="d465c-103">UI- \_ pkey \_ fontproperties \_ Delta size</span><span class="sxs-lookup"><span data-stu-id="d465c-103">UI\_PKEY\_FontProperties\_DeltaSize</span></span>

<span data-ttu-id="d465c-104">Bezeichnet die Eigenschaft "Benutzeroberflächen- \_ pkey \_ fontproperties \_ Delta size".</span><span class="sxs-lookup"><span data-stu-id="d465c-104">Identifies the UI\_PKEY\_FontProperties\_DeltaSize property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_DeltaSize
   shellPKey = UI_PKEY_FontProperties_DeltaSize
   formatID = 00000309-7363-696e-8441798acf5aebb7
   propID = 313
   typeInfo
      type = UI_FONTDELTASIZE
```

## <a name="remarks"></a><span data-ttu-id="d465c-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d465c-105">Remarks</span></span>

<span data-ttu-id="d465c-106">UI \_ pkey \_ fontproperties \_ Delta Size wird von einer Anwendung in Fällen verwendet, in denen es nicht möglich ist, dass die Anwendung einen Wert für den **Schrift** Grad angibt, z. b. Wenn eine Textgröße mit Hetero gener Größe ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="d465c-106">UI\_PKEY\_FontProperties\_DeltaSize is used by an application in cases where it is not possible for the application to specify a value for **Font size**, such as when a run of heterogeneously sized text is selected.</span></span> <span data-ttu-id="d465c-107">Das Steuerelement **Schriftart Größe** ist auf Blank festgelegt, und die \_ Benutzeroberfläche pkey \_ fontproperties \_ Delta Size wird verwendet, um die Benutzerinteraktion mit den Schaltflächen für **Schriftart** Vergrößerung und **Schriftart verkleinern** zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="d465c-107">The **Font size** control is set to blank and UI\_PKEY\_FontProperties\_DeltaSize is used to capture user interaction with the **Font grow** and **Font shrink** buttons.</span></span>

<span data-ttu-id="d465c-108">UI \_ pkey \_ fontproperties \_ Delta size ist in [UI \_ pkey \_ fontproperties \_ changedproperties](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md)enthalten.</span><span class="sxs-lookup"><span data-stu-id="d465c-108">UI\_PKEY\_FontProperties\_DeltaSize is included in [UI\_PKEY\_FontProperties\_ChangedProperties](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md).</span></span>

<span data-ttu-id="d465c-109">Der folgende Screenshot zeigt die Schaltflächen **vergrößern** und **Verkleinern der Schriftart** des Menübands [**FontControl**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="d465c-109">The following screen shot shows the **Font grow** and **Font shrink** buttons of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![Screenshot der Schaltflächen zum Vergrößern der Schriftart und zum Verkleinern der Schriftart auf dem FontControl-Steuerelement.](images/markup/fontcontrol-incdec.png)

<span data-ttu-id="d465c-111">Die folgende Tabelle enthält eine Beschreibung der Eigenschaftswerte.</span><span class="sxs-lookup"><span data-stu-id="d465c-111">The following table describes the property values.</span></span>



|                           |                                 |
|---------------------------|---------------------------------|
| `UI_FONTDELTASIZE_GROW`   | <span data-ttu-id="d465c-112">Schaltfläche " **Schriftart vergrößern** " geklickt.</span><span class="sxs-lookup"><span data-stu-id="d465c-112">**Grow font** button clicked.</span></span>   |
| `UI_FONTDELTASIZE_SHRINK` | <span data-ttu-id="d465c-113">Schaltfläche zum **Verkleinern der Schriftart** .</span><span class="sxs-lookup"><span data-stu-id="d465c-113">**Shrink font** button clicked.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d465c-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d465c-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d465c-115">Schriftart Steuerelement-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d465c-115">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="d465c-116">**UI \_ fontdelta size**</span><span class="sxs-lookup"><span data-stu-id="d465c-116">**UI\_FONTDELTASIZE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontdeltasize)
</dt> <dt>

[<span data-ttu-id="d465c-117">Schriftart-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="d465c-117">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 