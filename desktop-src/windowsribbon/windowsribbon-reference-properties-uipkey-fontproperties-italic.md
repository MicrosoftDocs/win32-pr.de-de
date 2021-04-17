---
title: UI_PKEY_FontProperties_Italic
description: Bezeichnet die Eigenschaft für die Eigenschaft "Benutzeroberflächen- \_ pkey \_ fontproperties" \_ .
ms.assetid: 53edd88e-ed7e-4385-9fd9-bfa90be348cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00825807c57632b1bbea69c47bc9b90d705efa94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390458"
---
# <a name="ui_pkey_fontproperties_italic"></a><span data-ttu-id="3d631-103">UI \_ pkey \_ fontproperties \_ kursiv</span><span class="sxs-lookup"><span data-stu-id="3d631-103">UI\_PKEY\_FontProperties\_Italic</span></span>

<span data-ttu-id="3d631-104">Bezeichnet die Eigenschaft für die Eigenschaft "Benutzeroberflächen- \_ pkey \_ fontproperties" \_ .</span><span class="sxs-lookup"><span data-stu-id="3d631-104">Identifies the UI\_PKEY\_FontProperties\_Italic property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Italic
   shellPKey = UI_PKEY_FontProperties_Italic
   formatID = 00000304-7363-696e-8441798acf5aebb7
   propID = 304
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a><span data-ttu-id="3d631-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d631-105">Remarks</span></span>

<span data-ttu-id="3d631-106">UI \_ pkey \_ fontproperties \_ Italic wird von einer Anwendung verwendet, um den Zustand der **kursiv** Schaltfläche abzufragen.</span><span class="sxs-lookup"><span data-stu-id="3d631-106">UI\_PKEY\_FontProperties\_Italic is used by an application to query the state of the **Italic** button.</span></span>

<span data-ttu-id="3d631-107">Der Eigenschafts Wert ist aus der [**UI \_ fontproperties**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="3d631-107">The property value is from the [**UI\_FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) enumeration.</span></span>

<span data-ttu-id="3d631-108">Der Standardwert ist `UI_FONTPROPERTIES_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="3d631-108">The default value is `UI_FONTPROPERTIES_NOTSET`.</span></span>

<span data-ttu-id="3d631-109">In der folgenden Tabelle werden die Eigenschaften und das Benutzeroberflächen Ergebnis beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3d631-109">The following table describes the properties and the UI result.</span></span>



|                                  |                                                                       |
|----------------------------------|-----------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | <span data-ttu-id="3d631-110">Die Schaltfläche " **kursiv** " ist deaktiviert und kann nur von der Anwendung festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3d631-110">**Italic** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTPROPERTIES_NOTSET`       | <span data-ttu-id="3d631-111">Die Schaltfläche " **kursiv** " ist nicht ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="3d631-111">**Italic** button is not selected.</span></span>                                    |
| `UI_FONTPROPERTIES_SET`          | <span data-ttu-id="3d631-112">Die Schaltfläche **kursiv** formatiert ist ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="3d631-112">**Italic** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="3d631-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3d631-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d631-114">Schriftart Steuerelement-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3d631-114">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="3d631-115">**UI- \_ fontproperties**</span><span class="sxs-lookup"><span data-stu-id="3d631-115">**UI\_FONTPROPERTIES**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[<span data-ttu-id="3d631-116">Schriftart-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="3d631-116">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 