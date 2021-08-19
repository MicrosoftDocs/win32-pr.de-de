---
title: SB_GETTEXTLENGTH (Commctrl.h)
description: Ruft die Länge des Texts aus dem angegebenen Teil eines Statusfensters in Zeichen ab.
ms.assetid: 2cd43106-dd43-499e-b595-760e9ededab5
keywords:
- SB_GETTEXTLENGTH meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- SB_GETTEXTLENGTH
- SB_GETTEXTLENGTHA
- SB_GETTEXTLENGTHW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b2c203862b2a17352924f3df07560034c9f52784c84676d924d78524b05be1c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084960"
---
# <a name="sb_gettextlength-message"></a>SB \_ GETTEXTLENGTH-Nachricht

Ruft die Länge des Texts aus dem angegebenen Teil eines Statusfensters in Zeichen ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nullbasierter Index des Teils, aus dem Text abgerufen werden soll.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen 32-Bit-Wert zurück, der aus zwei 16-Bit-Werten besteht. Das niedrige Wort gibt die Länge des Texts in Zeichen an. Das hohe Wort gibt den Typ des Vorgangs an, der zum Zeichnen des Texts verwendet wird. Der Typ kann einer der folgenden Werte sein:



| Rückgabecode                                                                                    | Beschreibung                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <dt>**0**</dt> </dl>               | Der Text wird mit einem Rahmen gezeichnet, der unter der Ebene des Fensters angezeigt wird.<br/>          |
| <dl> <dt>**SBT \_ NOBORDERS**</dt> </dl>  | Der Text wird ohne Rahmen gezeichnet.<br/>                                                     |
| <dl> <dt>**SBT \_ OWNERDRAW**</dt> </dl>  | Der Text wird vom übergeordneten Fenster gezeichnet.<br/>                                                |
| <dl> <dt>**\_SBT-POPOUT**</dt> </dl>     | Der Text wird mit einem Rahmen gezeichnet, der höher als die Ebene des Fensters angezeigt wird.<br/>         |
| <dl> <dt>**SBT \_ RTLREADING**</dt> </dl> | Der Text wird in der entgegengesetzten Richtung zum Text im übergeordneten Fenster angezeigt.<br/> |



 

## <a name="remarks"></a>Hinweise

Normale Fenster zeigen Text von links nach rechts (LTR) an. Windows kann *gespiegelt werden,* um Sprachen wie Hebräisch oder Arabisch anzuzeigen, die von rechts nach links (RTL) lesen. Wenn SBT RTLREADING festgelegt ist, wird der angegebene Statusfenstertext in umgekehrter Richtung aus dem Text \_ im übergeordneten Fenster gelesen.

Diese Meldung gibt eine maximale Zeichenfolgenlänge von 65.535 Zeichen zurück. Wenn die tatsächliche Textzeichenfolge länger als diese ist, wird sie von der [**SB \_ GETTEXT-Nachricht**](sb-gettext.md) abgeschnitten.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **SB \_ GETTEXTLENGTHW** (Unicode) und **SB \_ GETTEXTLENGBIG** (ANSI)<br/>         |



 

 





