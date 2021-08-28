---
title: EM_SETTOUCHOPTIONS-Nachricht (Richedit.h)
description: Legt die touch-Optionen fest, die einem Rich-Edit-Steuerelement zugeordnet sind.
ms.assetid: C15036D6-B74F-414D-B731-F1587B616644
keywords:
- EM_SETTOUCHOPTIONS Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 4ea2f372d1e59a76ea13667e994534df1088fe1c78c51c30ac54db1b4dfeed2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048010"
---
# <a name="em_settouchoptions-message"></a>EM \_ SETTOUCHOPTIONS-Meldung

Legt die touch-Optionen fest, die einem Rich-Edit-Steuerelement zugeordnet sind.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die festzulegende Touchoption. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                        | Bedeutung                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTO_SHOWHANDLES"></span><span id="rto_showhandles"></span><dl> <dt>**RTO \_ SHOWHANDLES**</dt> </dl>          | Ein- oder Ausblenden der Touchhandles, abhängig vom Wert von *lParam.*<br/>                                                                                                                                                       |
| <span id="RTO_DISABLEHANDLES"></span><span id="rto_disablehandles"></span><dl> <dt>**RTO \_ DISABLEHANDLES**</dt> </dl> | Aktivieren oder deaktivieren Sie die Touchhandles abhängig vom Wert von *lParam.* Wenn Handles deaktiviert sind, werden sie ausgeblendet, wenn sie sichtbar sind und ausgeblendet bleiben, bis eine **EM \_ SETTOUCHOPTIONS-Nachricht** ihren Status ändert. <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Legen Sie diese Einstellung auf **TRUE** fest, um die Touchauswahlhandles anzuzeigen/zu aktivieren, oder **FALSE,** um die Touchauswahlhandles auszublenden/zu deaktivieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt 0 (null) zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ GETTOUCHOPTIONS**](em-settouchoptions.md)
</dt> </dl>

 

 





