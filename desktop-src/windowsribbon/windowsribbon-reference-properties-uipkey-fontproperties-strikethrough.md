---
title: UI_PKEY_FontProperties_Strikethrough
description: Identifiziert die Eigenschaft "Benutzeroberflächen- \_ pkey- \_ fontproperties-Eigenschaften" \_ .
ms.assetid: 18ee653d-db01-4615-a85d-ad4ac6a0f422
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b07804a74671bb219b34b1c67580af083fd5c34c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390853"
---
# <a name="ui_pkey_fontproperties_strikethrough"></a><span data-ttu-id="d2464-103">UI- \_ pkey- \_ fontproperties \_ durchgestrichen</span><span class="sxs-lookup"><span data-stu-id="d2464-103">UI\_PKEY\_FontProperties\_Strikethrough</span></span>

<span data-ttu-id="d2464-104">Identifiziert die Eigenschaft "Benutzeroberflächen- \_ pkey- \_ fontproperties-Eigenschaften" \_ .</span><span class="sxs-lookup"><span data-stu-id="d2464-104">Identifies the UI\_PKEY\_FontProperties\_Strikethrough property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Strikethrough
   shellPKey = UI_PKEY_FontProperties_Strikethrough
   formatID = 00000306-7363-696e-8441798acf5aebb7
   propID = 306
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a><span data-ttu-id="d2464-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d2464-105">Remarks</span></span>

<span data-ttu-id="d2464-106">UI \_ pkey \_ fontproperties durchgestrichen \_ wird von einer Anwendung verwendet, um den Zustand der Schaltfläche **durch** gestrichen abzufragen.</span><span class="sxs-lookup"><span data-stu-id="d2464-106">UI\_PKEY\_FontProperties\_Strikethrough is used by an application to query the state of the **Strikethrough** button.</span></span>

<span data-ttu-id="d2464-107">Der Eigenschafts Wert ist aus der [**UI \_ fontproperties**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="d2464-107">The property value is from the [**UI\_FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) enumeration.</span></span>

<span data-ttu-id="d2464-108">Der Standardwert ist `UI_FONTPROPERTIES_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="d2464-108">The default value is `UI_FONTPROPERTIES_NOTSET`.</span></span>

<span data-ttu-id="d2464-109">Der folgende Screenshot zeigt die Schaltfläche **durch** gestrichen des Menübands [**FontControl**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="d2464-109">The following screen shot shows the **Strikethrough** button of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![Screenshot des FontControl-Elements, bei dem das richfont-Attribut auf "true" festgelegt ist.](images/markup/fontcontrol-strikethrough.png)

<span data-ttu-id="d2464-111">In der folgenden Tabelle werden die Eigenschaften und das Benutzeroberflächen Ergebnis beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d2464-111">The following table describes the properties and the UI result.</span></span>



|                                  |                                                                              |
|----------------------------------|------------------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | <span data-ttu-id="d2464-112">Die Schaltfläche " **durch** gestrichen" ist deaktiviert und kann nur von der Anwendung festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d2464-112">**Strikethrough** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTPROPERTIES_NOTSET`       | <span data-ttu-id="d2464-113">Die Schaltfläche " **durch** gestrichen" ist nicht ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="d2464-113">**Strikethrough** button is not selected.</span></span>                                    |
| `UI_FONTPROPERTIES_SET`          | <span data-ttu-id="d2464-114">Die Schaltfläche " **durch** gestrichen" ist ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="d2464-114">**Strikethrough** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="d2464-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d2464-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2464-116">Schriftart Steuerelement-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d2464-116">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="d2464-117">**UI- \_ fontproperties**</span><span class="sxs-lookup"><span data-stu-id="d2464-117">**UI\_FONTPROPERTIES**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[<span data-ttu-id="d2464-118">Schriftart-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="d2464-118">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 