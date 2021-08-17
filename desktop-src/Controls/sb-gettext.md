---
title: SB_GETTEXT Nachricht (Commctrl.h)
description: Ruft den Text aus dem angegebenen Teil eines Statusfensters ab.
ms.assetid: 95bef9ff-04e5-431e-bc79-06d8498fcab0
keywords:
- SB_GETTEXT Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- SB_GETTEXT
- SB_GETTEXTA
- SB_GETTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05967d41d86ad039e39259c8179a9e768e8fbbf76e5112b531048ac0ed7b56bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168728"
---
# <a name="sb_gettext-message"></a>SB \_ GETTEXT-Nachricht

Ruft den Text aus dem angegebenen Teil eines Statusfensters ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nullbasierter Index des Teils, aus dem Text abgerufen werden soll.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf den Puffer, der den Text als auf NULL endende Zeichenfolge empfängt. Verwenden Sie die [**SB \_ GETTEXTLENGTH-Nachricht,**](sb-gettextlength.md) um die erforderliche Größe des Puffers zu bestimmen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen 32-Bit-Wert zurück, der aus zwei 16-Bit-Werten besteht. Das niedrige Wort gibt die Länge des Texts in Zeichen an. Das obere Wort gibt den Vorgangstyp an, der zum Zeichnen des Texts verwendet wird. Der Typ kann einer der folgenden Werte sein.



| Rückgabecode                                                                                    | Beschreibung                                                                               |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>**0**</dt> </dl>               | Der Text wird mit einem Rahmen gezeichnet, der unterhalb der Fensterebene angezeigt wird.<br/>  |
| <dl> <dt>**SBT \_ NOBORDERS**</dt> </dl>  | Der Text wird ohne Rahmen gezeichnet.<br/>                                             |
| <dl> <dt>**SBT \_ POPOUT**</dt> </dl>     | Der Text wird mit einem Rahmen gezeichnet, der höher als die Ebene des Fensters angezeigt wird.<br/> |
| <dl> <dt>**SBT \_ RTLREADING**</dt> </dl> | Der Text wird in der entgegengesetzten Richtung des Texts im übergeordneten Fenster angezeigt.<br/>  |



 

## <a name="remarks"></a>Hinweise

**Sicherheitswarnung:** Wenn Sie diese Meldung falsch verwenden, kann dies die Sicherheit Ihres Programms beeinträchtigen. Diese Meldung bietet keine Möglichkeit, die Größe des Puffers zu kennen. Wenn Sie diese Nachricht verwenden, rufen Sie zuerst [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) auf, um die erforderliche Anzahl von Zeichen abzurufen, und rufen Sie dann die Nachricht auf, um die Zeichenfolge abzurufen. Wenn Sie warten, bevor Sie **SB \_ GETTEXT** aufrufen, könnte sich der Text ändern, wodurch der Rückgabewert von **SB \_ GETTEXTLENGTH** ungültig wird. Lesen Sie die [Sicherheitsüberlegungen: Microsoft Windows Controls,](sec-comctls.md) bevor Sie fortfahren.

Diese Meldung gibt maximal 65.535 Zeichen zurück. Wenn die Textzeichenfolge länger ist, wird sie abgeschnitten.

Wenn der Text über den Zeichnungstyp SBT \_ OWNERDRAW verfügt, gibt diese Nachricht den dem Text zugeordneten 32-Bit-Wert anstelle der Länge und des Vorgangstyps zurück.

Normale Fenster zeigen Text von links nach rechts (LTR) an. Windows können *gespiegelt* werden, um Sprachen wie Hebräisch oder Arabisch anzuzeigen, die von rechts nach links (RTL) lesen. Wenn SBT \_ RTLREADING festgelegt ist, liest die *lParam-Zeichenfolge* in entgegengesetzter Richtung aus dem Text im übergeordneten Fenster.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **SB \_ GETTEXTW** (Unicode) und **SB \_ GETTEXTA** (ANSI)<br/>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SB \_ SETTEXT**](sb-settext.md)
</dt> </dl>

 

 





