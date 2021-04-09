---
title: SB_GETTEXT Meldung (kommstrg. h)
description: Ruft den Text aus dem angegebenen Teil eines Status Fensters ab.
ms.assetid: 95bef9ff-04e5-431e-bc79-06d8498fcab0
keywords:
- Windows-Steuerelemente für SB_GETTEXT Meldung
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
ms.openlocfilehash: e90b132c3f934188aea36afd86d53ab8f75bdadb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040845"
---
# <a name="sb_gettext-message"></a>SB \_ gettext-Nachricht

Ruft den Text aus dem angegebenen Teil eines Status Fensters ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der null basierte Index des Teils, von dem Text abgerufen werden soll.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf den Puffer, der den Text als eine mit NULL endenden Zeichenfolge empfängt. Verwenden Sie die [**SB \_ getTextLength**](sb-gettextlength.md) -Nachricht, um die erforderliche Größe des Puffers zu bestimmen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen 32-Bit-Wert zurück, der aus 2 16-Bit-Werten besteht. Das niedrige Wort gibt die Länge des Texts in Zeichen an. Das hohe Wort gibt den Typ des Vorgangs an, mit dem der Text gezeichnet wird. Der Typ kann einen der folgenden Werte aufweisen.



| Rückgabecode                                                                                    | Beschreibung                                                                               |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>**0**</dt> </dl>               | Der Text wird mit einem Rahmen gezeichnet, der unterhalb der Ebene des Fensters angezeigt wird.<br/>  |
| <dl> <dt>**SBT- \_ Knoten**</dt> </dl>  | Der Text wird ohne Rahmen gezeichnet.<br/>                                             |
| <dl> <dt>**SBT- \_ Popout**</dt> </dl>     | Der Text wird mit einem Rahmen gezeichnet, der höher als die Ebene des Fensters angezeigt wird.<br/> |
| <dl> <dt>**SBT \_ RtlReading**</dt> </dl> | Der Text wird in umgekehrter Richtung des Texts im übergeordneten Fenster angezeigt.<br/>  |



 

## <a name="remarks"></a>Bemerkungen

**Sicherheitswarnung:** Wenn Sie diese Meldung falsch verwenden, kann dies die Sicherheit des Programms beeinträchtigen. Diese Meldung bietet keine Möglichkeit, die Größe des Puffers zu kennen. Wenn Sie diese Meldung verwenden, rufen Sie zunächst [**SB \_ getTextLength**](sb-gettextlength.md) auf, um die erforderliche Anzahl von Zeichen abzurufen, und rufen Sie dann die Nachricht auf, um die Zeichenfolge abzurufen. Wenn Sie warten, bis **SB \_ gettext** aufgerufen wird, kann sich der Text ändern, wodurch der Rückgabewert von **SB \_ getTextLength** ungültig wird. Überprüfen Sie die [Sicherheitsaspekte: Microsoft Windows](sec-comctls.md) -Steuerelemente, bevor Sie fortfahren.

Diese Meldung gibt maximal 65.535 Zeichen zurück. Wenn die Text Zeichenfolge länger als die Zeichenfolge ist, wird Sie abgeschnitten.

Wenn der Text den Typ SBT \_ -Besitzer zeichnen aufweist, gibt diese Meldung den 32-Bit-Wert zurück, der dem Text anstelle der Länge und dem Vorgangstyp zugeordnet ist.

Normaler Windows-Anzeige Text von links nach rechts (LTR). Windows kann so *gespiegelt* werden, dass Sprachen wie Hebräisch oder Arabisch angezeigt werden, die von rechts nach links (RTL) gelesen wurden. Wenn SBT \_ RtlReading festgelegt ist, wird die *LPARAM* -Zeichenfolge in der entgegengesetzten Richtung aus dem Text im übergeordneten Fenster gelesen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **SB \_ Gettextw** (Unicode) und **SB \_ gettexta** (ANSI)<br/>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SB- \_ SetText**](sb-settext.md)
</dt> </dl>

 

 





