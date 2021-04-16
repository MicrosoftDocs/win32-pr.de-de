---
title: EM_SETTOUCHOPTIONS Meldung (RichEdit. h)
description: Legt die einem Rich-Edit-Steuerelement zugeordneten Berührungs Optionen fest.
ms.assetid: C15036D6-B74F-414D-B731-F1587B616644
keywords:
- Windows-Steuerelemente für EM_SETTOUCHOPTIONS Meldung
topic_type:
- apiref
api_name:
- EM_SETTOUCHOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7613679a574955ef726da9fa10e8d919c8fe53b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477307"
---
# <a name="em_settouchoptions-message"></a>EM \_ settouchoptions-Meldung

Legt die einem Rich-Edit-Steuerelement zugeordneten Berührungs Optionen fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die festzulegende Berührungs Option. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                        | Bedeutung                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTO_SHOWHANDLES"></span><span id="rto_showhandles"></span><dl> <dt>**RTO- \_ showhandles**</dt> </dl>          | Ein-oder Ausblenden der Berührungs Zieh Punkte, abhängig vom Wert von *LPARAM*.<br/>                                                                                                                                                       |
| <span id="RTO_DISABLEHANDLES"></span><span id="rto_disablehandles"></span><dl> <dt>**RTO- \_ disablehandles**</dt> </dl> | Aktiviert oder deaktiviert die Berührungs Zieh Punkte, abhängig vom Wert von *LPARAM*. Wenn Handles deaktiviert sind, werden Sie ausgeblendet, wenn Sie sichtbar sind und ausgeblendet bleiben, bis eine **EM \_ settouchoptions** -Nachricht ihren Status ändert. <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Auf **true** festgelegt, um die Berührungs Auswahl Handles anzuzeigen bzw. zu aktivieren, oder **false** , um die Berührungs Auswahl Handles auszublenden bzw. zu deaktivieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt NULL zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ gettouchoptions**](em-settouchoptions.md)
</dt> </dl>

 

 





