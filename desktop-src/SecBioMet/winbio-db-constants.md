---
title: WINBIO_DB Konstanten (winbio \_ types. h)
description: Geben Sie die Datenbank an, die für einen System Pool verwendet werden soll.
ms.assetid: 2cffa455-5834-4a35-b8d8-f9d1feddcaa1
topic_type:
- apiref
api_name:
- WINBIO_DB_DEFAULT
- WINBIO_DB_BOOTSTRAP
- WINBIO_DB_ONCHIP
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20503e1dc3cd7b5e47651889dd9c67777614593c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104367"
---
# <a name="winbio_db-constants"></a>Winbio \_ DB-Konstanten

Die folgenden Konstanten können beim Aufrufen von [**winbioopensession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) verwendet werden, um die Datenbank anzugeben, die für einen System Pool verwendet werden soll.



| Konstante                                                                                                                                                                         | BESCHREIBUNG                                                                                                                                                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DB_DEFAULT"></span><span id="winbio_db_default"></span><dl> <dt>**winbio \_ DB- \_ Standard**</dt> </dl>       | Jede biometrische Einheit im Sensor Pool verwendet die Standarddatenbank, die in der Standardkonfiguration für biometrische Einheiten angegeben ist.<br/>                                                                   |
| <span id="WINBIO_DB_BOOTSTRAP"></span><span id="winbio_db_bootstrap"></span><dl> <dt>**winbio- \_ DB- \_ Bootstrap**</dt> </dl> | Kann für Szenarien vor dem Starten von Windows verwendet werden. In der Regel ist die Datenbank Teil des Sensorchips oder Bestandteil des BIOS und kann nur für die Vorlagen Registrierung und-Löschung verwendet werden.<br/> |
| <span id="WINBIO_DB_ONCHIP"></span><span id="winbio_db_onchip"></span><dl> <dt>**winbio- \_ DB- \_ Onchip**</dt> </dl>          | Die Datenbank befindet sich auf dem Sensorchip.<br/>                                                                                                                                                  |



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

 

 





