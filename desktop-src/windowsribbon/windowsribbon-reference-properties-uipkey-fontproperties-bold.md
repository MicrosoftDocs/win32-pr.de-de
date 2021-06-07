---
title: UI_PKEY_FontProperties_Bold
description: Identifiziert die \_ PKEY \_ FontProperties \_ Bold-Eigenschaft der Benutzeroberfläche.
ms.assetid: 9d33142a-bd63-423e-ba77-083c86bce1e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68800d3cfed72382f3576edfc01272c82b46c825
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444381"
---
# <a name="ui_pkey_fontproperties_bold"></a><span data-ttu-id="bafef-103">UI \_ PKEY \_ FontProperties \_ Bold</span><span class="sxs-lookup"><span data-stu-id="bafef-103">UI\_PKEY\_FontProperties\_Bold</span></span>

<span data-ttu-id="bafef-104">Identifiziert die \_ PKEY \_ FontProperties \_ Bold-Eigenschaft der Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="bafef-104">Identifies the UI\_PKEY\_FontProperties\_Bold property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Bold
   shellPKey = UI_PKEY_FontProperties_Bold
   formatID = 00000303-7363-696e-8441798acf5aebb7
   propID = 303
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a><span data-ttu-id="bafef-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bafef-105">Remarks</span></span>

<span data-ttu-id="bafef-106">Ui \_ PKEY \_ FontProperties \_ Bold wird von einer Anwendung verwendet, um den Zustand der Schaltfläche **Bold** abzufragen.</span><span class="sxs-lookup"><span data-stu-id="bafef-106">UI\_PKEY\_FontProperties\_Bold is used by an application to query the state of the **Bold** button.</span></span>

<span data-ttu-id="bafef-107">Der Eigenschaftswert stammt aus der [**\_ FONTPROPERTIES-Enumeration der Benutzeroberfläche.**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)</span><span class="sxs-lookup"><span data-stu-id="bafef-107">The property value is from the [**UI\_FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) enumeration.</span></span>

<span data-ttu-id="bafef-108">Standardwert: `UI_FONTPROPERTIES_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="bafef-108">The default value is `UI_FONTPROPERTIES_NOTSET`.</span></span>

<span data-ttu-id="bafef-109">In der folgenden Tabelle werden die Eigenschaften und das Benutzeroberflächenergebnis beschrieben.</span><span class="sxs-lookup"><span data-stu-id="bafef-109">The following table describes the properties and the UI result.</span></span>



|      <span data-ttu-id="bafef-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bafef-110">Property</span></span>                    |    <span data-ttu-id="bafef-111">Ergebnis der Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="bafef-111">UI Result</span></span>                                                        |
|----------------------------------|---------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | <span data-ttu-id="bafef-112">**Die** Schaltfläche Fett ist deaktiviert und kann nur von der Anwendung festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="bafef-112">**Bold** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTPROPERTIES_NOTSET`       | <span data-ttu-id="bafef-113">**Die** Schaltfläche Fett ist nicht ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="bafef-113">**Bold** button is not selected.</span></span>                                    |
| `UI_FONTPROPERTIES_SET`          | <span data-ttu-id="bafef-114">**Die** Schaltfläche Fett ist ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="bafef-114">**Bold** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="bafef-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bafef-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bafef-116">Eigenschaften des Schriftartsteuerelements</span><span class="sxs-lookup"><span data-stu-id="bafef-116">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="bafef-117">**UI \_ FONTPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="bafef-117">**UI\_FONTPROPERTIES**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[<span data-ttu-id="bafef-118">Schriftartsteuerelement</span><span class="sxs-lookup"><span data-stu-id="bafef-118">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 