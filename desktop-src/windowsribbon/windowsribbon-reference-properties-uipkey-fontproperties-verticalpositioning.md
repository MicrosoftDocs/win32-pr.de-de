---
title: UI_PKEY_FontProperties_VerticalPositioning
description: Identifiziert die \_ PKEY \_ FontProperties \_ VerticalPositioning-Eigenschaft der Benutzeroberfläche.
ms.assetid: a92f845e-b0fc-4e23-9d06-ca16d2becf0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 954b01ff3271b9f74fac2c130c697a70e910fc93
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444301"
---
# <a name="ui_pkey_fontproperties_verticalpositioning"></a><span data-ttu-id="2eaa6-103">UI \_ PKEY \_ FontProperties \_ VerticalPositioning</span><span class="sxs-lookup"><span data-stu-id="2eaa6-103">UI\_PKEY\_FontProperties\_VerticalPositioning</span></span>

<span data-ttu-id="2eaa6-104">Identifiziert die \_ PKEY \_ FontProperties \_ VerticalPositioning-Eigenschaft der Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="2eaa6-104">Identifies the UI\_PKEY\_FontProperties\_VerticalPositioning property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_VerticalPositioning
   shellPKey = UI_PKEY_FontProperties_VerticalPositioning
   formatID = 00000307-7363-696e-8441798acf5aebb7
   propID = 307
   typeInfo
      type = UI_FONTVERTICALPOSITION
```

## <a name="remarks"></a><span data-ttu-id="2eaa6-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2eaa6-105">Remarks</span></span>

<span data-ttu-id="2eaa6-106">Ui \_ PKEY \_ FontProperties \_ VerticalPositioning wird von einer Anwendung verwendet, um den Wert der **Steuerelemente Superscript** und **Subscript** abzufragen.</span><span class="sxs-lookup"><span data-stu-id="2eaa6-106">UI\_PKEY\_FontProperties\_VerticalPositioning is used by an application to query the value of the **Superscript** and **Subscript** controls.</span></span>

<span data-ttu-id="2eaa6-107">Der Eigenschaftswert stammt aus der [**\_ FONTVERTICALPOSITION-Enumeration der Benutzeroberfläche.**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition)</span><span class="sxs-lookup"><span data-stu-id="2eaa6-107">The property value is from the [**UI\_FONTVERTICALPOSITION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition) enumeration.</span></span>

<span data-ttu-id="2eaa6-108">Standardwert: `UI_FONTVERTICALPOSITION_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="2eaa6-108">The default value is `UI_FONTVERTICALPOSITION_NOTSET`.</span></span>

<span data-ttu-id="2eaa6-109">Der folgende Screenshot zeigt die Schaltflächen **Superscript** und **Subscript** des Menübands [**FontControl**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="2eaa6-109">The following screen shot shows the **Superscript** and **Subscript** buttons of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![Screenshot des fontcontrol-Elements mit dem richfont-Attribut, das auf TRUE festgelegt ist.](images/markup/fontcontrol-subsuper.png)

<span data-ttu-id="2eaa6-111">In der folgenden Tabelle werden die Eigenschaften und das Benutzeroberflächenergebnis beschrieben.</span><span class="sxs-lookup"><span data-stu-id="2eaa6-111">The following table describes the properties and the UI result.</span></span>



|     <span data-ttu-id="2eaa6-112">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2eaa6-112">Property</span></span>                           |          <span data-ttu-id="2eaa6-113">Ergebnis der Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="2eaa6-113">UI Result</span></span>                                                                             |
|----------------------------------------|------------------------------------------------------------------------------------------------|
| `UI_FONTVERTICALPOSITION_NOTAVAILABLE` | <span data-ttu-id="2eaa6-114">Die Schaltflächen **"Superscript"** und **"Subscript"** sind deaktiviert und können nur von der Anwendung festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="2eaa6-114">**Superscript** and **Subscript** buttons are disabled and can only be set by the application.</span></span> |
| `UI_FONTVERTICALPOSITION_NOTSET`       | <span data-ttu-id="2eaa6-115">**Schaltflächen "Superscript"** und **"Subscript"** sind nicht ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="2eaa6-115">**Superscript** and **Subscript** buttons are not selected.</span></span>                                    |
| `UI_FONTVERTICALPOSITION_SUPERSCRIPT`  | <span data-ttu-id="2eaa6-116">Die Schaltfläche **"Superscript"** ist ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="2eaa6-116">**Superscript** button is selected.</span></span>                                                            |
| `UI_FONTVERTICALPOSITION_SUBSCRIPT`    | <span data-ttu-id="2eaa6-117">Die Schaltfläche **"Tiefgestellt"** ist ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="2eaa6-117">**Subscript** button is selected.</span></span>                                                              |



 

> [!Note]  
> <span data-ttu-id="2eaa6-118">Die Schaltflächen **Superscript** und **Subscript** können nicht beide ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="2eaa6-118">The **Superscript** and **Subscript** buttons cannot both be selected.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="2eaa6-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2eaa6-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2eaa6-120">Eigenschaften des Schriftartsteuerelements</span><span class="sxs-lookup"><span data-stu-id="2eaa6-120">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="2eaa6-121">**UI \_ FONTVERTICALPOSITION**</span><span class="sxs-lookup"><span data-stu-id="2eaa6-121">**UI\_FONTVERTICALPOSITION**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition)
</dt> <dt>

[<span data-ttu-id="2eaa6-122">Schriftartsteuerelement</span><span class="sxs-lookup"><span data-stu-id="2eaa6-122">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 