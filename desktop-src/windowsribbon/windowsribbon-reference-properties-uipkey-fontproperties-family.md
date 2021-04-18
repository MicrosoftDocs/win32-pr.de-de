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
# <a name="ui_pkey_fontproperties_family"></a>UI \_ pkey \_ fontproperties- \_ Familie

Bezeichnet die Eigenschaft der Eigenschaft "UI \_ pkey \_ fontproperties" \_ .

```
propertyDescription
   name = UI_PKEY_FontProperties_Family
   shellPKey = UI_PKEY_FontProperties_Family
   formatID = 00000301-7363-696e-8441798acf5aebb7
   propID = 301
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Bemerkungen

\_Die UI pkey \_ fontproperties \_ -Familie wird von einer Anwendung verwendet, um den Wert des Dropdown Katalogs der **Schriftart Familie** abzufragen.

Der Wert der UI \_ pkey \_ fontproperties- \_ Familie stimmt mit dem Namen einer [Windows GDI-Schriftart](../gdi/font-families.md) Familie überein, die mit der [Funktion EnumFontFamilies](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) oder der [Funktion enumfontfamiliesex](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa)abgerufen wurde.

Der Standardwert ist eine leere Zeichenfolge.

Wenn für den Wert der UI pkey fontproperties-Familie eine leere Zeichenfolge angegeben wird \_ \_ \_ , wird die Schriftart Auswahl gelöscht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schriftart Steuerelement-Eigenschaften](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[Schriftart-Steuerelement](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 