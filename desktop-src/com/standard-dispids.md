---
title: Standard-DispIds
description: Es wurden eine Reihe von Standard-DISPIDs für die Steuerelement Spezifikation definiert.
ms.assetid: f938b64f-5d45-40e7-ad02-665ce9c86a70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657a7cd12ac92504bb5d63dcd486b6a45da47310
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341439"
---
# <a name="standard-dispids"></a>Standard-DispIds

Es wurden eine Reihe von Standard-DISPIDs für die Steuerelement Spezifikation definiert.

## <a name="dispid_mousepointer"></a>DISPID- \_ mouum Zeiger

Eigenschaft vom Typ Integer.

``` syntax
#define DISPID_MOUSEPOINTER            -521
```

Die MousePointer-Eigenschaft identifiziert Standard Maus Symbole.



| Wert         | BESCHREIBUNG                                                                |
|---------------|----------------------------------------------------------------------------|
| 0<br/>  | Vorgegebene Die vom-Objekt festgelegte Form.<br/>                       |
| 1<br/>  | Pfeil<br/>                                                           |
| 2<br/>  | Kreuz (Kreuz-Mauszeiger)<br/>                                      |
| 3<br/>  | I-Strahl<br/>                                                          |
| 4<br/>  | Symbol (kleines Quadrat innerhalb eines Quadrats)<br/>                             |
| 5<br/>  | Größe (vier-Spitze-Pfeil, der nach Nord, Süd, Ost und West zeigt)<br/> |
| 6<br/>  | Größe ne SW (doppelter Pfeil, der auf Nordost und Südwest zeigt)<br/>      |
| 7<br/>  | Größe N S (doppelter Pfeil, der nach Norden und Süden zeigt)<br/>                |
| 8<br/>  | Größe NW, SE<br/>                                                     |
| 9<br/>  | Größe E W (doppelter Pfeil, der nach Osten und Westen zeigt)<br/>                  |
| 10<br/> | NACH-OBEN<br/>                                                        |
| 11<br/> | Sanduhr (warten)<br/>                                                |
| 12<br/> | Kein Drop<br/>                                                         |
| 13<br/> | Pfeil und Sanduhr<br/>                                             |
| 14<br/> | Pfeil und Fragezeichen<br/>                                         |
| 15<br/> | Größe alle<br/>                                                        |
| 99<br/> | Durch die MouseIcon-Eigenschaft angegebenes benutzerdefiniertes Symbol<br/>                 |



 

## <a name="dispid_mouseicon"></a>DISPID \_ MouseIcon

-Eigenschaft des Typs "Bild".

``` syntax
#define DISPID_MOUSEICON               -522
```

## <a name="dispid_picture"></a>DISPID- \_ Bild

-Eigenschaft des Typs "Bild".

``` syntax
#define DISPID_PICTURE                 -523
```

## <a name="dispid_valid"></a>DISPID \_ gültig

Wird verwendet, um zu bestimmen, ob das Steuerelement über gültige Daten verfügt.

-Eigenschaft vom Typ bool.

``` syntax
#define DISPID_VALID                   -524
```

## <a name="dispid_-ambient_palette"></a>"DISPID \_ AMBIENT \_ Palette"

Wird verwendet, um dem Steuerelement zu ermöglichen, den hpal des Containers zu erhalten. Wenn der Container eine Ambient-Palette liefert, ist dies die einzige Palette, die möglicherweise im Vordergrund erkannt wird. Steuerelemente, die ihre eigenen Paletten erkennen möchten, müssen dies im Hintergrund tun. Wenn keine Ambient-Palette durch den Container bereitgestellt wird, kann das aktive Steuerelement seine Palette im Vordergrund erkennen. Die palettenbehandlung wird im Palette-Verhalten für OLE-Steuerelemente, die sich im ActiveX SDK befinden, ausführlicher erläutert.

``` syntax
#define DISPID_AMBIENT_PALETTE         -726
```

 

 





