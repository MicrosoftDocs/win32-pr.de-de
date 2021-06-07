---
title: UI_PKEY_FontProperties_DeltaSize
description: Identifiziert die \_ PKEY \_ FontProperties \_ DeltaSize-Eigenschaft der Benutzeroberfläche.
ms.assetid: 021a6c79-1d3e-47d2-9601-cdaa2e66a50a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67778a710de8f69e0aea1134c12fb9ee3ebe0133
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444391"
---
# <a name="ui_pkey_fontproperties_deltasize"></a><span data-ttu-id="23757-103">UI \_ PKEY \_ FontProperties \_ DeltaSize</span><span class="sxs-lookup"><span data-stu-id="23757-103">UI\_PKEY\_FontProperties\_DeltaSize</span></span>

<span data-ttu-id="23757-104">Identifiziert die \_ PKEY \_ FontProperties \_ DeltaSize-Eigenschaft der Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="23757-104">Identifies the UI\_PKEY\_FontProperties\_DeltaSize property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_DeltaSize
   shellPKey = UI_PKEY_FontProperties_DeltaSize
   formatID = 00000309-7363-696e-8441798acf5aebb7
   propID = 313
   typeInfo
      type = UI_FONTDELTASIZE
```

## <a name="remarks"></a><span data-ttu-id="23757-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="23757-105">Remarks</span></span>

<span data-ttu-id="23757-106">Ui \_ PKEY \_ FontProperties \_ DeltaSize wird von einer Anwendung in Fällen verwendet, in denen es für die Anwendung nicht möglich ist, einen Wert für **Schriftgrad** anzugeben, z. B. wenn eine Ausführung von text heterogener Größe ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="23757-106">UI\_PKEY\_FontProperties\_DeltaSize is used by an application in cases where it is not possible for the application to specify a value for **Font size**, such as when a run of heterogeneously sized text is selected.</span></span> <span data-ttu-id="23757-107">Das **Steuerelement Schriftgrad** ist auf blank festgelegt, und die Ui \_ PKEY \_ FontProperties \_ DeltaSize wird verwendet, um Benutzerinteraktionen mit den Schaltflächen **Schriftvergrößerung** und **Schriftver verkleinern** zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="23757-107">The **Font size** control is set to blank and UI\_PKEY\_FontProperties\_DeltaSize is used to capture user interaction with the **Font grow** and **Font shrink** buttons.</span></span>

<span data-ttu-id="23757-108">Ui \_ PKEY \_ FontProperties \_ DeltaSize ist in [ui \_ PKEY \_ FontProperties \_ ChangedProperties](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md)enthalten.</span><span class="sxs-lookup"><span data-stu-id="23757-108">UI\_PKEY\_FontProperties\_DeltaSize is included in [UI\_PKEY\_FontProperties\_ChangedProperties](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md).</span></span>

<span data-ttu-id="23757-109">Der folgende Screenshot zeigt die Schaltflächen **Schriftgröße** und **Schrift verkleinern** des Menübands [**FontControl**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="23757-109">The following screen shot shows the **Font grow** and **Font shrink** buttons of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![Screenshot der Schaltflächen "Schrift vergrößern" und "Schrift verkleinern" auf dem fontcontrol.)](images/markup/fontcontrol-incdec.png)

<span data-ttu-id="23757-111">Die folgende Tabelle enthält eine Beschreibung der Eigenschaftswerte.</span><span class="sxs-lookup"><span data-stu-id="23757-111">The following table describes the property values.</span></span>



|     <span data-ttu-id="23757-112">Wert</span><span class="sxs-lookup"><span data-stu-id="23757-112">Value</span></span>                 |  <span data-ttu-id="23757-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="23757-113">Description</span></span>                    |
|---------------------------|---------------------------------|
| `UI_FONTDELTASIZE_GROW`   | <span data-ttu-id="23757-114">Auf die Schaltfläche **"Schriftart** vergrößern" geklickt.</span><span class="sxs-lookup"><span data-stu-id="23757-114">**Grow font** button clicked.</span></span>   |
| `UI_FONTDELTASIZE_SHRINK` | <span data-ttu-id="23757-115">Auf die Schaltfläche **Schriftart verkleinern** geklickt.</span><span class="sxs-lookup"><span data-stu-id="23757-115">**Shrink font** button clicked.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="23757-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="23757-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23757-117">Eigenschaften des Schriftartsteuerelements</span><span class="sxs-lookup"><span data-stu-id="23757-117">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="23757-118">**UI \_ FONTDELTASIZE**</span><span class="sxs-lookup"><span data-stu-id="23757-118">**UI\_FONTDELTASIZE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontdeltasize)
</dt> <dt>

[<span data-ttu-id="23757-119">Schriftartsteuerelement</span><span class="sxs-lookup"><span data-stu-id="23757-119">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 