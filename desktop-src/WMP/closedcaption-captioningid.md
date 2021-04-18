---
title: Closedcaption. captioningid
description: Die captioningid-Eigenschaft gibt den Namen des Elements an, das die Untertitel anzeigt, oder ruft ihn ab.
ms.assetid: 99d4aae3-485f-4c86-9130-101b1ca968e9
keywords:
- Fenster "closedcaption. captioningid" Media Player
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
ms.openlocfilehash: faadae626dd5ac0314c4140e3f9d82ab645ef9b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365364"
---
# <a name="closedcaptioncaptioningid"></a>Closedcaption. captioningid

Die **captioningid** -Eigenschaft gibt den Namen des Elements an, das die Untertitel anzeigt, oder ruft ihn ab.

``` syntax
player.closedCaption.captioningID
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine Lese- **/schreibzeichenfolge**.

## <a name="remarks"></a>Bemerkungen

Der angegebene Elementname kann ein beliebiges HTML-Element auf der Webseite sein, solange es das innerHTML-Attribut unterstützt. Wenn die Webseite mehrere Frames enthält, kann der Elementname nur auf ein Element im gleichen Frame wie das Player-Steuerelement verweisen.

**Windows Media Player 10 Mobile:** Diese Eigenschaft ist schreibgeschützt und gibt immer eine leere Zeichenfolge zurück.

## <a name="examples"></a>Beispiele

Im folgenden Microsoft JScript-Beispiel wird *closedcaption* verwendet. **captioningid** zum Auswählen des Bereichs einer Webseite, in der Beschriftungen angezeigt werden. Es wurden zwei HTML-div-Elemente mit ID = CC1 bzw. ID = cc2 erstellt. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Hinzufügen von Untertiteln zu digitalen Medien**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Closedcaption-Objekt**](closedcaption-object.md)
</dt> </dl>

 

 





