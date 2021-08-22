---
title: WINBIO_EVENT Konstanten (Winbio \_ types.h)
description: Geben Sie die Typen von Dienstanbieterereignisbenachrichtigungen an, die überwacht werden sollen.
ms.assetid: 73805413-a8d9-4682-aa21-7032451d750a
topic_type:
- apiref
api_name:
- WINBIO_EVENT_FP_UNCLAIMED
- WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a871022c51a906bd078125ae6aa6aa30c2e97024279f3309ca4ece58c00a88f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910658"
---
# <a name="winbio_event-constants"></a>WINBIO \_ EVENT-Konstanten

Die folgenden Konstanten können in der [**WinBioRegisterEventMonitor-Funktion**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) verwendet werden, um die Typen der zu überwachenden Dienstanbieterereignisbenachrichtigungen anzugeben.



| Konstante                                                                                                                                                                                                                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_EVENT_FP_UNCLAIMED"></span><span id="winbio_event_fp_unclaimed"></span><dl> <dt>**WINBIO \_ EVENT \_ FP \_ UNCLAIMED**</dt> </dl>                             | Der Sensor hat eine Fingerwischbewegung erkannt, die von der Anwendung oder dem Fenster, das derzeit den Fokus besitzt, nicht angefordert wurde. Der Windows Biometric Framework ruft Ihre Rückruffunktion auf, um anzugeben, dass ein Fingerwischen aufgetreten ist, aber nicht versucht, den Fingerabdruck zu identifizieren.<br/> |
| <span id="WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY"></span><span id="winbio_event_fp_unclaimed_identify"></span><dl> <dt>**WINBIO \_ EVENT \_ FP \_ UNCLAIMED \_ IDENTIFY**</dt> </dl> | Der Sensor hat eine Fingerwischbewegung erkannt, die von der Anwendung oder dem Fenster, das derzeit den Fokus besitzt, nicht angefordert wurde. Der Windows Biometric Framework versucht, den Fingerabdruck zu identifizieren, und übergibt das Ergebnis dieses Prozesses an Ihre Rückruffunktion.<br/>                        |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (winbio.h einschließen)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Clientanwendungskonstanten](client-application-constants.md)
</dt> </dl>

 

 





