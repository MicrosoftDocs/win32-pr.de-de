---
title: WINBIO_PRESENCE-Struktur (Winbio \_ types.h)
description: Enthält Informationen über das Vorhandensein einer Person, deren Vorhandensein überwacht wird.
ms.assetid: 810D452E-DDFA-4AB2-AEFB-0C170C0C18D4
keywords:
- WINBIO_PRESENCE Struktur Windows Biometrieframework-API
- PWINBIO_PRESENCE Strukturzeiger Windows Biometrieframework-API
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

Der biometrische Faktor, der zum Überwachen des Vorhandenseins der Person verwendet wird.

</dd> <dt>

**SubFactor**
</dt> <dd>

Der biometrische Teilfaktorqualifizierer für den biometrischen Faktor, der zum Überwachen des Vorhandenseins der Person verwendet wird.

</dd> <dt>

**Status**
</dt> <dd>

Der Status der Identifikationsprozedur für die Person.

</dd> <dt>

**RejectDetail**
</dt> <dd>

Zusätzliche Informationen zum Fehler bei der Erkennung einer Person, einschließlich Feedback, in dem erläutert wird, wie der Fehler behoben werden kann.

</dd> <dt>

**Identität**
</dt> <dd>

Die Identität der Person, deren Vorhandensein überwacht wird, sobald diese Person identifiziert wurde.

</dd> <dt>

**TrackingId**
</dt> <dd>

Eine ganze Zahl, die vom Adapter generiert wird und die Person eindeutig identifiziert. Der Nachverfolgungsbezeichner, den der Adapter einer bestimmten Person zuweist, ist garantiert konstant, solange diese Person im Kamerarahmen verbleibt.

</dd> <dt>

**Ticket**
</dt> <dd>

Reserviert. Wird vom Adapter auf 0 festgelegt.

</dd> <dt>

**Eigenschaften**
</dt> <dd>

Faktorspezifische Informationen zur Position einer Einzelperson.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die [**EngineAdapterIdentifyAll-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_all_fn) erstellt ein Array von **WINBIO \_ PRESENCE-Strukturen** und sendet dieses Array an den biometrischen Dienst. Der biometrische Dienst verwendet das Array, um sein internes Modell von Menschen in der Nähe des Computers zu aktualisieren.

Abhängig von den Ergebnissen dieses Updates kann der biometrische Dienst eine [**WINBIO \_ ASYNC \_ RESULT-Struktur**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) für die [**WinBioMonitorPresence-Funktion**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence) für alle Clients mit Monitoren mit aktiver Präsenz generieren. Das **\_ WINBIO-ASYNCHRONE \_ ERGEBNIS. Der Vorgangsmember** der -Struktur enthält **WINBIO \_ OPERATION MONITOR \_ \_ PRESENCE** und das **WINBIO \_ ASYNC \_ RESULT. Parameters.MonitorPresence.ChangeType-Member** stellt zusätzliche Informationen zum Zustand der Einzelnen bereit.

Wenn eine Person, die der Engine-Adapter einem bestimmten Nachverfolgungsbezeichner zuweist, zum ersten Mal im Eingabestream angezeigt wird, generiert der biometrische Dienst eine clientseitige [**\_ WINBIO-ASYNC \_ RESULT-Struktur,**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) in der **WINBIO \_ ASYNC RESULT enthalten \_ ist. Parameters.MonitorPresence.ChangeType** Member ist **WINBIO \_ CHANGE TYPE \_ \_ ARRIVAL**. Diese Struktur wird an Ihre Anwendungsrückruffunktion oder Anwendungsnachrichtenwarteschlange vor allen anderen **WINBIO \_ ASYNC \_ RESULT-Strukturen** gesendet, bei denen **winbio \_ ASYNC \_ RESULT. Parameters.MonitorPresence.PresenceArray** enthält eine **WINBIO \_ PRESENCE-Struktur** mit dem gleichen Wert für **WINBIO \_ PRESENCE. TrackingId**.

Die folgenden Kombinationen von Werten im Array von **WINBIO \_ PRESENCE-Strukturen,** die das **WINBIO \_ ASYNC RESULT \_ aufweisen. Parameters.MonitorPresence.PresenceArray-Member** geben bestimmte Arten von Änderungen im Zustand einer Einzelperson an.

-   Wenn eine Person im Kamerarahmen sichtbar ist, die Engine jedoch weiterhin versucht, die Person zu identifizieren, verfügen die Member der **WINBIO \_ PRESENCE-Struktur** über die Werte in der folgenden Tabelle.

    

    | Member            | Wert                                                    |
    |-------------------|----------------------------------------------------------|
    | **TrackingId**    | Eine ganze Zahl, die die Person für die Engine identifiziert. |
    | **Status**        | **S \_ OK**                                                |
    | **Identity.Type** | **\_WINBIO-ID-TYP \_ \_ NULL**                               |

    

     

    In diesem Fall verlängert der biometrische Dienst die Ablaufzeit für die Person und generiert keine clientseitige [**\_ WINBIO-ASYNC \_ RESULT-Struktur**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) für den Nachverfolgungsbezeichner, bei dem **winbio \_ ASYNC \_ RESULT vorhanden ist. Parameters.MonitorPresence.ChangeType** member is **WINBIO \_ CHANGE TYPE \_ \_ RECOGNIZE**.

    Wenn eine [**WINBIO \_ ASYNC \_ RESULT-Struktur**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) zum ersten Mal eine **\_ WINBIO-PRESENCE-Struktur** enthält, bei der der **Statusmember** **S \_ OK** und der **Identity.Type-Member** **WINBIO ID TYPE \_ \_ \_ NULL** ist, nachdem eine oder mehrere **\_ WINBIO-ASYNC \_ RESULT-Strukturen** eine **WINBIO \_ PRESENCE-Struktur** mit einem **Statusmember** von **WINBIO \_ E BAD \_ \_ CAPTURE** enthalten haben, generiert der Anwesenheitsmonitor eine einzelne **WINBIO \_ ASYNC \_ RESULT-Struktur** für den Überwachungsbezeichner, bei dem das **WINBIO ASYNC RESULT enthalten \_ \_ ist. Parameters.MonitorPresence.ChangeType** member is **WINBIO \_ CHANGE TYPE \_ \_ TRACK**. Diese **WINBIO \_ ASYNC \_ RESULT-Struktur,** in der das **\_ WINBIO-ASYNCHRONE \_ ERGEBNIS enthalten ist. Parameters.MonitorPresence.ChangeType** member is **WINBIO \_ CHANGE TYPE \_ \_ TRACK** informiert den Client, dass das Problem, das den **WINBIO E BAD \_ \_ \_ CAPTURE-Fehler** verursacht hat, behoben wurde. Weitere Informationen zu den Umständen, unter denen eine **WINBIO \_ PRESENCE-Struktur** **den Statusmember** von **WINBIO \_ E BAD \_ \_ CAPTURE** aufweist, finden Sie in der Beschreibung dazu, wie der Engine-Adapter dem Benutzer Feedback zum Beheben von Erkennungsfehlern weiter unten in diesen Hinweisen bereitstellt.

-   Wenn eine Person im Kamerarahmen sichtbar ist, die Engine jedoch weiterhin versucht, die Person zu identifizieren, und dem Benutzer Feedback zur Behebung eines Erkennungsfehlers geben möchte, verfügen die Member der **WINBIO \_ PRESENCE-Struktur** über die Werte in der folgenden Tabelle.

    

    | Member                                                                                                      | Wert                                                                         |
    |-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
    | **TrackingId**                                                                                              | Eine ganze Zahl, die die Person für die Engine identifiziert.                      |
    | **Status**                                                                                                  | **WINBIO \_ E \_ BAD \_ CAPTURE**                                                   |
    | **Identity.Type**                                                                                           | **\_WINBIO-ID-TYP \_ \_ NULL**                                                    |
    | **Properties.FacialFeatures.BoundingBox**, wenn der Wert von **Factor** **WINBIO \_ TYPE FACIAL \_ \_ FEATURES** ist | Die Position des Gesichts des Einzelnen innerhalb des Kamerarahmens.           |
    | **Properties.Iris.BoundingBox**, wenn der Wert von **Factor** **WINBIO \_ TYPE \_ IRIS** ist                       | Die Position der Schwertlilien oder Schwertlilien des Einzelnen innerhalb des Kamerarahmens. |

    

     

    In diesem Fall verlängert der biometrische Dienst die Ablaufzeit für für die Person und generiert eine [**\_ WINBIO-ASYNC \_ RESULT-Struktur**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) für den Nachverfolgungsbezeichner, wobei **winbio \_ ASYNC \_ RESULT ist. Parameters.MonitorPresence.ChangeType** member is **WINBIO \_ CHANGE TYPE \_ \_ TRACK**.

-   Wenn eine Person im Kamerarahmen sichtbar ist und der Engine-Adapter die Identität der Person bestimmt, weisen die Member der **WINBIO \_ PRESENCE-Struktur** die Werte in der folgenden Tabelle auf.

    

    | Member                        | Wert                                                    |
    |-------------------------------|----------------------------------------------------------|
    | **TrackingId**                | Eine ganze Zahl, die die Person für die Engine identifiziert. |
    | **Status**                    | **S \_ OK**                                                |
    | **Identity.Type**             | **\_ \_ WINBIO-ID-TYP-SID \_**                                |
    | **Identity.Value.AccountSid** | Die Sicherheits-ID (SID) der Einzelperson.         |

    

     

    In diesem Fall ordnet der biometrische Dienst den Nachverfolgungsbezeichner der SID für die Person zu und generiert eine clientseitige [**WINBIO \_ ASYNC \_ RESULT-Struktur**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) für den Nachverfolgungsbezeichner, bei dem **winbio \_ ASYNC \_ RESULT. Parameters.MonitorPresence.ChangeType** member is **WINBIO \_ CHANGE TYPE \_ \_ RECOGNIZE**. Der biometrische Dienst generiert keine zusätzlichen clientseitigen **\_ WINBIO-ASYNC \_ RESULT-Strukturen** für den Nachverfolgungsbezeichner, es sei denn, die Person verlässt den Kamerarahmen.

-   Wenn eine Person im Kamerarahmen sichtbar ist, der Engine-Adapter jedoch bestimmt, dass die Person nicht registriert ist, weisen die Member der **WINBIO \_ PRESENCE-Struktur** die Werte in der folgenden Tabelle auf.

    

    | Member            | Wert                                                    |
    |-------------------|----------------------------------------------------------|
    | **TrackingId**    | Eine ganze Zahl, die die Person für die Engine identifiziert. |
    | **Status**        | **WINBIO \_ E \_ UNKNOWN \_ ID**                               |
    | **Identity.Type** | **\_WINBIO-ID-TYP \_ \_ NULL**                               |

    

     

    In diesem Fall ordnet der biometrische Dienst den Nachverfolgungsbezeichner der Person der Identität UNKNOWN zu und generiert eine clientseitige [**\_ WINBIO-ASYNC \_ RESULT-Struktur**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) für den Überwachungsbezeichner, wobei **winbio \_ ASYNC \_ RESULT ist. Parameters.MonitorPresence.ChangeType** member is **WINBIO \_ CHANGE TYPE \_ \_ RECOGNIZE**. Der biometrische Dienst generiert keine zusätzlichen clientseitigen **\_ WINBIO-ASYNC \_ RESULT-Strukturen** für den Nachverfolgungsbezeichner, es sei denn, die Person verlässt den Kamerarahmen.

Wenn eine Person, die vom Engine-Adapter einem bestimmten Nachverfolgungsbezeichner zugeordnet wird, den Kamerarahmen verlässt und in den Von der [**EngineAdapterIdentifyAll-Funktion**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_all_fn) zurückgegebenen Werten nicht mehr angezeigt wird, läuft der Nachverfolgungsbezeichner schließlich ab. Wenn der Nachverfolgungsbezeichner abläuft, generiert der biometrische Dienst eine clientseitige [**\_ WINBIO-ASYNC \_ RESULT-Struktur,**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) in der **das \_ WINBIO-ASYNCHRONE \_ ERGEBNIS vorhanden ist. Parameters.MonitorPresence.ChangeType-Member** ist **WINBIO \_ CHANGE TYPE \_ \_ VERÄNDERLICHKEIT**. Der Engine-Adapter kann verhindern, dass der biometrische Dienst diese Struktur mit dem **WINBIO \_ CHANGE TYPE \_ \_ ENTF-Wert** generiert, indem er eine **WINBIO \_ PRESENCE-Struktur** in das Array einschließt, das **EngineAdapterIdentifyAll** zurückgibt, wobei **winbio PRESENCE verwendet \_ wird. Statusmember** ist **S \_ OK** und **WINBIO \_ PRESENCE. Identity.Type-Member** ist **WINBIO \_ ID TYPE \_ \_ NULL,** wie weiter oben in diesen Hinweisen beschrieben. Diese Aktion verlängert die Ablaufzeit für den Nachverfolgungsbezeichner, ohne dass eine clientseitige Aktivität verursacht wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Nur Desktop-Apps\]<br/>                                                                                                                     |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (winbio.h für Clientanwendungen oder Winbio \_ adapters.h für Adapter einschließen)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**WINBIO \_ \_ ASYNC-ERGEBNIS**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result)
</dt> <dt>

[**WinBioMonitorPresence**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence)
</dt> <dt>

[**EngineAdapterIdentifyAll**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_all_fn)
</dt> </dl>

 

 





