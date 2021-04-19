---
description: Ein Dienst kann sich registrieren, um gestartet oder angehalten zu werden, wenn ein Auslöserereignis auftritt.
ms.assetid: ca02a3ae-b16a-4427-b6db-b935c9cf23b3
title: Dienst Triggerereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdefd94b7896936f7ab4fc014647b08470611573
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360807"
---
# <a name="service-trigger-events"></a>Dienst Triggerereignisse

Ein Dienst kann sich registrieren, um gestartet oder angehalten zu werden, wenn ein Auslöserereignis auftritt. Dadurch entfällt die Notwendigkeit, Dienste zu starten, wenn das System gestartet wird, oder Dienste, die auf ein Ereignis warten oder es aktiv warten. ein Dienst kann bei Bedarf gestartet werden, anstatt automatisch zu starten, ob eine Arbeit durchzuführen ist. Beispiele für vordefinierte Triggerereignisse sind die Ankunft eines Geräts einer angegebenen Geräteschnittstellen Klasse oder die Verfügbarkeit eines bestimmten Firewallports. Ein Dienst kann sich auch für ein benutzerdefiniertes Ereignis registrieren, das von einem ETW-Anbieter ( [Ereignis Ablauf Verfolgung für Windows](../etw/event-tracing-portal.md) ) generiert wurde.

**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dienst Triggerereignisse werden erst ab Windows Server 2008 R2 und Windows 7 unterstützt.

Ein-Triggern besteht aus einem triggerereignistyp, einem triggerereignisuntertyp, der Aktion, die als Reaktion auf das Triggerereignis ausgeführt werden soll, und (bei bestimmten triggerereignistypen) einem oder mehreren triggerspezifischen Datenelementen. Der Untertyp und die triggerspezifischen Datenelemente geben zusammen die Bedingungen an, mit denen der Dienst des Ereignisses benachrichtigt wird. Das Format eines Datenelements hängt vom Typ des auslöserereignisses ab. ein Datenelement kann Binärdaten, eine Zeichenfolge oder eine mehrteilige Zeichenfolge sein. Zeichen folgen müssen Unicode sein. ANSI-Zeichen folgen werden nicht unterstützt.

Um für Triggerereignisse zu registrieren, ruft der Dienst [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) mit **Service \_ config- \_ \_ Triggerinformationen** auf und stellt eine dienstinganformationen- [**\_ \_ Informations**](/windows/desktop/api/winsvc/ns-winsvc-service_trigger_info) Struktur bereit. Die **Dienst \_ - \_ auslöserinfo** -Struktur verweist auf ein Array von [**Dienst- \_ auslöserstrukturen**](/windows/desktop/api/winsvc/ns-winsvc-service_trigger) , die jeweils einen-Parameter angeben

Die angegebene Triggeraktion wird ausgeführt, wenn die Auslöserbedingung beim Starten des Systems true ist, oder wenn die Triggerbedingung bei Ausführung des Systems true wird. Wenn z. b. ein Dienst registriert wird, wenn ein bestimmtes Gerät verfügbar ist, wird der Dienst gestartet, wenn das System gestartet wird, wenn das Gerät bereits an den Computer angeschlossen ist. der Dienst wird gestartet, wenn das Gerät eintrifft, wenn der Benutzer das Gerät in den Betrieb einfügt, während das System ausgeführt wird.

Wenn ein triggerspezifische Datenelemente enthält, wird die Triggeraktion nur dann durchgeführt, wenn das Datenelement, das das Triggerereignis begleitet, mit einem der Datenelemente übereinstimmt, die der Dienst mit dem-Triggerwert angegeben hat. Der binäre Datenabgleich erfolgt durch einen bitweisen Vergleich. Beim Zeichen folgen Vergleich wird die Groß-/Kleinschreibung beachtet Wenn das Datenelement eine mehrteilige Zeichenfolge ist, müssen alle Zeichen folgen in der mehrteiligen Zeichenfolge entsprechen.

Wenn ein Dienst als Antwort auf ein Triggerereignis gestartet wird, empfängt der Dienst das **Dienst \_ Trigger- \_ \_ Argument Started** als *argv* \[ 1 \] in seiner [*ServiceMain*](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) -Rückruffunktion. *Argv* \[ 0 \] ist immer der Kurzname des Dienstanbieter.

Ein Dienst, der als Antwort auf ein auslösereignis registriert wird, wird möglicherweise nach einem Leerlauf Timeout angehalten, wenn der Dienst nicht ausgeführt werden kann. Ein Dienst, der sich selbst beendet, muss darauf vorbereitet sein, **Service \_ Control- \_ triggerEvent** -Steuerungsanforderungen zu verarbeiten, die ankommen, während der Dienst sich selbst beendet. Der SCM sendet bei jedem Auftreten eines neuen triggerereignisses, wenn der Dienst ausgeführt wird, eine Dienst Steuerungs Anforderung für das **\_ \_ triggerEvent** -Steuerelement. Um den Verlust von Triggerereignissen zu vermeiden, sollte der Dienst das Herunterfahren des Fehlers für jede **\_ Dienststeuerungs- \_ triggerEvent** -Steuerungs Anforderung zurückgeben, die eingeht, während der Dienst von der Ausführung zu "beendet" übergeht. **\_ \_ \_** Dadurch wird der SCM angewiesen, Triggerereignisse in die Warteschlange zu stellen und zu warten, bis der Dienst beendet wird. Der SCM führt dann die Aktion aus, die dem Ereignis in der Warteschlange zugeordnet ist, beispielsweise das Starten des Dienstanbieter.

Wenn der Dienst für die erneute Verarbeitung von Triggerereignissen bereit ist, wird das **Dienst \_ Accept- \_ triggerEvent** in der vom Steuerelement akzeptierten Maske in einem Aufrufen von [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)festgelegt. Dies erfolgt in der Regel, wenn der Dienst **SetServiceStatus** aufruft, während der **Dienst \_ ausgeführt** wird. Der SCM gibt dann eine **Dienst \_ Steuerungs \_ triggerEvent** -Anforderung für jedes Trigger-Ereignis in der Warteschlange aus, bis die Warteschlange leer ist.

Ein Dienst, für den abhängige Dienste ausgeführt werden, kann nicht als Antwort auf ein Auslöserereignis beendet werden.

Auslösende-und triggeranhalte-Anforderungen sind unter wenig Arbeitsspeicher nicht garantiert.

Verwenden Sie die [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) -Funktion, um die triggerereigniskonfiguration eines dienstangs abzurufen

Das SC-Tool (sc.exe) kann verwendet werden, um die Triggerereignisse eines Dienstanbieter an der Eingabeaufforderung zu konfigurieren oder abzufragen. Verwenden Sie die Option **TriggerInfo** , um einen Dienst so zu konfigurieren, dass er als Reaktion auf ein Triggerereignis gestartet oder beendet wird. Verwenden Sie die Option **qtriggerinfo, um die triggerkonfiguration** eines Dienstanbieter abzufragen.

Im folgenden Beispiel wird die auslöserkonfiguration des W32Time-Dienstanbieter abgefragt, die so konfiguriert ist, dass gestartet wird, wenn der Computer einer Domäne hinzugefügt wird.

``` syntax
C:\>sc qtriggerinfo w32time
[SC] QueryServiceConfig2 SUCCESS

SERVICE_NAME: w32time

        START SERVICE
          DOMAIN JOINED STATUS         : 1ce20aba-9851-4421-9430-1ddeb766e809 [DOMAIN JOINED]
        STOP SERVICE
          DOMAIN JOINED STATUS         : ddaf516e-58c2-4866-9574-c3b615d42ea1 [NOT DOMAIN JOINED]
```

Im folgenden Beispiel wird die auslöserkonfiguration des Tablet Input-diensdienstanbieter abgefragt, die für den Start konfiguriert ist, wenn ein HID-Gerät mit der **GUID** {4d1e55b2-f16f-11CF-88cb-001111000030} und einer der angegebenen versteckten Geräte-IDs eintreffen.

``` syntax
C:\>sc qtriggerinfo tabletinputservice
[SC] QueryServiceConfig2 SUCCESS

SERVICE_NAME: tabletinputservice

        START SERVICE
          DEVICE INTERFACE ARRIVAL     : 4d1e55b2-f16f-11cf-88cb-001111000030 [INTERFACE CLASS GUID]
            DATA                       : HID_DEVICE_UP:000D_U:0001
            DATA                       : HID_DEVICE_UP:000D_U:0002
            DATA                       : HID_DEVICE_UP:000D_U:0003
            DATA                       : HID_DEVICE_UP:000D_U:0004
```

 

 
