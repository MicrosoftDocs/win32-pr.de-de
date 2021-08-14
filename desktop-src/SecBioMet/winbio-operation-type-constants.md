---
title: WINBIO_OPERATION_TYPE Konstanten (Winbio \_ types.h)
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
ms.openlocfilehash: b39dd6e2656ad73623df9d6a92d514e90371bc3761563e5f24c41211680c2455
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909949"
---
# <a name="winbio_operation_type-constants"></a>WINBIO \_ OPERATION \_ TYPE-Konstanten

Die folgenden Konstanten können vom Windows Biometric Framework in einem [**WINBIO \_ ASYNC \_ RESULT**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) zurückgegeben werden, um den Typ des ausgeführten asynchronen Vorgangs anzugeben.

<dl> <dt>

<span id="WINBIO_OPERATION_NONE"></span><span id="winbio_operation_none"></span>**\_WINBIO-VORGANG \_ NONE**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Es wurde kein Vorgang identifiziert.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_OPEN"></span><span id="winbio_operation_open"></span>**WINBIO \_ OPERATION \_ OPEN**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Eine biometrische Sitzung wurde geöffnet. Weitere Informationen finden Sie unter [**WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CLOSE"></span><span id="winbio_operation_close"></span>**WINBIO \_ OPERATION \_ CLOSE**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Eine biometrische Sitzung wurde geschlossen. Weitere Informationen finden Sie unter [**WinBioCloseSession**](/windows/desktop/api/Winbio/nf-winbio-winbioclosesession).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_VERIFY"></span><span id="winbio_operation_verify"></span>**WINBIO \_ OPERATION \_ VERIFY**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



Ein biometrisches Beispiel wurde anhand einer Benutzeridentität überprüft. Weitere Informationen finden Sie unter [**WinBioVerify.**](/windows/desktop/api/Winbio/nf-winbio-winbioverify)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_IDENTIFY"></span><span id="winbio_operation_identify"></span>**WINBIO \_ OPERATION \_ IDENTIFY**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Ein biometrisches Beispiel wurde erfasst und mit einer vorhandenen Vorlage verglichen. Weitere Informationen finden Sie unter [**WinBioIdentify.**](/windows/desktop/api/Winbio/nf-winbio-winbioidentify)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_LOCATE_SENSOR"></span><span id="winbio_operation_locate_sensor"></span>**WINBIO \_ OPERATION \_ LOCATE \_ SENSOR**
</dt> <dd> <dl> <dt>

5
</dt> <dt>



Die ID-Nummer einer biometrischen Einheit wurde abgerufen. Weitere Informationen finden Sie unter [**WinBioLocateSensor**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensor).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_BEGIN"></span><span id="winbio_operation_enroll_begin"></span>**WINBIO \_ OPERATION \_ ENROLL \_ BEGIN**
</dt> <dd> <dl> <dt>

6
</dt> <dt>



Eine biometrische Registrierungssequenz wurde initiiert. Weitere Informationen finden Sie unter [**WinBioEnrollBegin.**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_CAPTURE"></span><span id="winbio_operation_enroll_capture"></span>**WINBIO \_ OPERATION \_ ENROLL \_ CAPTURE**
</dt> <dd> <dl> <dt>

7
</dt> <dt>



Ein biometrisches Beispiel wurde erfasst und der Vorlage hinzugefügt. Weitere Informationen finden Sie unter [**WinBioEnrollCapture**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapture).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_COMMIT"></span><span id="winbio_operation_enroll_commit"></span>**WINBIO \_ OPERATION \_ ENROLL \_ COMMIT**
</dt> <dd> <dl> <dt>

8
</dt> <dt>



Eine ausstehende biometrische Vorlage wurde abgeschlossen. Weitere Informationen finden Sie unter [**WinBioEnrollCommit.**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_DISCARD"></span><span id="winbio_operation_enroll_discard"></span>**VERWERFEN DES \_ WINBIO-VORGANGS \_ \_ "REGISTRIEREN"**
</dt> <dd> <dl> <dt>

9
</dt> <dt>



Eine ausstehende biometrische Vorlage wurde verworfen. Weitere Informationen finden Sie unter [**WinBioEnrollDiscard.**](/windows/desktop/api/Winbio/nf-winbio-winbioenrolldiscard)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENUM_ENROLLMENTS"></span><span id="winbio_operation_enum_enrollments"></span>**\_ \_ \_ WINBIO-VORGANGS-ENUMERATIONSREGISTRIERUNGEN**
</dt> <dd> <dl> <dt>

10
</dt> <dt>



Die Unterfaktoren für eine bestimmte Vorlage wurden aufzählt. Weitere Informationen finden Sie unter [**WinBioEnumEnrollments**](/windows/desktop/api/Winbio/nf-winbio-winbioenumenrollments).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_DELETE_TEMPLATE"></span><span id="winbio_operation_delete_template"></span>**WINBIO \_ OPERATION \_ DELETE \_ TEMPLATE**
</dt> <dd> <dl> <dt>

11
</dt> <dt>



Eine biometrische Vorlage wurde aus dem Speicher gelöscht. Weitere Informationen finden Sie unter [**WinBioDeleteTemplate.**](/windows/desktop/api/Winbio/nf-winbio-winbiodeletetemplate)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CAPTURE_SAMPLE"></span><span id="winbio_operation_capture_sample"></span>**BEISPIEL \_ FÜR WINBIO-VORGANGSERFASSUNG \_ \_**
</dt> <dd> <dl> <dt>

12
</dt> <dt>



Ein biometrisches Beispiel wurde erfasst. Weitere Informationen finden Sie unter [**WinBioCaptureSample.**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_GET_PROPERTY"></span><span id="winbio_operation_get_property"></span>**\_GET-EIGENSCHAFT DES WINBIO-VORGANGS \_ \_**
</dt> <dd> <dl> <dt>

13
</dt> <dt>



Eine biometrische Sitzung, Einheit oder Vorlageneigenschaft wurde abgerufen. Weitere Informationen finden Sie unter [**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_SET_PROPERTY"></span><span id="winbio_operation_set_property"></span>**SET-EIGENSCHAFT DES \_ WINBIO-VORGANGS \_ \_**
</dt> <dd> <dl> <dt>

14
</dt> <dt>



Eine biometrische Sitzung, Einheit, Vorlage oder Kontoeigenschaft wurde festgelegt. Weitere Informationen finden Sie unter [**WinBioSetProperty**](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_GET_EVENT"></span><span id="winbio_operation_get_event"></span>**WINBIO \_ OPERATION \_ GET \_ EVENT**
</dt> <dd> <dl> <dt>

15
</dt> <dt>



Wird nicht verwendet.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_LOCK_UNIT"></span><span id="winbio_operation_lock_unit"></span>**WINBIO \_ OPERATION \_ LOCK \_ UNIT**
</dt> <dd> <dl> <dt>

16
</dt> <dt>



Eine biometrische Einheit wurde für die exklusive Verwendung durch eine Sitzung gesperrt. Weitere Informationen finden Sie unter [**WinBioLockUnit.**](/windows/desktop/api/Winbio/nf-winbio-winbiolockunit)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_UNLOCK_UNIT"></span><span id="winbio_operation_unlock_unit"></span>**WINBIO \_ OPERATION \_ UNLOCK \_ UNIT**
</dt> <dd> <dl> <dt>

17
</dt> <dt>



Die Sitzungssperre für eine biometrische Einheit wurde aufgehoben. Weitere Informationen finden Sie unter [**WinBioUnlockUnit.**](/windows/desktop/api/Winbio/nf-winbio-winbiounlockunit)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CONTROL_UNIT"></span><span id="winbio_operation_control_unit"></span>**\_ \_ WINBIO-VORGANGSSTEUERUNGSEINHEIT \_**
</dt> <dd> <dl> <dt>

18
</dt> <dt>



Vom Anbieter definierte Vorgänge wurden für eine Steuereinheit ausgeführt. Weitere Informationen finden Sie unter [**WinBioControlUnit.**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunit)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CONTROL_UNIT_PRIVILEGED"></span><span id="winbio_operation_control_unit_privileged"></span>**\_ \_ WINBIO-VORGANGSSTEUERUNGSEINHEIT \_ \_ PRIVILEGED**
</dt> <dd> <dl> <dt>

19
</dt> <dt>



Vom privilegierten Anbieter definierte Vorgänge wurden für eine Steuerungseinheit ausgeführt. Weitere Informationen finden Sie unter [**WinBioControlUnitPrivileged.**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_OPEN_FRAMEWORK"></span><span id="winbio_operation_open_framework"></span>**WINBIO \_ OPERATION \_ OPEN \_ FRAMEWORK**
</dt> <dd> <dl> <dt>

20
</dt> <dt>



Ein Handle für das biometrische Framework wurde geöffnet.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CLOSE_FRAMEWORK"></span><span id="winbio_operation_close_framework"></span>**WINBIO \_ OPERATION \_ CLOSE \_ FRAMEWORK**
</dt> <dd> <dl> <dt>

21
</dt> <dt>



Ein Handle für das biometrische Framework wurde geschlossen. Weitere Informationen finden Sie unter [**WinBioCloseFramework**](/windows/desktop/api/Winbio/nf-winbio-winbiocloseframework).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENUM_SERVICE_PROVIDERS"></span><span id="winbio_operation_enum_service_providers"></span>**\_ \_ WINBIO-VORGANGSENUMER-DIENSTANBIETER \_ \_**
</dt> <dd> <dl> <dt>

22
</dt> <dt>



Die installierten biometrischen Dienstanbieter wurden aufzählt. Weitere Informationen finden Sie unter [**WinBioEnumServiceProviders.**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENUM_BIOMETRIC_UNITS"></span><span id="winbio_operation_enum_biometric_units"></span>**WINBIO \_ OPERATION \_ ENUM \_ BIOMETRIC \_ UNITS**
</dt> <dd> <dl> <dt>

23
</dt> <dt>



Die angefügten biometrischen Einheiten wurden aufzählt. Weitere Informationen finden Sie unter [**WinBioAsyncEnumBiometricUnits.**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncenumbiometricunits)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENUM_DATABASES"></span><span id="winbio_operation_enum_databases"></span>**\_ \_ WINBIO-VORGANGSENUMERDATENBANKEN \_**
</dt> <dd> <dl> <dt>

24
</dt> <dt>



Die registrierten Datenbanken wurden aufzählt. Weitere Informationen finden Sie unter [**WinBioEnumDatabases.**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_UNIT_ARRIVAL"></span><span id="winbio_operation_unit_arrival"></span>**WINBIO \_ OPERATION \_ UNIT \_ ARRIVAL**
</dt> <dd> <dl> <dt>

25
</dt> <dt>



Es wurde eine biometrische Einheit erstellt. Weitere Informationen finden Sie unter [**WinBioAsyncMonitorFrameworkChanges.**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_UNIT_REMOVAL"></span><span id="winbio_operation_unit_removal"></span>**ENTFERNEN VON \_ WINBIO-VORGANGSEINHEITEN \_ \_**
</dt> <dd> <dl> <dt>

26
</dt> <dt>



Eine biometrische Einheit wurde gelöscht. Weitere Informationen finden Sie unter [**WinBioAsyncMonitorFrameworkChanges.**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges)


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_IDENTIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_identify_and_release_ticket"></span>**\_WINBIO-VORGANG: \_ IDENTIFIZIEREN UND FREIGEBEN DES \_ \_ \_ TICKETS**
</dt> <dd> <dl> <dt>

27
</dt> <dt>



Reserviert. Dieser Wert wird ab Windows 10 unterstützt.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_VERIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_verify_and_release_ticket"></span>**WINBIO \_ OPERATION \_ VERIFY \_ AND \_ RELEASE \_ TICKET**
</dt> <dd> <dl> <dt>

28
</dt> <dt>



Reserviert. Dieser Wert wird ab Windows 10 unterstützt.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_MONITOR_PRESENCE"></span><span id="winbio_operation_monitor_presence"></span>**VORHANDENSEIN DES \_ WINBIO-VORGANGSMONITORS \_ \_**
</dt> <dd> <dl> <dt>

29
</dt> <dt>



Der Gesichtserkennungs- oder Irisüberwachungsmechanismus wurde aktiviert. Weitere Informationen finden Sie unter [**WinBioMonitorPresence**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence). Dieser Wert wird ab Windows 10 unterstützt.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_SELECT"></span><span id="winbio_operation_enroll_select"></span>**WINBIO \_ OPERATION \_ ENROLL \_ SELECT**
</dt> <dd> <dl> <dt>

30
</dt> <dt>



Eine Einzelperson aus einer Gruppe von Personen, die durch Daten im Beispielpuffer dargestellt werden, wurde als die zu registrierende Person angegeben. Weitere Informationen finden Sie unter [**WinBioEnrollSelect.**](/windows/desktop/api/winbio/nf-winbio-winbioenrollselect) Dieser Wert wird ab Windows 10 unterstützt.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                                                                                     |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (winbio.h für Clientanwendungen oder Winbio \_ adapters.h für Adapter einschließen)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Clientanwendungskonstanten](client-application-constants.md)
</dt> </dl>

 

 





