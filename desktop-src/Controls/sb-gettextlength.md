---
title: SB_GETTEXTLENGTH Meldung (kommstrg. h)
description: Ruft die Länge des Texts aus dem angegebenen Teil eines Status Fensters in Zeichen ab.
ms.assetid: 2cd43106-dd43-499e-b595-760e9ededab5
keywords:
- Windows-Steuerelemente für SB_GETTEXTLENGTH Meldung
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
ms.openlocfilehash: 8b08dd3b870c3c59e5aafbeb9d53baef3816a726
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956888"
---
# <a name="sb_gettextlength-message"></a>SB \_ getTextLength-Nachricht

Ruft die Länge des Texts aus dem angegebenen Teil eines Status Fensters in Zeichen ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der null basierte Index des Teils, von dem Text abgerufen werden soll.

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen 32-Bit-Wert zurück, der aus 2 16-Bit-Werten besteht. Das niedrige Wort gibt die Länge des Texts in Zeichen an. Das hohe Wort gibt den Typ des Vorgangs an, mit dem der Text gezeichnet wird. Der Typ kann einen der folgenden Werte aufweisen:



| Rückgabecode                                                                                    | Beschreibung                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <dt>**0**</dt> </dl>               | Der Text wird mit einem Rahmen gezeichnet, der unterhalb der Ebene des Fensters angezeigt wird.<br/>          |
| <dl> <dt>**SBT- \_ Knoten**</dt> </dl>  | Der Text wird ohne Rahmen gezeichnet.<br/>                                                     |
| <dl> <dt>**SBT-Besitzer \_ Zeichnen**</dt> </dl>  | Der Text wird vom übergeordneten Fenster gezeichnet.<br/>                                                |
| <dl> <dt>**SBT- \_ Popout**</dt> </dl>     | Der Text wird mit einem Rahmen gezeichnet, der höher als die Ebene des Fensters angezeigt wird.<br/>         |
| <dl> <dt>**SBT \_ RtlReading**</dt> </dl> | Der Text wird in umgekehrter Richtung zum Text im übergeordneten Fenster angezeigt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Normaler Windows-Anzeige Text von links nach rechts (LTR). Windows kann so *gespiegelt* werden, dass Sprachen wie Hebräisch oder Arabisch angezeigt werden, die von rechts nach links (RTL) gelesen wurden. Wenn SBT \_ RtlReading festgelegt ist, wird der angegebene Statusfenster Text in umgekehrter Richtung aus dem Text im übergeordneten Fenster gelesen.

Diese Meldung gibt eine maximale Zeichen folgen Länge von 65.535 Zeichen zurück. Wenn die tatsächliche Text Zeichenfolge länger ist, wird Sie von der [**SB \_ gettext**](sb-gettext.md) -Nachricht abgeschnitten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **SB \_ Gettextlengthw** (Unicode) und **SB \_ gettextlengtha** (ANSI)<br/>         |



 

 





