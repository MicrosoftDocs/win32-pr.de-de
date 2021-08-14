---
title: UI_PKEY_FontProperties_Family
description: Identifiziert die \_ PKEY \_ FontProperties \_ Family-Eigenschaft der Benutzeroberfläche.
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
# <a name="ui_pkey_fontproperties_family"></a>\_ \_ PKEY-Schriftarteigenschaftenfamilie der \_ Benutzeroberfläche

Identifiziert die \_ PKEY \_ FontProperties \_ Family-Eigenschaft der Benutzeroberfläche.

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

Die \_ PKEY FontProperties-Familie der Benutzeroberfläche wird von einer Anwendung verwendet, um den Wert des Dropdownkatalogs der \_ \_ Schriftfamilie abfragt. 

Der Wert der PKEY FontProperties-Familie der Benutzeroberfläche entspricht einem Windows GDI-Schriftartfamiliennamen, der mit der \_ \_ \_ [EnumFontFamilies-Funktion](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) oder der [EnumFontFamiliesEx-Funktion](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa) [](../gdi/font-families.md) abgerufen wird.

Der Standardwert ist eine leere Zeichenfolge.

Wenn für den Wert für die \_ PKEY FontProperties-Familie der Benutzeroberfläche eine leere Zeichenfolge angegeben wird, wird die \_ \_ Schriftartauswahl nicht mehr angezeigt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eigenschaften des Schriftart-Steuerelements](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[Schriftart-Steuerelement](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 