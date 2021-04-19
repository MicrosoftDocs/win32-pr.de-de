---
title: UI_PKEY_FontProperties_Bold
description: Gibt die Eigenschaft "Bold Properties" der UI \_ pkey \_ fontproperties an \_ .
ms.assetid: 9d33142a-bd63-423e-ba77-083c86bce1e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dca8a58b9c5bfa51cfba8d80a477dafb744dfb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338482"
---
# <a name="ui_pkey_fontproperties_bold"></a><span data-ttu-id="bbe2d-103">UI- \_ pkey \_ fontproperties \_ Fett</span><span class="sxs-lookup"><span data-stu-id="bbe2d-103">UI\_PKEY\_FontProperties\_Bold</span></span>

<span data-ttu-id="bbe2d-104">Gibt die Eigenschaft "Bold Properties" der UI \_ pkey \_ fontproperties an \_ .</span><span class="sxs-lookup"><span data-stu-id="bbe2d-104">Identifies the UI\_PKEY\_FontProperties\_Bold property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Bold
   shellPKey = UI_PKEY_FontProperties_Bold
   formatID = 00000303-7363-696e-8441798acf5aebb7
   propID = 303
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a><span data-ttu-id="bbe2d-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bbe2d-105">Remarks</span></span>

<span data-ttu-id="bbe2d-106">UI \_ pkey \_ fontproperties \_ Bold wird von einer Anwendung verwendet, um den Status der **Fett** formatierten Schaltfläche abzufragen.</span><span class="sxs-lookup"><span data-stu-id="bbe2d-106">UI\_PKEY\_FontProperties\_Bold is used by an application to query the state of the **Bold** button.</span></span>

<span data-ttu-id="bbe2d-107">Der Eigenschafts Wert ist aus der [**UI \_ fontproperties**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="bbe2d-107">The property value is from the [**UI\_FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) enumeration.</span></span>

<span data-ttu-id="bbe2d-108">Der Standardwert ist `UI_FONTPROPERTIES_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="bbe2d-108">The default value is `UI_FONTPROPERTIES_NOTSET`.</span></span>

<span data-ttu-id="bbe2d-109">In der folgenden Tabelle werden die Eigenschaften und das Benutzeroberflächen Ergebnis beschrieben.</span><span class="sxs-lookup"><span data-stu-id="bbe2d-109">The following table describes the properties and the UI result.</span></span>



|                                  |                                                                     |
|----------------------------------|---------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | <span data-ttu-id="bbe2d-110">Die **Fett** formatierte Schaltfläche ist deaktiviert und kann nur von der Anwendung festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="bbe2d-110">**Bold** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTPROPERTIES_NOTSET`       | <span data-ttu-id="bbe2d-111">Die Schaltfläche " **Fett** " ist nicht ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="bbe2d-111">**Bold** button is not selected.</span></span>                                    |
| `UI_FONTPROPERTIES_SET`          | <span data-ttu-id="bbe2d-112">Die Schaltfläche **Fett** ist ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="bbe2d-112">**Bold** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="bbe2d-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bbe2d-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbe2d-114">Schriftart Steuerelement-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bbe2d-114">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="bbe2d-115">**UI- \_ fontproperties**</span><span class="sxs-lookup"><span data-stu-id="bbe2d-115">**UI\_FONTPROPERTIES**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[<span data-ttu-id="bbe2d-116">Schriftart-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="bbe2d-116">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 