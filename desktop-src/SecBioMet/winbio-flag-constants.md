---
title: WINBIO_FLAG Konstanten (winbio \_ types. h)
description: Geben Sie die Konfiguration für biometrische Einheiten und die Zugriffs Merkmale für die neue Sitzung an.
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
ms.openlocfilehash: 9ed632b5f15cc3d6a7ac6b0c6c70a2b3431b73db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391640"
---
# <a name="winbio_flag-constants"></a>Winbio- \_ Flag-Konstanten

Die folgenden Konstanten können in der [**winbioopensession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) -Funktion verwendet werden, um die Konfiguration und die Zugriffs Merkmale für biometrische Einheiten für die neue Sitzung anzugeben.



| Konstante                                                                                                                                                                                     | BESCHREIBUNG                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_FLAG_DEFAULT"></span><span id="winbio_flag_default"></span><dl> <dt>**winbio- \_ Flag ( \_ Standard)**</dt> </dl>             | Sensorkonfigurationsflag. Die biometrischen Einheiten arbeiten in der während der Installation angegebenen Weise.<br/>                                                                           |
| <span id="WINBIO_FLAG_BASIC"></span><span id="winbio_flag_basic"></span><dl> <dt>**winbio- \_ Flag \_ Basic**</dt> </dl>                   | Sensorkonfigurationsflag. Die biometrischen Einheiten werden nur als einfache Erfassungsgeräte betrieben.<br/>                                                                                         |
| <span id="WINBIO_FLAG_ADVANCED"></span><span id="winbio_flag_advanced"></span><dl> <dt>**winbio- \_ Flag \_ erweitert**</dt> </dl>          | Sensorkonfigurationsflag. Die biometrischen Einheiten verwenden interne Verarbeitungs-und Speicherfunktionen.<br/>                                                                              |
| <span id="WINBIO_FLAG_RAW"></span><span id="winbio_flag_raw"></span><dl> <dt>**winbio- \_ Flag \_ RAW**</dt> </dl>                         | Gewünschtes Zugriffsflag. Die Client Anwendung erfasst biometrische Rohdaten mithilfe von [**winbiocapturesample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample).<br/>                                             |
| <span id="WINBIO_FLAG_MAINTENANCE"></span><span id="winbio_flag_maintenance"></span><dl> <dt>**winbio- \_ Flag- \_ Wartung**</dt> </dl> | Gewünschtes Zugriffsflag. Der Client führt vom Hersteller definierte Steuerungs Vorgänge für eine biometrische Einheit durch Aufrufen von [**winbiocontrolunitprivilegierte**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged)durch.<br/> |



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

 

 





