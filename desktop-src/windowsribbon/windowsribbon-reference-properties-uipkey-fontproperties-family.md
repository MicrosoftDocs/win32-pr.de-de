---
title: UI_PKEY_FontProperties_Family
description: Bezeichnet die Eigenschaft der Eigenschaft "UI \_ pkey \_ fontproperties" \_ .
ms.assetid: 95064588-9c14-401f-a86e-7b11e86faaf9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a7183e51105a397f14154639512ca11f7c03d44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338667"
---
# <a name="ui_pkey_fontproperties_family"></a><span data-ttu-id="ce908-103">UI \_ pkey \_ fontproperties- \_ Familie</span><span class="sxs-lookup"><span data-stu-id="ce908-103">UI\_PKEY\_FontProperties\_Family</span></span>

<span data-ttu-id="ce908-104">Bezeichnet die Eigenschaft der Eigenschaft "UI \_ pkey \_ fontproperties" \_ .</span><span class="sxs-lookup"><span data-stu-id="ce908-104">Identifies the UI\_PKEY\_FontProperties\_Family property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Family
   shellPKey = UI_PKEY_FontProperties_Family
   formatID = 00000301-7363-696e-8441798acf5aebb7
   propID = 301
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a><span data-ttu-id="ce908-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce908-105">Remarks</span></span>

<span data-ttu-id="ce908-106">\_Die UI pkey \_ fontproperties \_ -Familie wird von einer Anwendung verwendet, um den Wert des Dropdown Katalogs der **Schriftart Familie** abzufragen.</span><span class="sxs-lookup"><span data-stu-id="ce908-106">UI\_PKEY\_FontProperties\_Family is used by an application to query the value of the **Font family** drop-down gallery.</span></span>

<span data-ttu-id="ce908-107">Der Wert der UI \_ pkey \_ fontproperties- \_ Familie stimmt mit dem Namen einer [Windows GDI-Schriftart](../gdi/font-families.md) Familie überein, die mit der [Funktion EnumFontFamilies](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) oder der [Funktion enumfontfamiliesex](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa)abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="ce908-107">The value of UI\_PKEY\_FontProperties\_Family matches a [Windows GDI Font Families](../gdi/font-families.md) name retrieved with the [EnumFontFamilies function](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) or [EnumFontFamiliesEx function](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa).</span></span>

<span data-ttu-id="ce908-108">Der Standardwert ist eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="ce908-108">The default value is an empty string.</span></span>

<span data-ttu-id="ce908-109">Wenn für den Wert der UI pkey fontproperties-Familie eine leere Zeichenfolge angegeben wird \_ \_ \_ , wird die Schriftart Auswahl gelöscht.</span><span class="sxs-lookup"><span data-stu-id="ce908-109">If an empty string is supplied for the value for UI\_PKEY\_FontProperties\_Family, then the font selection is cleared.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce908-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ce908-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce908-111">Schriftart Steuerelement-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ce908-111">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="ce908-112">Schriftart-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="ce908-112">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 