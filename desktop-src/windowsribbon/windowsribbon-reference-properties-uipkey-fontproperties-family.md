---
title: UI_PKEY_FontProperties_Family
description: Identifiziert die \_ PKEY \_ FontProperties-Eigenschaft der \_ Benutzeroberfläche.
ms.assetid: 95064588-9c14-401f-a86e-7b11e86faaf9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e0574ea4fb104cff29b58c8b1f649bd9287672acef677e3ea4cdc6ad5f91367
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118438659"
---
# <a name="ui_pkey_fontproperties_family"></a>UI \_ PKEY \_ FontProperties \_ Family

Identifiziert die \_ PKEY \_ FontProperties-Eigenschaft der \_ Benutzeroberfläche.

```
propertyDescription
   name = UI_PKEY_FontProperties_Family
   shellPKey = UI_PKEY_FontProperties_Family
   formatID = 00000301-7363-696e-8441798acf5aebb7
   propID = 301
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Hinweise

Die \_ PKEY \_ FontProperties-Familie der Benutzeroberfläche wird von einer Anwendung \_ verwendet, um den Wert des Dropdownkatalogs der **Schriftfamilie** abzufragen.

Der Wert der \_ Ui-PKEY \_ FontProperties-Familie \_ entspricht einem [Windows GDI-Schriftartfamiliennamen,](../gdi/font-families.md) der mit der [EnumFontFamilies-Funktion](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) oder [der EnumFontFamiliesEx-Funktion](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa)abgerufen wurde.

Der Standardwert ist eine leere Zeichenfolge.

Wenn eine leere Zeichenfolge für den Wert für die \_ Ui PKEY \_ FontProperties Family angegeben \_ wird, wird die Schriftartauswahl gelöscht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eigenschaften des Schriftartsteuerelements](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[Schriftartsteuerelement](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 