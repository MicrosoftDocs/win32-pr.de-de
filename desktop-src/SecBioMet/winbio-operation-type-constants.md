---
title: WINBIO_OPERATION_TYPE Konstanten (winbio \_ types. h)
description: Geben Sie den Typ des asynchronen Vorgangs an, der ausgeführt wird.
ms.assetid: D4ECEF91-BEC7-4A42-8808-F09F5C141180
topic_type:
- apiref
api_name:
- WINBIO_OPERATION_NONE
- WINBIO_OPERATION_OPEN
- WINBIO_OPERATION_CLOSE
- WINBIO_OPERATION_VERIFY
- WINBIO_OPERATION_IDENTIFY
- WINBIO_OPERATION_LOCATE_SENSOR
- WINBIO_OPERATION_ENROLL_BEGIN
- WINBIO_OPERATION_ENROLL_CAPTURE
- WINBIO_OPERATION_ENROLL_COMMIT
- WINBIO_OPERATION_ENROLL_DISCARD
- WINBIO_OPERATION_ENUM_ENROLLMENTS
- WINBIO_OPERATION_DELETE_TEMPLATE
- WINBIO_OPERATION_CAPTURE_SAMPLE
- WINBIO_OPERATION_GET_PROPERTY
- WINBIO_OPERATION_SET_PROPERTY
- WINBIO_OPERATION_GET_EVENT
- WINBIO_OPERATION_LOCK_UNIT
- WINBIO_OPERATION_UNLOCK_UNIT
- WINBIO_OPERATION_CONTROL_UNIT
- WINBIO_OPERATION_CONTROL_UNIT_PRIVILEGED
- WINBIO_OPERATION_OPEN_FRAMEWORK
- WINBIO_OPERATION_CLOSE_FRAMEWORK
- WINBIO_OPERATION_ENUM_SERVICE_PROVIDERS
- WINBIO_OPERATION_ENUM_BIOMETRIC_UNITS
- WINBIO_OPERATION_ENUM_DATABASES
- WINBIO_OPERATION_UNIT_ARRIVAL
- WINBIO_OPERATION_UNIT_REMOVAL
- WINBIO_OPERATION_IDENTIFY_AND_RELEASE_TICKET
- WINBIO_OPERATION_VERIFY_AND_RELEASE_TICKET
- WINBIO_OPERATION_MONITOR_PRESENCE
- WINBIO_OPERATION_ENROLL_SELECT
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b83f32b9f98a24d0ed4d9995bf5fcb7eaa3a2b6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106496"
---
# <a name="winbio_operation_type-constants"></a>Winbio \_ - \_ Vorgangstyp Konstanten

Die folgenden Konstanten können von der Windows-Biometrieframework in einem asynchronen [**winbio- \_ \_ Ergebnis**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) zurückgegeben werden, um den Typ des asynchronen Vorgangs anzugeben, der ausgeführt wird.

<dl> <dt>

<span id="WINBIO_OPERATION_NONE"></span><span id="winbio_operation_none"></span>**winbio- \_ Vorgang " \_ None"**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Es wurde kein Vorgang identifiziert.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_OPEN"></span><span id="winbio_operation_open"></span>**winbio- \_ Vorgang \_ geöffnet**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Eine biometrische Sitzung wurde geöffnet. Weitere Informationen finden Sie unter [**winbioasyncopensession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CLOSE"></span><span id="winbio_operation_close"></span>**winbio- \_ Vorgang \_ Schließen**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Eine biometrische Sitzung wurde geschlossen. Weitere Informationen finden Sie unter [**winbioclosesession**](/windows/desktop/api/Winbio/nf-winbio-winbioclosesession).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_VERIFY"></span><span id="winbio_operation_verify"></span>**Überprüfung des winbio- \_ Vorgangs \_**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



Ein biometrisches Beispiel wurde anhand einer Benutzeridentität überprüft. Weitere Informationen finden Sie unter [**winbioverify**](/windows/desktop/api/Winbio/nf-winbio-winbioverify).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_IDENTIFY"></span><span id="winbio_operation_identify"></span>**winbio- \_ Vorgang \_ identifizieren**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Ein biometrisches Beispiel wurde aufgezeichnet und mit einer vorhandenen Vorlage verglichen. Weitere Informationen finden Sie unter [**winbioidentifi.**](/windows/desktop/api/Winbio/nf-winbio-winbioidentify)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_LOCATE_SENSOR"></span><span id="winbio_operation_locate_sensor"></span>**winbio- \_ Vorgang zum \_ Suchen des \_ Sensors**
</dt> <dd> <dl> <dt>

5
</dt> <dt>



Die ID-Nummer einer biometrischen Einheit wurde abgerufen. Weitere Informationen finden Sie unter [**winbiolosinesensor**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensor).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_BEGIN"></span><span id="winbio_operation_enroll_begin"></span>**Beginn der winbio- \_ Operation beim \_ registrieren \_**
</dt> <dd> <dl> <dt>

6
</dt> <dt>



Eine biometrische Registrierungs Sequenz wurde initiiert. Weitere Informationen finden Sie unter [**winbioeinschreibung**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_CAPTURE"></span><span id="winbio_operation_enroll_capture"></span>**Erfassung von winbio- \_ Operation \_ registrieren \_**
</dt> <dd> <dl> <dt>

7
</dt> <dt>



Ein biometrisches Beispiel wurde aufgezeichnet und der Vorlage hinzugefügt. Weitere Informationen finden Sie unter [**winbioregistricapture**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapture).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_COMMIT"></span><span id="winbio_operation_enroll_commit"></span>**winbio- \_ Vorgangs Registrierungs \_ \_ Commit**
</dt> <dd> <dl> <dt>

8
</dt> <dt>



Eine ausstehende biometrische Vorlage wurde abgeschlossen. Weitere Informationen finden Sie unter [**winbioregistricommit**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_DISCARD"></span><span id="winbio_operation_enroll_discard"></span>**die Registrierung des winbio- \_ Vorgangs wird \_ \_ verworfen.**
</dt> <dd> <dl> <dt>

9
</dt> <dt>



Eine ausstehende biometrische Vorlage wurde verworfen. Weitere Informationen finden Sie unter [**winbioregistrierungs verwerfen**](/windows/desktop/api/Winbio/nf-winbio-winbioenrolldiscard).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENUM_ENROLLMENTS"></span><span id="winbio_operation_enum_enrollments"></span>**winbio-Operation-Aufzählungs \_ \_ \_ Registrierungen**
</dt> <dd> <dl> <dt>

10
</dt> <dt>



Die unter Faktoren für eine bestimmte Vorlage wurden aufgelistet. Weitere Informationen finden Sie unter [**winbioenumregistrierungen**](/windows/desktop/api/Winbio/nf-winbio-winbioenumenrollments).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_DELETE_TEMPLATE"></span><span id="winbio_operation_delete_template"></span>**Vorlage zum Löschen des winbio- \_ Vorgangs \_ \_**
</dt> <dd> <dl> <dt>

11
</dt> <dt>



Eine biometrische Vorlage wurde aus dem Speicher gelöscht. Weitere Informationen finden Sie unter [**winbiodeletetemplate**](/windows/desktop/api/Winbio/nf-winbio-winbiodeletetemplate).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CAPTURE_SAMPLE"></span><span id="winbio_operation_capture_sample"></span>**Beispiel für winbio- \_ Vorgangs \_ Erfassung \_**
</dt> <dd> <dl> <dt>

12
</dt> <dt>



Ein biometrisches Beispiel wurde aufgezeichnet. Weitere Informationen finden Sie unter [**winbiocapturesample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_GET_PROPERTY"></span><span id="winbio_operation_get_property"></span>**winbio- \_ Operation \_ get- \_ Eigenschaft**
</dt> <dd> <dl> <dt>

13
</dt> <dt>



Eine biometrische Sitzung, eine Einheit oder eine Vorlagen Eigenschaft wurde abgerufen. Weitere Informationen finden Sie unter [**winbiogetproperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_SET_PROPERTY"></span><span id="winbio_operation_set_property"></span>**winbio \_ Operation \_ Set ( \_ Eigenschaft)**
</dt> <dd> <dl> <dt>

14
</dt> <dt>



Es wurde eine biometrische Sitzung, eine Einheit, eine Vorlage oder eine Konto Eigenschaft festgelegt. Weitere Informationen finden Sie unter [**winbiosetproperty**](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_GET_EVENT"></span><span id="winbio_operation_get_event"></span>**winbio- \_ Operation \_ get- \_ Ereignis**
</dt> <dd> <dl> <dt>

15
</dt> <dt>



Nicht verwendet.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_LOCK_UNIT"></span><span id="winbio_operation_lock_unit"></span>**winbio- \_ Vorgangs \_ Sperr \_ Einheit**
</dt> <dd> <dl> <dt>

16
</dt> <dt>



Eine biometrische Einheit wurde für eine ausschließliche Verwendung durch eine Sitzung gesperrt. Weitere Informationen finden Sie unter [**winbiolockunit**](/windows/desktop/api/Winbio/nf-winbio-winbiolockunit).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_UNLOCK_UNIT"></span><span id="winbio_operation_unlock_unit"></span>**winbio- \_ Vorgang zum \_ Entsperren der \_ Einheit**
</dt> <dd> <dl> <dt>

17
</dt> <dt>



Die Sitzungs Sperre für eine biometrische Einheit wurde freigegeben. Weitere Informationen finden Sie unter [**winbiounlockunit**](/windows/desktop/api/Winbio/nf-winbio-winbiounlockunit).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CONTROL_UNIT"></span><span id="winbio_operation_control_unit"></span>**winbio- \_ Vorgangs \_ Steuerungs \_ Einheit**
</dt> <dd> <dl> <dt>

18
</dt> <dt>



Hersteller definierte Vorgänge wurden für eine Steuereinheit ausgeführt. Weitere Informationen finden Sie unter [**winbiocontrolunit**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunit).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CONTROL_UNIT_PRIVILEGED"></span><span id="winbio_operation_control_unit_privileged"></span>**privilegierter winbio- \_ Vorgangs \_ Steuerungs \_ Einheit \_**
</dt> <dd> <dl> <dt>

19
</dt> <dt>



Privilegierte Hersteller definierte Vorgänge wurden für eine Steuerungseinheit durchgeführt. Weitere Informationen finden Sie unter [**winbiocontrolunitprivilegiert**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_OPEN_FRAMEWORK"></span><span id="winbio_operation_open_framework"></span>**winbio \_ Operation \_ Open \_ Framework**
</dt> <dd> <dl> <dt>

20
</dt> <dt>



Ein Handle für das biometrische Framework wurde geöffnet.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CLOSE_FRAMEWORK"></span><span id="winbio_operation_close_framework"></span>**winbio- \_ Vorgang \_ Schließen- \_ Framework**
</dt> <dd> <dl> <dt>

21
</dt> <dt>



Ein Handle für das biometrische Framework wurde geschlossen. Weitere Informationen finden Sie unter [**winbiocloseframework**](/windows/desktop/api/Winbio/nf-winbio-winbiocloseframework).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENUM_SERVICE_PROVIDERS"></span><span id="winbio_operation_enum_service_providers"></span>**winbio \_ Operation \_ Enum- \_ Dienst \_ Anbieter**
</dt> <dd> <dl> <dt>

22
</dt> <dt>



Die installierten biometrischen Dienstanbieter wurden aufgelistet. Weitere Informationen finden Sie unter [**winbioenumserviceproviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENUM_BIOMETRIC_UNITS"></span><span id="winbio_operation_enum_biometric_units"></span>**\_ \_ \_ biometrische \_ Einheiten für winbio-Operation-Aufzählung**
</dt> <dd> <dl> <dt>

23
</dt> <dt>



Die angefügten biometrischen Einheiten wurden aufgezählt. Weitere Informationen finden Sie unter [**winbioasyncengbiometricunits**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncenumbiometricunits).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENUM_DATABASES"></span><span id="winbio_operation_enum_databases"></span>**winbio-Operation-Aufzählungs \_ \_ \_ Datenbanken**
</dt> <dd> <dl> <dt>

24
</dt> <dt>



Die registrierten Datenbanken wurden aufgelistet. Weitere Informationen finden Sie unter [**winbioenumdatenbanken**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_UNIT_ARRIVAL"></span><span id="winbio_operation_unit_arrival"></span>**winbio- \_ Vorgangs \_ Einheiten \_ Ankunft**
</dt> <dd> <dl> <dt>

25
</dt> <dt>



Es wurde eine biometrische Einheit erstellt. Weitere Informationen finden Sie unter [**winbioasyncmonitorframeworkchanges**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_UNIT_REMOVAL"></span><span id="winbio_operation_unit_removal"></span>**Entfernen von winbio- \_ Vorgangs \_ Einheiten \_**
</dt> <dd> <dl> <dt>

26
</dt> <dt>



Eine biometrische Einheit wurde gelöscht. Weitere Informationen finden Sie unter [**winbioasyncmonitorframeworkchanges**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_IDENTIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_identify_and_release_ticket"></span>**winbio \_ -Vorgang zum \_ identifizieren \_ und \_ Freigeben des \_ Tickets**
</dt> <dd> <dl> <dt>

27
</dt> <dt>



Reserviert. Dieser Wert wird ab Windows 10 unterstützt.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_VERIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_verify_and_release_ticket"></span>**winbio \_ -Vorgang zum \_ überprüfen \_ und \_ Freigeben des \_ Tickets**
</dt> <dd> <dl> <dt>

28
</dt> <dt>



Reserviert. Dieser Wert wird ab Windows 10 unterstützt.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_MONITOR_PRESENCE"></span><span id="winbio_operation_monitor_presence"></span>**Anwesenheit des winbio- \_ Vorgangs \_ Monitors \_**
</dt> <dd> <dl> <dt>

29
</dt> <dt>



Der Gesichts Erkennungsmechanismus oder der Iris-Überwachungsmechanismus wurde aktiviert. Weitere Informationen finden Sie unter [**winbiomonitorpresence**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence). Dieser Wert wird ab Windows 10 unterstützt.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_SELECT"></span><span id="winbio_operation_enroll_select"></span>**winbio- \_ Operation \_ registrieren ( \_ Select)**
</dt> <dd> <dl> <dt>

30
</dt> <dt>



Eine Person aus einer Gruppe von Einzelpersonen, die durch Daten im Beispiel Puffer dargestellt wird, wurde als zu registrierende Person angegeben. Weitere Informationen finden Sie unter [**winbioeinschreibung Select**](/windows/desktop/api/winbio/nf-winbio-winbioenrollselect). Dieser Wert wird ab Windows 10 unterstützt.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                                                                                     |
| Header<br/>                   | <dl> <dt>Winbio \_ types. h (Include winbio. h für Client Anwendungen oder winbio \_ Adapters. h für Adapter)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Client Anwendungs Konstanten](client-application-constants.md)
</dt> </dl>

 

 





