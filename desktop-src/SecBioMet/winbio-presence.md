---
title: WINBIO_PRESENCE -Struktur (Winbio \_ types.h)
description: Enthält Informationen über das Vorhandensein einer Person, deren Vorhandensein überwacht wird.
ms.assetid: 810D452E-DDFA-4AB2-AEFB-0C170C0C18D4
keywords:
- WINBIO_PRESENCE Struktur Windows Biometrieframework-API
- PWINBIO_PRESENCE Strukturzeiger für Windows Biometrieframework-API
topic_type:
- apiref
api_name:
- WINBIO_PRESENCE
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2671faaee7bc277f9389d7c993e4d511dac03db459755b40bf3f659ff5256a56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909578"
---
# <a name="winbio_presence-structure"></a>WINBIO \_ PRESENCE-Struktur

Enthält Informationen über das Vorhandensein einer Person, deren Vorhandensein überwacht wird.

## <a name="syntax"></a>Syntax


```C++
typedef struct _WINBIO_PRESENCE {
  WINBIO_BIOMETRIC_TYPE      Factor;
  WINBIO_BIOMETRIC_SUBTYPE   SubFactor;
  HRESULT                    Status;
  WINBIO_REJECT_DETAIL       RejectDetail;
  WINBIO_IDENTITY            Identity;
  ULONGLONG                  TrackingId;
  WINBIO_PROTECTION_TICKET   Ticket;
  WINBIO_PRESENCE_PROPERTIES Properties;
} WINBIO_PRESENCE, *PWINBIO_PRESENCE;
```



## <a name="members"></a>Member

<dl> <dt>

**Aspekt**
</dt> <dd>

Der biometrische Faktor, der verwendet wird, um das Vorhandensein der Person zu überwachen.

</dd> <dt>

**SubFactor**
</dt> <dd>

Der biometrische Unterfaktorqualifizierer für den biometrischen Faktor, der verwendet wird, um das Vorhandensein der Person zu überwachen.

</dd> <dt>

**Status**
</dt> <dd>

Der Status der Identifikationsprozedur für die Person.

</dd> <dt>

**RejectDetail**
</dt> <dd>

Zusätzliche Informationen zum Fehler beim Erkennen einer Person, einschließlich Feedback, das erklärt, wie der Fehler korrigiert werden kann.

</dd> <dt>

**Identität**
</dt> <dd>

Die Identität der Person, deren Vorhandensein überwacht wird, sobald diese Person identifiziert wurde.

</dd> <dt>

**TrackingId**
</dt> <dd>

Eine ganze Zahl, die vom Adapter generiert wird und die Person eindeutig identifiziert. Der Nachverfolgungsbezeichner, den der Adapter einer bestimmten Person zuteilt, ist garantiert konstant, solange diese Person im Kamerarahmen verbleibt.

</dd> <dt>

**Ticket**
</dt> <dd>

Reserviert. Legen Sie vom Adapter auf 0 fest.

</dd> <dt>

**Eigenschaften**
</dt> <dd>

Faktorspezifische Informationen zur Position einer Person.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die [**EngineAdapterIdentifyAll-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_all_fn) erstellt ein Array von **WINBIO \_ PRESENCE-Strukturen** und sendet dieses Array an den biometrischen Dienst. Der biometrische Dienst verwendet das Array, um sein internes Menschenmodell in der Nähe des Computers zu aktualisieren.

Abhängig von den Ergebnissen dieses Updates generiert der biometrische Dienst möglicherweise eine [**WINBIO \_ ASYNC \_ RESULT-Struktur**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) für die [**WinBioMonitorPresence-Funktion**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence) für alle Clients mit aktiven Anwesenheitsmonitoren. DAS **\_ WINBIO-ASYNCHRONE \_ ERGEBNIS. Das** Vorgangsmitglied der -Struktur enthält **WINBIO \_ OPERATION MONITOR \_ \_ PRESENCE** und **das WINBIO \_ ASYNC \_ RESULT. Der Parameter.MonitorPresence.ChangeType-Member** stellt zusätzliche Informationen zum Zustand der Person zur Verfügung.

Wenn eine Person, die der Engine-Adapter einem bestimmten Nachverfolgungsbezeichner zuteilt, zum ersten Mal im Eingabestream angezeigt wird, generiert der biometrische Dienst eine clientseitige [**WINBIO \_ ASYNC \_ RESULT-Struktur,**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) bei der **das WINBIO-ASYNCHRONE ERGEBNIS angezeigt \_ \_ wird. Der Parameter.MonitorPresence.ChangeType-Member** ist **WINBIO \_ CHANGE TYPE \_ \_ ARRIVAL.** Diese Struktur wird vor allen anderen **WINBIO \_ ASYNC \_ RESULT-Strukturen,** bei denen WINBIO ASYNC RESULT verwendet wird, an die Anwendungsrückruffunktion **oder \_ Anwendungsnachrichtenwarteschlange \_ gesendet. Parameters.MonitorPresence.PresenceArray** enthält eine **WINBIO \_ PRESENCE-Struktur** mit demselben Wert für **WINBIO \_ PRESENCE. TrackingId**.

Die folgenden Kombinationen von Werten im Array von **WINBIO \_ PRESENCE-Strukturen,** die **winbio \_ ASYNC \_ RESULT sind. Parameters.MonitorPresence.PresenceArray-Member** geben bestimmte Arten von Änderungen am Zustand einer Person an.

-   Wenn eine Person im Kamerarahmen sichtbar ist, die Engine jedoch weiterhin versucht, die Person zu identifizieren, verfügen die Member der **WINBIO \_ PRESENCE-Struktur** über die Werte in der folgenden Tabelle.

    

    | Member            | Wert                                                    |
    |-------------------|----------------------------------------------------------|
    | **TrackingId**    | Eine ganze Zahl, die die Person für die Engine identifiziert. |
    | **Status**        | **S \_ OK**                                                |
    | **Identity.Type** | **\_WINBIO-ID-TYP \_ \_ NULL**                               |

    

     

    In diesem Fall verlängert der biometrische Dienst die Ablaufzeit für die Person und generiert keine clientseitige [**WINBIO \_ ASYNC \_ RESULT-Struktur**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) für den Nachverfolgungsbezeichner, bei dem **das WINBIO \_ ASYNC \_ RESULT-Ergebnis ist. Der Parameter.MonitorPresence.ChangeType-Member** ist **WINBIO \_ CHANGE TYPE \_ \_ RECOGNIZE.**

    Wenn eine [**WINBIO \_ ASYNC \_ RESULT-Struktur**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) zum ersten Mal eine **WINBIO \_ PRESENCE-Struktur** enthält, bei der das **Status-Member** **S \_ OK** und das **Identity.Type-Member** **WINBIO ID TYPE \_ \_ \_ NULL** ist, nachdem eine oder mehrere **WINBIO ASYNC RESULT-Strukturen eine \_ \_** **WINBIO \_ PRESENCE-Struktur** mit einem **Status-Member** von **WINBIO \_ E BAD \_ \_ CAPTURE** enthalten haben, generiert der Anwesenheitsmonitor eine einzelne **WINBIO \_ ASYNC \_ RESULT-Struktur** für den Nachverfolgungsbezeichner, in dem **winbio ASYNC RESULT enthalten \_ \_ ist. Der Parameter.MonitorPresence.ChangeType-Member** ist **WINBIO \_ CHANGE TYPE \_ \_ TRACK.** Diese **WINBIO \_ ASYNC \_ RESULT-Struktur,** bei der **das \_ WINBIO-ASYNCHRONE \_ ERGEBNIS. Der Parameter.MonitorPresence.ChangeType-Member** ist **WINBIO \_ CHANGE TYPE \_ \_ TRACK** und informiert den Client darüber, dass das Problem, das den **WINBIO E BAD \_ \_ \_ CAPTURE-Fehler** verursacht hat, behoben wurde. Weitere Informationen zu den Umständen, in  denen eine **WINBIO \_ PRESENCE-Struktur** status member of **WINBIO \_ E \_ BAD \_ CAPTURE** auf hat, finden Sie in der Beschreibung darüber, wie der Engine-Adapter dem Benutzer Feedback zur Behebung von Erkennungsfehlern weiter unten in diesen Anmerkungen gibt.

-   Wenn eine Person im Kameraframe sichtbar ist, die Engine jedoch weiterhin versucht, die Person zu identifizieren, und dem Benutzer Feedback zur Behebung eines Erkennungsfehlers geben möchte, verfügen die Member der **WINBIO \_ PRESENCE-Struktur** über die Werte in der folgenden Tabelle.

    

    | Member                                                                                                      | Wert                                                                         |
    |-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
    | **TrackingId**                                                                                              | Eine ganze Zahl, die die Person für die Engine identifiziert.                      |
    | **Status**                                                                                                  | **WINBIO \_ E \_ BAD \_ CAPTURE**                                                   |
    | **Identity.Type**                                                                                           | **\_WINBIO-ID-TYP \_ \_ NULL**                                                    |
    | **Properties.FacialFeatures.BoundingBox**, wenn der Wert von **Factor** **WINBIO \_ TYPE FACIAL \_ FEATURES \_ ist** | Die Position des Gesichts der Person innerhalb des Kamerarahmens.           |
    | **Properties.Iris.BoundingBox**, wenn der Wert von **Factor** **WINBIO \_ TYPE IRIS \_ ist**                       | Die Position der Schwertlilien oder Schwertlilien der Person innerhalb des Kamerarahmens. |

    

     

    In diesem Fall verlängert der biometrische Dienst die Ablaufzeit für die Person und generiert eine [**WINBIO \_ ASYNC \_ RESULT-Struktur**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) für den Nachverfolgungsbezeichner, bei dem **winbio \_ ASYNC \_ RESULT verwendet wird. Der Parameter.MonitorPresence.ChangeType-Member** ist **WINBIO \_ CHANGE TYPE \_ \_ TRACK.**

-   Wenn eine Person im Kameraframe sichtbar ist und der Engine-Adapter die Identität der Person bestimmt, verfügen die Member der **WINBIO \_ PRESENCE-Struktur** über die Werte in der folgenden Tabelle.

    

    | Member                        | Wert                                                    |
    |-------------------------------|----------------------------------------------------------|
    | **TrackingId**                | Eine ganze Zahl, die die Person für die Engine identifiziert. |
    | **Status**                    | **S \_ OK**                                                |
    | **Identity.Type**             | **\_ \_ WINBIO-ID-TYP-SID \_**                                |
    | **Identity.Value.AccountSid** | Die Sicherheits-ID (SID) der Einzelperson.         |

    

     

    In diesem Fall ordnet der biometrische Dienst den Nachverfolgungsbezeichner der SID für die Person zu und generiert eine clientseitige [**WINBIO \_ ASYNC \_ RESULT-Struktur**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) für den Nachverfolgungsbezeichner, bei dem **das WINBIO \_ ASYNC \_ RESULT-Ergebnis ist. Der Parameter.MonitorPresence.ChangeType-Member** ist **WINBIO \_ CHANGE TYPE \_ \_ RECOGNIZE.** Der biometrische Dienst generiert keine zusätzlichen clientseitigen **WINBIO \_ ASYNC \_ RESULT-Strukturen** für den Nachverfolgungsbezeichner, es sei denn, die Person verlässt den Kamerarahmen.

-   Wenn eine Person im Kameraframe sichtbar ist, der Engine-Adapter jedoch sicher bestimmt, dass die Person nicht registriert ist, verfügen die Member der **WINBIO \_ PRESENCE-Struktur** über die Werte in der folgenden Tabelle.

    

    | Member            | Wert                                                    |
    |-------------------|----------------------------------------------------------|
    | **TrackingId**    | Eine ganze Zahl, die die Person für die Engine identifiziert. |
    | **Status**        | **WINBIO \_ E \_ UNKNOWN \_ ID**                               |
    | **Identity.Type** | **\_WINBIO-ID-TYP \_ \_ NULL**                               |

    

     

    In diesem Fall ordnet der biometrische Dienst den Nachverfolgungsbezeichner der Person der Identität UNKNOWN zu und generiert eine clientseitige [**WINBIO \_ ASYNC \_ RESULT-Struktur**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) für den Nachverfolgungsbezeichner, bei dem **das WINBIO \_ ASYNC \_ RESULT-Ergebnis ist. Der Parameter.MonitorPresence.ChangeType-Member** ist **WINBIO \_ CHANGE TYPE \_ \_ RECOGNIZE.** Der biometrische Dienst generiert keine zusätzlichen clientseitigen **WINBIO \_ ASYNC \_ RESULT-Strukturen** für den Nachverfolgungsbezeichner, es sei denn, die Person verlässt den Kamerarahmen.

Wenn eine Person, die der Engine-Adapter einem bestimmten Nachverfolgungsbezeichner zulässt, den Kamerarahmen verlässt und nicht mehr in den Werten angezeigt wird, die die [**EngineAdapterIdentifyAll-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_all_fn) zurückgibt, läuft der Nachverfolgungsbezeichner schließlich ab. Wenn der Nachverfolgungsbezeichner abläuft, generiert der biometrische Dienst eine clientseitige [**WINBIO \_ ASYNC \_ RESULT-Struktur,**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) bei der **WINBIO \_ ASYNC \_ RESULT verwendet wird. Der Parameter.MonitorPresence.ChangeType-Member** ist **WINBIO \_ CHANGE \_ \_ TYPEENCE**. Der Engine-Adapter kann verhindern, dass der biometrische Dienst diese Struktur mit dem **WINBIO \_ CHANGE \_ \_ TYPE-WERT FÜR DIE VERWENDUNG GENERIERT,** indem er eine **WINBIO \_ PRESENCE-Struktur** in das Array eingibt, das **EngineAdapterIdentifyAll** zurückgibt, wobei WINBIO PRESENCE zurückgegeben **\_ wird. Statusmitglied** ist **S \_ OK** und **WINBIO \_ PRESENCE. Der Identity.Type-Member** ist **WINBIO \_ ID TYPE \_ \_ NULL,** wie weiter oben in diesen Anmerkungen beschrieben. Diese Aktion verlängert die Ablaufzeit für den Nachverfolgungsbezeichner, ohne clientseitige Aktivitäten zu verursachen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Nur Desktop-Apps\]<br/>                                                                                                                     |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (winbio.h für Clientanwendungen oder Winbio \_ adapters.h für Adapter enthalten)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_WINBIO-ASYNCHRONES \_ ERGEBNIS**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result)
</dt> <dt>

[**WinBioMonitorPresence**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence)
</dt> <dt>

[**EngineAdapterIdentifyAll**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_all_fn)
</dt> </dl>

 

 





