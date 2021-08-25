---
title: WINBIO_DB Konstanten (Winbio \_ types.h)
description: Geben Sie die Datenbank an, die für einen Systempool verwendet werden soll.
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
ms.openlocfilehash: 0a9d8392fd38e9d53588002c8aeab688ffc8b76efced83819318d9c6b6c2b721
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867980"
---
# <a name="winbio_db-constants"></a>WINBIO \_ DB-Konstanten

Die folgenden Konstanten können beim Aufrufen von [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) verwendet werden, um die Datenbank anzugeben, die für einen Systempool verwendet werden soll.



| Konstante                                                                                                                                                                         | BESCHREIBUNG                                                                                                                                                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DB_DEFAULT"></span><span id="winbio_db_default"></span><dl> <dt>**WINBIO \_ DB \_ DEFAULT**</dt> </dl>       | Jede biometrische Einheit im Sensorpool verwendet die Standarddatenbank, die in der Standardkonfiguration biometrischer Einheiten angegeben ist.<br/>                                                                   |
| <span id="WINBIO_DB_BOOTSTRAP"></span><span id="winbio_db_bootstrap"></span><dl> <dt>**WINBIO \_ DB \_ BOOTSTRAP**</dt> </dl> | Kann für Szenarien vor dem Starten Windows verwendet werden. In der Regel ist die Datenbank Teil des Sensorchips oder Teil des BIOS und kann nur für die Registrierung und Löschung von Vorlagen verwendet werden.<br/> |
| <span id="WINBIO_DB_ONCHIP"></span><span id="winbio_db_onchip"></span><dl> <dt>**WINBIO \_ DB \_ ONCHIP**</dt> </dl>          | Die Datenbank befindet sich auf dem Sensorchip.<br/>                                                                                                                                                  |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (winbio.h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Clientanwendungskonstanten](client-application-constants.md)
</dt> </dl>

 

 





