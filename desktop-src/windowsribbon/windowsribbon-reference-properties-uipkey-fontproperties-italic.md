---
title: UI_PKEY_FontProperties_Italic
description: Identifiziert die \_ italische PKEY \_ FontProperties-Eigenschaft der \_ Benutzeroberfläche.
ms.assetid: 53edd88e-ed7e-4385-9fd9-bfa90be348cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d0dfa07b5112e91d8c25a4ff8c4f31175adf9b7
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443811"
---
# <a name="ui_pkey_fontproperties_italic"></a><span data-ttu-id="dad07-103">UI \_ PKEY \_ FontProperties \_ Italic</span><span class="sxs-lookup"><span data-stu-id="dad07-103">UI\_PKEY\_FontProperties\_Italic</span></span>

<span data-ttu-id="dad07-104">Identifiziert die \_ italische PKEY \_ FontProperties-Eigenschaft der \_ Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="dad07-104">Identifies the UI\_PKEY\_FontProperties\_Italic property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Italic
   shellPKey = UI_PKEY_FontProperties_Italic
   formatID = 00000304-7363-696e-8441798acf5aebb7
   propID = 304
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a><span data-ttu-id="dad07-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dad07-105">Remarks</span></span>

<span data-ttu-id="dad07-106">Ui \_ PKEY \_ FontProperties \_ Italic wird von einer Anwendung verwendet, um den Zustand der **Italic-Schaltfläche** abzufragen.</span><span class="sxs-lookup"><span data-stu-id="dad07-106">UI\_PKEY\_FontProperties\_Italic is used by an application to query the state of the **Italic** button.</span></span>

<span data-ttu-id="dad07-107">Der Eigenschaftswert stammt aus der [**\_ FONTPROPERTIES-Enumeration der Benutzeroberfläche.**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)</span><span class="sxs-lookup"><span data-stu-id="dad07-107">The property value is from the [**UI\_FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) enumeration.</span></span>

<span data-ttu-id="dad07-108">Standardwert: `UI_FONTPROPERTIES_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="dad07-108">The default value is `UI_FONTPROPERTIES_NOTSET`.</span></span>

<span data-ttu-id="dad07-109">In der folgenden Tabelle werden die Eigenschaften und das Benutzeroberflächenergebnis beschrieben.</span><span class="sxs-lookup"><span data-stu-id="dad07-109">The following table describes the properties and the UI result.</span></span>



|    <span data-ttu-id="dad07-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="dad07-110">Property</span></span>                      |       <span data-ttu-id="dad07-111">Ergebnis der Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="dad07-111">UI Result</span></span>                                                       |
|----------------------------------|-----------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | <span data-ttu-id="dad07-112">**Die italische** Schaltfläche ist deaktiviert und kann nur von der Anwendung festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="dad07-112">**Italic** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTPROPERTIES_NOTSET`       | <span data-ttu-id="dad07-113">**Die italische** Schaltfläche ist nicht ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="dad07-113">**Italic** button is not selected.</span></span>                                    |
| `UI_FONTPROPERTIES_SET`          | <span data-ttu-id="dad07-114">**Die italische** Schaltfläche ist ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="dad07-114">**Italic** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="dad07-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dad07-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dad07-116">Eigenschaften des Schriftartsteuerelements</span><span class="sxs-lookup"><span data-stu-id="dad07-116">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="dad07-117">**UI \_ FONTPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="dad07-117">**UI\_FONTPROPERTIES**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[<span data-ttu-id="dad07-118">Schriftartsteuerelement</span><span class="sxs-lookup"><span data-stu-id="dad07-118">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 