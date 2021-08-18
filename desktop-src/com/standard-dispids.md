---
title: Standard-DISPIDS
description: Für die Steuerelementspezifikation wurde eine Reihe von Standard-Dispids definiert.
ms.assetid: f938b64f-5d45-40e7-ad02-665ce9c86a70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af35ce4e4cad884b54bb0982037721608364a0249d3be6dd566f3aac766bb1f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129782"
---
# <a name="standard-dispids"></a>Standard-DISPIDS

Für die Steuerelementspezifikation wurde eine Reihe von Standard-Dispids definiert.

## <a name="dispid_mousepointer"></a>DISPID \_ MOUSEPOINTER

Eigenschaft vom Typ integer.

``` syntax
#define DISPID_MOUSEPOINTER            -521
```

Die Mousepointer-Eigenschaft identifiziert Standardmaussymbole.



| Wert         | Beschreibung                                                                |
|---------------|----------------------------------------------------------------------------|
| 0<br/>  | (Standard) Die vom -Objekt bestimmte Form.<br/>                       |
| 1<br/>  | Pfeil<br/>                                                           |
| 2<br/>  | Cross (Cross-Hair-Zeiger)<br/>                                      |
| 3<br/>  | I Balken<br/>                                                          |
| 4<br/>  | Symbol (kleines Quadrat innerhalb eines Quadrats)<br/>                             |
| 5<br/>  | Größe (vier zeigende Pfeile, die nach Norden, Süden, Osten und Westen zeigen)<br/> |
| 6<br/>  | Größe NE SW (Doppelpfeil, der nach Nordosten und Südosten zeigt)<br/>      |
| 7<br/>  | Größe N S (Doppelpfeil, der nach Norden und Süden zeigt)<br/>                |
| 8<br/>  | Größe NW, SE<br/>                                                     |
| 9<br/>  | Größe E W (Doppelpfeil, der nach Osten und Westen zeigt)<br/>                  |
| 10<br/> | NACH-OBEN<br/>                                                        |
| 11<br/> | Sanduhr (Warten)<br/>                                                |
| 12<br/> | Keine Ablage<br/>                                                         |
| 13<br/> | Pfeil und Sanduhr<br/>                                             |
| 14<br/> | Pfeil und Fragezeichen<br/>                                         |
| 15<br/> | Größe aller<br/>                                                        |
| 99<br/> | Benutzerdefiniertes Symbol, das von der MouseIcon-Eigenschaft angegeben wird<br/>                 |



 

## <a name="dispid_mouseicon"></a>DISPID \_ MOUSEICON

Eigenschaft vom Typ "Bild".

``` syntax
#define DISPID_MOUSEICON               -522
```

## <a name="dispid_picture"></a>\_DISPID-BILD

Eigenschaft vom Typ "Bild".

``` syntax
#define DISPID_PICTURE                 -523
```

## <a name="dispid_valid"></a>DISPID \_ VALID

Wird verwendet, um zu bestimmen, ob das Steuerelement über gültige Daten verfügt oder nicht.

Eigenschaft vom Typ BOOL.

``` syntax
#define DISPID_VALID                   -524
```

## <a name="dispid_-ambient_palette"></a>DISPID \_ AMBIENT \_ PALETTE

Wird verwendet, um dem Steuerelement das Abrufen der HPAL des Containers zu ermöglichen. Wenn der Container eine Umgebungspalette bietet, ist dies die einzige Palette, die im Vordergrund realisiert werden kann. Steuerelemente, die ihre eigenen Paletten realisieren möchten, müssen dies im Hintergrund tun. Wenn vom Container keine Umgebungspalette bereitgestellt wird, kann das aktive Steuerelement seine Palette im Vordergrund erkennen. Die Palettenbehandlung wird unter Palettenverhalten für OLE-Steuerelemente im ActiveX SDK näher erläutert.

``` syntax
#define DISPID_AMBIENT_PALETTE         -726
```

 

 





