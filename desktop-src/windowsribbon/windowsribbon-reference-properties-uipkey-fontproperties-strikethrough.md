---
title: UI_PKEY_FontProperties_Strikethrough
description: Identifiziert die \_ PKEY \_ FontProperties \_ Strikethrough-Eigenschaft der Benutzeroberfläche.
ms.assetid: 18ee653d-db01-4615-a85d-ad4ac6a0f422
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b684704fdd90a8dd1b88b14db2b52540b15fccb
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443791"
---
# <a name="ui_pkey_fontproperties_strikethrough"></a><span data-ttu-id="c4473-103">UI \_ PKEY \_ FontProperties \_ Strikethrough</span><span class="sxs-lookup"><span data-stu-id="c4473-103">UI\_PKEY\_FontProperties\_Strikethrough</span></span>

<span data-ttu-id="c4473-104">Identifiziert die \_ PKEY \_ FontProperties \_ Strikethrough-Eigenschaft der Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="c4473-104">Identifies the UI\_PKEY\_FontProperties\_Strikethrough property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Strikethrough
   shellPKey = UI_PKEY_FontProperties_Strikethrough
   formatID = 00000306-7363-696e-8441798acf5aebb7
   propID = 306
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a><span data-ttu-id="c4473-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c4473-105">Remarks</span></span>

<span data-ttu-id="c4473-106">PKEY FontProperties Strikethrough der Benutzeroberfläche wird von einer Anwendung verwendet, um den Zustand der \_ \_ Schaltfläche \_ **Durchgestreichen** abfragt.</span><span class="sxs-lookup"><span data-stu-id="c4473-106">UI\_PKEY\_FontProperties\_Strikethrough is used by an application to query the state of the **Strikethrough** button.</span></span>

<span data-ttu-id="c4473-107">Der -Eigenschaftswert ist aus der [**\_ FONTPROPERTIES-Enumeration der Benutzeroberfläche.**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)</span><span class="sxs-lookup"><span data-stu-id="c4473-107">The property value is from the [**UI\_FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) enumeration.</span></span>

<span data-ttu-id="c4473-108">Standardwert: `UI_FONTPROPERTIES_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="c4473-108">The default value is `UI_FONTPROPERTIES_NOTSET`.</span></span>

<span data-ttu-id="c4473-109">Der folgende Screenshot zeigt die Schaltfläche **Durchstreichen** des [**FontControl-Menübands.**](windowsribbon-element-fontcontrol.md)</span><span class="sxs-lookup"><span data-stu-id="c4473-109">The following screen shot shows the **Strikethrough** button of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![Screenshot des fontcontrol-Elements mit dem richfont-Attribut, das auf TRUE festgelegt ist.](images/markup/fontcontrol-strikethrough.png)

<span data-ttu-id="c4473-111">In der folgenden Tabelle werden die Eigenschaften und das Ergebnis der Benutzeroberfläche beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c4473-111">The following table describes the properties and the UI result.</span></span>



|   <span data-ttu-id="c4473-112">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c4473-112">Property</span></span>                       |    <span data-ttu-id="c4473-113">Ergebnis der Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="c4473-113">UI Result</span></span>                                                                 |
|----------------------------------|------------------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | <span data-ttu-id="c4473-114">**Die Schaltfläche** "Durchgestreichen" ist deaktiviert und kann nur von der Anwendung festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c4473-114">**Strikethrough** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTPROPERTIES_NOTSET`       | <span data-ttu-id="c4473-115">**Die Durchstreichschaltfläche** ist nicht ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="c4473-115">**Strikethrough** button is not selected.</span></span>                                    |
| `UI_FONTPROPERTIES_SET`          | <span data-ttu-id="c4473-116">**Die Schaltfläche Durchgestreichen** ist ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="c4473-116">**Strikethrough** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="c4473-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c4473-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4473-118">Eigenschaften des Schriftart-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="c4473-118">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="c4473-119">**SCHRIFTARTEIGENSCHAFTEN \_ DER BENUTZEROBERFLÄCHE**</span><span class="sxs-lookup"><span data-stu-id="c4473-119">**UI\_FONTPROPERTIES**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[<span data-ttu-id="c4473-120">Schriftart-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="c4473-120">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 