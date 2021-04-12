---
title: UI_PKEY_FontProperties_Underline
description: Gibt die Eigenschaft "UI \_ pkey fontproperties-Unterstreichung" an \_ \_ .
ms.assetid: 88492558-ab19-4606-8fe0-5f100677b88a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 380c3fdadb636775f80b789a585c42ff2369234a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473588"
---
# <a name="ui_pkey_fontproperties_underline"></a><span data-ttu-id="52250-103">Benutzeroberflächen- \_ pkey \_ fontproperties unter \_ streichen</span><span class="sxs-lookup"><span data-stu-id="52250-103">UI\_PKEY\_FontProperties\_Underline</span></span>

<span data-ttu-id="52250-104">Gibt die Eigenschaft "UI \_ pkey fontproperties-Unterstreichung" an \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="52250-104">Identifies the UI\_PKEY\_FontProperties\_Underline property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Underline
   shellPKey = UI_PKEY_FontProperties_Underline
   formatID = 00000305-7363-696e-8441798acf5aebb7
   propID = 305
   typeInfo
      type = UI_FONTUNDERLINE
```

## <a name="remarks"></a><span data-ttu-id="52250-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52250-105">Remarks</span></span>

<span data-ttu-id="52250-106">\_Die Unterstreichung von UI pkey \_ fontproperties \_ wird von einer Anwendung verwendet, um den Zustand der Schaltfläche "unter **streichen** " abzufragen.</span><span class="sxs-lookup"><span data-stu-id="52250-106">UI\_PKEY\_FontProperties\_Underline is used by an application to query the state of the **Underline** button.</span></span>

<span data-ttu-id="52250-107">Der Eigenschafts Wert ist aus der [**UI \_ fontstreicht**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="52250-107">The property value is from the [**UI\_FONTUNDERLINE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline) enumeration.</span></span>

<span data-ttu-id="52250-108">Der Standardwert ist `UI_FONTUNDERLINE_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="52250-108">The default value is `UI_FONTUNDERLINE_NOTSET`.</span></span>

<span data-ttu-id="52250-109">Der folgende Screenshot zeigt die unter **Streichung** -Schaltfläche des Menübands [**FontControl**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="52250-109">The following screen shot shows the **Underline** button of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![Screenshot des FontControl-Elements, bei dem das richfont-Attribut auf "true" festgelegt ist.](images/markup/fontcontrol-underline.png)

<span data-ttu-id="52250-111">In der folgenden Tabelle werden die Eigenschaften und das Benutzeroberflächen Ergebnis beschrieben.</span><span class="sxs-lookup"><span data-stu-id="52250-111">The following table describes the properties and the UI result.</span></span>



|                                 |                                                                          |
|---------------------------------|--------------------------------------------------------------------------|
| `UI_FONTUNDERLINE_NOTAVAILABLE` | <span data-ttu-id="52250-112">Die Schaltfläche "unter **streichen** " ist deaktiviert und kann nur von der Anwendung festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="52250-112">**Underline** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTUNDERLINE_NOTSET`       | <span data-ttu-id="52250-113">Die Schaltfläche für unter **Streichung** ist nicht ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="52250-113">**Underline** button is not selected.</span></span>                                    |
| `UI_FONTUNDERLINE_SET`          | <span data-ttu-id="52250-114">Die Schaltfläche unter **Streichung** ist ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="52250-114">**Underline** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="52250-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="52250-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52250-116">Schriftart Steuerelement-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="52250-116">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="52250-117">**UI \_ fontunter Streichung**</span><span class="sxs-lookup"><span data-stu-id="52250-117">**UI\_FONTUNDERLINE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline)
</dt> <dt>

[<span data-ttu-id="52250-118">Schriftart-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="52250-118">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 