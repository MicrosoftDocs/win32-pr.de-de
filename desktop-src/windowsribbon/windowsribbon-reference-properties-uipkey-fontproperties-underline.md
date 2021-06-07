---
title: UI_PKEY_FontProperties_Underline
description: Identifiziert die \_ PKEY \_ FontProperties \_ Underline-Eigenschaft der Benutzeroberfläche.
ms.assetid: 88492558-ab19-4606-8fe0-5f100677b88a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 066027e5f62416667619937eea7dbe493a3ff279
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443781"
---
# <a name="ui_pkey_fontproperties_underline"></a><span data-ttu-id="40dca-103">UI \_ PKEY \_ FontProperties \_ Underline</span><span class="sxs-lookup"><span data-stu-id="40dca-103">UI\_PKEY\_FontProperties\_Underline</span></span>

<span data-ttu-id="40dca-104">Identifiziert die \_ PKEY \_ FontProperties \_ Underline-Eigenschaft der Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="40dca-104">Identifies the UI\_PKEY\_FontProperties\_Underline property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Underline
   shellPKey = UI_PKEY_FontProperties_Underline
   formatID = 00000305-7363-696e-8441798acf5aebb7
   propID = 305
   typeInfo
      type = UI_FONTUNDERLINE
```

## <a name="remarks"></a><span data-ttu-id="40dca-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="40dca-105">Remarks</span></span>

<span data-ttu-id="40dca-106">Ui \_ PKEY \_ FontProperties \_ Underline wird von einer Anwendung verwendet, um den Status der Schaltfläche **Unterstreichung** abzufragen.</span><span class="sxs-lookup"><span data-stu-id="40dca-106">UI\_PKEY\_FontProperties\_Underline is used by an application to query the state of the **Underline** button.</span></span>

<span data-ttu-id="40dca-107">Der Eigenschaftswert stammt aus der [**\_ FONTUNDERLINE-Enumeration der Benutzeroberfläche.**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline)</span><span class="sxs-lookup"><span data-stu-id="40dca-107">The property value is from the [**UI\_FONTUNDERLINE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline) enumeration.</span></span>

<span data-ttu-id="40dca-108">Standardwert: `UI_FONTUNDERLINE_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="40dca-108">The default value is `UI_FONTUNDERLINE_NOTSET`.</span></span>

<span data-ttu-id="40dca-109">Der folgende Screenshot zeigt die Schaltfläche **Unterstreichung** des [**Menübands FontControl**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="40dca-109">The following screen shot shows the **Underline** button of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![Screenshot des fontcontrol-Elements mit dem richfont-Attribut, das auf TRUE festgelegt ist.](images/markup/fontcontrol-underline.png)

<span data-ttu-id="40dca-111">In der folgenden Tabelle werden die Eigenschaften und das Benutzeroberflächenergebnis beschrieben.</span><span class="sxs-lookup"><span data-stu-id="40dca-111">The following table describes the properties and the UI result.</span></span>



|      <span data-ttu-id="40dca-112">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="40dca-112">Property</span></span>                   |       <span data-ttu-id="40dca-113">Ergebnis der Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="40dca-113">UI Result</span></span>                                                          |
|---------------------------------|--------------------------------------------------------------------------|
| `UI_FONTUNDERLINE_NOTAVAILABLE` | <span data-ttu-id="40dca-114">Die Schaltfläche **Unterstreichung** ist deaktiviert und kann nur von der Anwendung festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="40dca-114">**Underline** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTUNDERLINE_NOTSET`       | <span data-ttu-id="40dca-115">Die Schaltfläche **Unterstreichung** ist nicht ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="40dca-115">**Underline** button is not selected.</span></span>                                    |
| `UI_FONTUNDERLINE_SET`          | <span data-ttu-id="40dca-116">Die Schaltfläche **Unterstreichung** ist ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="40dca-116">**Underline** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="40dca-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="40dca-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40dca-118">Eigenschaften des Schriftartsteuerelements</span><span class="sxs-lookup"><span data-stu-id="40dca-118">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="40dca-119">**UI \_ FONTUNDERLINE**</span><span class="sxs-lookup"><span data-stu-id="40dca-119">**UI\_FONTUNDERLINE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline)
</dt> <dt>

[<span data-ttu-id="40dca-120">Schriftartsteuerelement</span><span class="sxs-lookup"><span data-stu-id="40dca-120">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 