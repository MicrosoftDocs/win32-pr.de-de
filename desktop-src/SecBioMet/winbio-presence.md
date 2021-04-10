---
title: WINBIO_PRESENCE Struktur (winbio \_ types. h)
description: Enthält Informationen über das vorhanden sein einer Person, deren Anwesenheit überwacht wird.
ms.assetid: 810D452E-DDFA-4AB2-AEFB-0C170C0C18D4
keywords:
- WINBIO_PRESENCE Struktur Windows-Biometrieframework-API
- PWINBIO_PRESENCE Struktur Zeiger Windows-Biometrieframework API
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
ms.openlocfilehash: 8a4a917f09f419ce8dd5eb59c9c277293261bffa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103845"
---
# <a name="winbio_presence-structure"></a>Winbio- \_ Anwesenheits Struktur

Enthält Informationen über das vorhanden sein einer Person, deren Anwesenheit überwacht wird.

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

Der biometrische Faktor, der zum Überwachen des Vorhandenseins der einzelnen Person verwendet wird.

</dd> <dt>

**Teilfaktor**
</dt> <dd>

Der biometrische unter Faktor Qualifizierer für den biometrischen Faktor, der zum Überwachen des Vorhandenseins der Person verwendet wird.

</dd> <dt>

**Status**
</dt> <dd>

Der Status des Identifizierungs Verfahrens für die Person.

</dd> <dt>

**Rejectdetail**
</dt> <dd>

Weitere Informationen über den Fehler bei der Erkennung einer einzelnen Person, einschließlich des Feedbacks, das erläutert, wie Sie den Fehler beheben können.

</dd> <dt>

**Identität**
</dt> <dd>

Die Identität der Person, deren Anwesenheit überwacht wird, nachdem diese Person identifiziert wurde.

</dd> <dt>

**TrackingId**
</dt> <dd>

Eine ganze Zahl, die vom Adapter generiert wird und die einzelne eindeutig identifiziert. Die nach Verfolgungs-ID, die der Adapter einer bestimmten Person zuweist, ist garantiert konstant, solange diese Person im Kamera Rahmen verbleibt.

</dd> <dt>

**Ticket**
</dt> <dd>

Reserviert. Wird vom Adapter auf 0 festgelegt.

</dd> <dt>

**Eigenschaften**
</dt> <dd>

Faktor spezifische Informationen über die Position einer einzelnen Person.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die [**engineadapteridentifyall**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_all_fn) -Funktion erstellt ein Array von **winbio- \_ Anwesenheits** Strukturen und sendet dieses Array an den biometrischen Dienst. Der biometrische Dienst verwendet das Array, um das interne Modell der Menschen in der Nähe des Computers zu aktualisieren.

Abhängig von den Ergebnissen dieses Updates kann der biometrische Dienst eine [**winbio \_ Async- \_ Ergebnis**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) Struktur für die [**winbiomonitorpresence**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence) -Funktion für alle Clients mit aktiven Anwesenheits Monitoren generieren. Das asynchrone **winbio- \_ \_ Ergebnis. Der Vorgangs** -Member der-Struktur enthält die **Anwesenheit des winbio- \_ Vorgangs \_ Monitors \_** und das asynchrone **winbio- \_ \_ Ergebnis. Der Parameter. monitorpresence. ChangeType** -Member stellt zusätzliche Informationen über den Zustand der einzelnen Person bereit.

Wenn eine Person, die der Engine-Adapter einem bestimmten nach Verfolgungs Bezeichner zuordnet, zum ersten Mal im Eingabestream angezeigt wird, generiert der biometrische Dienst eine Client seitige winbio-asynchrone [**\_ \_ Ergebnis**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) Struktur, in der das **winbio \_ Async- \_ Ergebnis ist. Parameter. monitorpresence. ChangeType** -Member ist eine **winbio- \_ \_ Änderungstyp \_ Ankunft**. Diese Struktur wird an die Rückruffunktion der Anwendung oder an die Anwendungs Nachrichten Warteschlange gesendet, bevor alle anderen **winbio \_ Async- \_ Ergebnis** Strukturen, in denen das **winbio \_ Async- \_ Ergebnis vorliegt Parameters. monitorpresence. presencearray** enthält eine **winbio- \_ Anwesenheits** Struktur mit dem gleichen Wert für die **winbio- \_ Präsenz. TrackingID**.

Die folgenden Kombinationen von Werten im Array von **winbio- \_ Anwesenheits** Strukturen, die das **winbio \_ Async-Ergebnis hat \_ . Der Parameter. monitorpresence. presencearray** -Member zeigt bestimmte Arten von Änderungen im Zustand einer einzelnen Person an.

-   Wenn eine Person im Kamera Rahmen sichtbar ist, die Engine aber immer noch versucht, die Person zu identifizieren, haben die Elemente der **winbio- \_ Anwesenheits** Struktur die Werte in der folgenden Tabelle.

    

    | Member            | Wert                                                    |
    |-------------------|----------------------------------------------------------|
    | **TrackingId**    | Eine ganze Zahl, die die Person für die Engine identifiziert. |
    | **Status**        | **S \_ OK**                                                |
    | **Identity. Type** | **winbio- \_ ID- \_ Typ \_ null**                               |

    

     

    In diesem Fall erweitert der biometrische Dienst die Ablaufzeit für die Einzelperson und generiert keine Client seitige winbio-asynchrone [**\_ \_ Ergebnis**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) Struktur für den nach Verfolgungs Bezeichner, in dem sich das **winbio \_ Async- \_ Ergebnis befindet. Der Parameter. monitorpresence. ChangeType** -Member ist **vom winbio- \_ \_ Änderungstyp " \_ erkennen**".

    Beim ersten Mal, wenn [**eine winbio \_ Async- \_ Ergebnis**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) Struktur eine **winbio- \_ Anwesenheits** Struktur enthält, bei der das **statusmember** **S \_ OK** und die **Identität ist. Typmember** ist ein **winbio-ID- \_ \_ Typ \_ null** , nachdem mindestens eine **winbio- \_ Async- \_ Ergebnis** Struktur eine **winbio- \_ Anwesenheits** Struktur mit einem **Status** Mitglied von **winbio E ungültige \_ \_ \_ Erfassung** enthielt. der Anwesenheits Monitor generiert eine einzelne **winbio \_ Async- \_ Ergebnis** Struktur für die nach Verfolgungs-ID, bei der das asynchrone **winbio-Ergebnis ist \_ \_ . Parameter. monitorpresence. ChangeType** -Member ist ein **winbio- \_ \_ Änderungstyp \_ Track**. Diese **winbio \_ Async- \_ Ergebnis** Struktur, in der das **winbio \_ Async-Ergebnis ist \_ . Der Parameter. monitorpresence. ChangeType** -Member ist ein **winbio- \_ \_ Änderungstyp \_** , der dem Client mitteilt, dass das Problem, das den Fehler aufgrund eines ungültigen **winbio- \_ \_ \_ Erfassungs** Fehlers verursacht hat Weitere Informationen zu den Fällen, in denen eine **winbio- \_ Anwesenheits** Struktur einen **Status** Mitglied von **winbio E ungültige \_ \_ \_ Erfassung** hat, finden Sie in der Beschreibung der Art und Weise, wie der Engine-Adapter dem Benutzer Feedback zur Behebung von Erkennungs Fehlern bietet, später in diesen hinweisen.

-   Wenn eine Person im Kamera Rahmen sichtbar ist, die Engine aber immer noch versucht, die Person zu identifizieren, und dem Benutzer Feedback zur Behebung eines Erkennungs Fehlers geben möchte, haben die Elemente der **winbio- \_ Anwesenheits** Struktur die Werte in der folgenden Tabelle.

    

    | Member                                                                                                      | Wert                                                                         |
    |-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
    | **TrackingId**                                                                                              | Eine ganze Zahl, die die Person für die Engine identifiziert.                      |
    | **Status**                                                                                                  | **winbio \_ E ungültige \_ \_ Erfassung**                                                   |
    | **Identity. Type**                                                                                           | **winbio- \_ ID- \_ Typ \_ null**                                                    |
    | **Properties. fakialfeatures. BoundingBox**, wenn der Wert des **Faktors** **winbio \_ - \_ typgesichts \_ Merkmale** ist | Die Position der Vorderseite der Person innerhalb des Kamera Rahmens.           |
    | **Properties. IRIS. BoundingBox**, wenn der Wert von **Faktor** **winbio- \_ Typ \_ IRIS** ist                       | Der Speicherort der Iris oder Irises der einzelnen im Kamera Rahmen. |

    

     

    In diesem Fall erweitert der biometrische Dienst die Ablaufzeit für die Einzelperson und generiert eine [**winbio \_ Async- \_ Ergebnis**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) Struktur für den nach Verfolgungs Bezeichner, in dem sich das **winbio \_ Async- \_ Ergebnis befindet. Parameter. monitorpresence. ChangeType** -Member ist ein **winbio- \_ \_ Änderungstyp \_ Track**.

-   Wenn eine Person im Kamera Rahmen sichtbar ist und der Engine-Adapter die Identität der einzelnen Person bestimmt, haben die Elemente der **winbio- \_ Anwesenheits** Struktur die Werte in der folgenden Tabelle.

    

    | Member                        | Wert                                                    |
    |-------------------------------|----------------------------------------------------------|
    | **TrackingId**                | Eine ganze Zahl, die die Person für die Engine identifiziert. |
    | **Status**                    | **S \_ OK**                                                |
    | **Identity. Type**             | **winbio- \_ ID- \_ Typ- \_ sid**                                |
    | **Identity. Value. AccountSid** | Die Sicherheits-ID (SID) der Person.         |

    

     

    In diesem Fall ordnet der biometrische Dienst den Überwachungs Bezeichner der sid für die Person zu und generiert eine Client seitige winbio-asynchrone [**\_ \_ Ergebnis**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) Struktur für den nach Verfolgungs Bezeichner, in dem sich das **winbio \_ Async- \_ Ergebnis befindet. Der Parameter. monitorpresence. ChangeType** -Member ist **vom winbio- \_ \_ Änderungstyp " \_ erkennen**". Der biometrische Dienst generiert keine zusätzlichen Client seitigen **winbio \_ Async- \_ Ergebnis** Strukturen für die nach Verfolgungs-ID, es sei denn, die Person verlässt den Kamera Rahmen.

-   Wenn eine Person im Kamera Rahmen sichtbar ist, der Engine-Adapter jedoch sicherstellt, dass die Person nicht registriert ist, haben die Elemente der **winbio- \_ Anwesenheits** Struktur die Werte in der folgenden Tabelle.

    

    | Member            | Wert                                                    |
    |-------------------|----------------------------------------------------------|
    | **TrackingId**    | Eine ganze Zahl, die die Person für die Engine identifiziert. |
    | **Status**        | **winbio \_ E \_ Unknown- \_ ID**                               |
    | **Identity. Type** | **winbio- \_ ID- \_ Typ \_ null**                               |

    

     

    In diesem Fall ordnet der biometrische Dienst die nach Verfolgungs-ID der Person der Identität unbekannt zu und generiert eine Client seitige winbio-asynchrone [**\_ \_ Ergebnis**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) Struktur für den nach Verfolgungs Bezeichner, in dem sich das asynchrone **winbio- \_ Ergebnis befindet \_ . Der Parameter. monitorpresence. ChangeType** -Member ist **vom winbio- \_ \_ Änderungstyp " \_ erkennen**". Der biometrische Dienst generiert keine zusätzlichen Client seitigen **winbio \_ Async- \_ Ergebnis** Strukturen für die nach Verfolgungs-ID, es sei denn, die Person verlässt den Kamera Rahmen.

Wenn eine Person, die der Engine-Adapter einem bestimmten nach Verfolgungs Bezeichner zuordnet, den Kamera Rahmen verlässt und in den von der [**engineadapteridentifyall**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_all_fn) -Funktion zurückgegebenen Werten nicht mehr angezeigt wird, läuft die nach Verfolgungs-ID schließlich ab. Wenn die nach Verfolgungs-ID abläuft, generiert der biometrische Dienst eine Client seitige [**winbio \_ Async- \_ Ergebnis**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) Struktur, in der das **winbio \_ Async- \_ Ergebnis ist. Parameter. monitorpresence. ChangeType** -Member ist ein **winbio- \_ \_ Änderungstyp \_**. Der Engine-Adapter kann verhindern, dass der biometrische Dienst diese Struktur mit dem Wert des Werts " **winbio- \_ \_ \_ Änderungstyp** " durch Einschließen einer **winbio- \_ Anwesenheits** Struktur in das Array, das **engineadapteridentifyall** zurückgibt, in der die **winbio-Präsenz zurückgibt \_ . Status** Mitglied ist **S \_ OK** und die **winbio- \_ Präsenz. Identity. Type** -Member ist der **winbio- \_ ID- \_ Typ \_ null** , wie zuvor in diesen Hinweisen beschrieben. Durch diese Aktion wird die Ablaufzeit für die nach Verfolgungs-ID erweitert, ohne dass eine Client seitige Aktivität verursacht wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2016 \[ -Desktop-Apps\]<br/>                                                                                                                     |
| Header<br/>                   | <dl> <dt>Winbio \_ types. h (Include winbio. h für Client Anwendungen oder winbio \_ Adapters. h für Adapter)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**winbio \_ Async- \_ Ergebnis**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result)
</dt> <dt>

[**Winbiomonitorpresence**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence)
</dt> <dt>

[**Engineadapteridentifyall**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_all_fn)
</dt> </dl>

 

 





