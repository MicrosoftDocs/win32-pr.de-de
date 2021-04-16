---
title: WINBIO_EVENT Konstanten (winbio \_ types. h)
description: Geben Sie die zu überwachenden Ereignis Benachrichtigungs Typen für Dienstanbieter an.
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
ms.openlocfilehash: 182a4ffe254e946f1b8deca2c5034e665a58f7ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517474"
---
# <a name="winbio_event-constants"></a>Winbio- \_ Ereignis Konstanten

Die folgenden Konstanten können in der [**winbioregistereventmonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) -Funktion verwendet werden, um die Typen der zu überwachenden Ereignis Benachrichtigungen für den Dienstanbieter anzugeben.



| Konstante                                                                                                                                                                                                                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_EVENT_FP_UNCLAIMED"></span><span id="winbio_event_fp_unclaimed"></span><dl> <dt>**winbio- \_ Ereignis \_ FP \_ nicht beansprucht**</dt> </dl>                             | Der Sensor hat einen Fingerring erkannt, der nicht von der Anwendung angefordert wurde, oder das Fenster, das gerade den Fokus besitzt. Der Windows-Biometrieframework Ruft die Rückruffunktion auf, um anzugeben, dass ein Finger schwenken aufgetreten ist, aber nicht versucht, den Fingerabdruck zu identifizieren.<br/> |
| <span id="WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY"></span><span id="winbio_event_fp_unclaimed_identify"></span><dl> <dt>**winbio- \_ Ereignis \_ FP \_ nicht beansprucht- \_ Identifizierung**</dt> </dl> | Der Sensor hat einen Fingerring erkannt, der nicht von der Anwendung angefordert wurde, oder das Fenster, das gerade den Fokus besitzt. Der Windows-Biometrieframework versucht, den Fingerabdruck zu identifizieren, und übergibt das Ergebnis dieses Prozesses an Ihre Rückruffunktion.<br/>                        |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types. h (Include winbio. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Client Anwendungs Konstanten](client-application-constants.md)
</dt> </dl>

 

 





