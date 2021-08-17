---
title: WINBIO_FLAG Konstanten (Winbio \_ types.h)
description: Geben Sie biometrische Komponentenkonfiguration und Zugriffsmerkmale für die neue Sitzung an.
ms.assetid: 82b57023-6c27-433d-bf13-f136f501fc60
topic_type:
- apiref
api_name:
- WINBIO_FLAG_DEFAULT
- WINBIO_FLAG_BASIC
- WINBIO_FLAG_ADVANCED
- WINBIO_FLAG_RAW
- WINBIO_FLAG_MAINTENANCE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e018b1d810e3a57b4adea1116aa9bebc7b82dd44888b2d720e018329d31acf4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910310"
---
# <a name="winbio_flag-constants"></a>WINBIO \_ FLAG-Konstanten

Die folgenden Konstanten können in der [**WinBioOpenSession-Funktion**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) verwendet werden, um biometrische Komponentenkonfiguration und Zugriffsmerkmale für die neue Sitzung anzugeben.



| Konstante                                                                                                                                                                                     | BESCHREIBUNG                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_FLAG_DEFAULT"></span><span id="winbio_flag_default"></span><dl> <dt>**\_WINBIO-FLAG \_ STANDARD**</dt> </dl>             | Sensorkonfigurationsflag. Die biometrischen Einheiten werden auf die während der Installation angegebene Weise betrieben.<br/>                                                                           |
| <span id="WINBIO_FLAG_BASIC"></span><span id="winbio_flag_basic"></span><dl> <dt>**\_WINBIO-FLAG \_ BASIC**</dt> </dl>                   | Sensorkonfigurationsflag. Die biometrischen Einheiten werden nur als einfache Erfassungsgeräte verwendet.<br/>                                                                                         |
| <span id="WINBIO_FLAG_ADVANCED"></span><span id="winbio_flag_advanced"></span><dl> <dt>**\_WINBIO-FLAG \_ ERWEITERT**</dt> </dl>          | Sensorkonfigurationsflag. Die biometrischen Einheiten verwenden interne Verarbeitungs- und Speicherfunktionen.<br/>                                                                              |
| <span id="WINBIO_FLAG_RAW"></span><span id="winbio_flag_raw"></span><dl> <dt>**WINBIO-FLAG \_ \_ RAW**</dt> </dl>                         | Gewünschtes Zugriffsflag. Die Clientanwendung erfasst biometrische Rohdaten mit [**winBioCaptureSample.**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample)<br/>                                             |
| <span id="WINBIO_FLAG_MAINTENANCE"></span><span id="winbio_flag_maintenance"></span><dl> <dt>**\_WINBIO-FLAGWARTUNG \_**</dt> </dl> | Gewünschtes Zugriffsflag. Der Client führt anbieterdefinierte Steuerungsvorgänge für eine biometrische Einheit durch Aufrufen [**von WinBioControlUnitPrivileged aus.**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged)<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (einschließlich Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Clientanwendungskonst constants](client-application-constants.md)
</dt> </dl>

 

 





