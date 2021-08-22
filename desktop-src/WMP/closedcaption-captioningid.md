---
title: ClosedCaption.captioningID
description: Die captioningID-Eigenschaft gibt den Namen des Elements an, das die Beschriftung angibt oder abruft.
ms.assetid: 99d4aae3-485f-4c86-9130-101b1ca968e9
keywords:
- ClosedCaption.captioningID Windows Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.captioningID
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1da667e5479cc33312375920c1d573f0e2c19607b2399ff6f4fe34b130ca61e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118580988"
---
# <a name="closedcaptioncaptioningid"></a>ClosedCaption.captioningID

Die **captioningID-Eigenschaft** gibt den Namen des Elements an, das die Beschriftung angibt oder abruft.

``` syntax
player.closedCaption.captioningID
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine Zeichenfolge mit **Lese-/Schreibzugriff.**

## <a name="remarks"></a>Hinweise

Der angegebene Elementname kann ein beliebiges HTML-Element auf der Webseite sein, solange es das innerHTML-Attribut unterstützt. Wenn die Webseite mehrere Frames enthält, kann der Elementname nur auf ein Element im selben Frame wie das Player-Steuerelement verweisen.

**Windows Media Player 10 Mobile:** Diese Eigenschaft ist schreibgeschützt und gibt immer eine leere Zeichenfolge zurück.

## <a name="examples"></a>Beispiele

Im folgenden Microsoft JScript beispiel wird *ClosedCaption verwendet.* **captioningID** zum Auswählen des Bereichs einer Webseite, der zum Anzeigen von Untertiteln verwendet wird. Es wurden zwei HTML-DIV-Elemente mit ID = CC1 bzw. ID = CC2 erstellt. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


```JScript
<!-- Create two HTML BUTTON elements to allow the user to choose a display region. -->
<INPUT TYPE = "BUTTON"  NAME = "SET1"  VALUE = "Move Caption to CC1"
       OnClick = "
           /* Clear the caption text from the other DIV */
           CC2.innerHTML = 'This is the CC2 DIV';

           /* Show the captions in the DIV named CC1. */ 
           Player.ClosedCaption.captioningID = 'CC1';
          ">

<INPUT TYPE = "BUTTON" NAME = "SET2" VALUE = "Move Caption to CC2"
       OnClick = "
           /* Clear the caption text from the other DIV */
           CC1.innerHTML = 'This is the CC1 DIV';

           /* Show the captions in the DIV named CC2. */
           Player.ClosedCaption.captioningID = 'CC2';
          ">

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Hinzufügen von Untertiteln zu digitalen Medien**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**ClosedCaption-Objekt**](closedcaption-object.md)
</dt> </dl>

 

 





