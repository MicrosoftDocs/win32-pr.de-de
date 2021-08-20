---
title: Fehler
description: In diesem Abschnitt wird ein Fehler beschrieben, der bei Windows Webdienstfunktionen aufgrund eines Fehlers beim Ausführen des Befehls auftreten kann.
ms.assetid: 2e5b853f-589c-4f89-9d7e-cd02263a2247
keywords:
- Fehlerwebdienste für Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a08a6371dcc5265239c6a25ce0c01075cff3ae12533862ed8a1cbbbe7aba705
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026528"
---
# <a name="errors"></a>Fehler

In diesem Abschnitt wird ein Fehler beschrieben, der bei Windows Webdienstfunktionen aufgrund eines Fehlers beim Ausführen des Befehls auftreten kann.

-   [Out-Parameter](#out-parameters)
-   [Fehlercodes](#error-codes)
-   [Umfangreiche Fehler](#rich-errors)
-   [Fehler und Fehler](#faults-and-errors)
-   [Sprachbezogene Fehlerinformationen](#language-sensitive-error-information)
-   [Kanonische Fehlercodes](#canonical-error-codes)
-   [Ungültige API-Nutzung](#invalid-api-usage)
-   [Sicherheit](#security)

## <a name="out-parameters"></a>Out-Parameter

Im Allgemeinen wird der Wert von out-Parametern nicht geändert, wenn eine Funktion fehlschlägt.

Es gibt einige Instanzen, in denen out-Parameter geändert werden, wenn die Funktion fehlschlägt. Diese Fälle werden explizit in der Dokumentation für jeden Parameter genannt. Wenn in der Dokumentation nichts über das Ändern von Out-Parametern im Falle eines Fehlers erwähnt wird, können Sie sicher davon ausgehen, dass die Funktion sie nicht ändert.

## <a name="error-codes"></a>Fehlercodes

Alle Fehlerrückgabecodes sind HRESULTs. Diese API definiert einen Satz von HRESULTs im FACILITY \_ WEBSERVICES-Bereich, gibt aber auch Fehler zurück, die an anderer Stelle in der Windows-API definiert sind.

Informationen dazu, welche Fehlercodes zurückgegeben werden, finden Sie in der Dokumentation zu bestimmten APIs. Die Liste soll nicht für jede API vollständig sein, sondern eine Liste von Fehlercodes, für die es gängige Szenarien für die explizite Behandlung gibt. Ein Aufrufer sollte immer davon ausgehen, dass andere Fehlercodes von jeder API aus möglich sind.

Diese API definiert eine relativ kleine Anzahl von Fehlercodes, die Szenarien entsprechen, in denen ein Programm basierend auf dem Fehler Maßnahmen ergreifen möchte. Fehlercodes allein sind möglicherweise nicht ausreichend, um zu ermitteln, was schief gelaufen ist, oder um dem Benutzer eine gute Beschreibung des Problems bereitzustellen. Das beste Verständnis des Problems ergibt sich aus der Verwendung umfangreicher Fehler, wie unten beschrieben.

## <a name="rich-errors"></a>Umfangreiche Fehler

Zusätzlich zur Rückgabe eines Fehlercodes kann ein Aufrufer optional umfangreiche Fehlerinformationen für jeden API-Aufruf anfordern, indem er ein [WS \_ ERROR-Objekt](ws-error.md) ungleich **NULL** übergibt. Verwenden Sie [**WsCreateError,**](/windows/desktop/api/WebServices/nf-webservices-wscreateerror)um ein Fehlerobjekt zu erstellen. Wenn ein Fehler auftritt, füllt die API, die den Fehler verursacht hat, das Fehlerobjekt mit zusätzlichem Kontext zur Fehlersituation. Wenn kein Fehler auftritt, bleibt das Fehlerobjekt unverändert. Das Übergeben eines **NULL-Fehlerobjekts** gibt an, dass der Aufrufer nicht an umfangreichen Fehlerinformationen interessiert ist. Aufgerufene (einschließlich Rückrufe) müssen darauf vorbereitet sein, **NULL-Fehlerobjekte** zu behandeln.

Beachten Sie, dass das gleiche Fehlerobjekt für mehrere API-Aufrufe verwendet werden kann, aber nur für jeweils einen API-Aufruf verwendet werden kann (da es sich um einen einzelnen Thread handelt). Jedes Mal, wenn ein Fehler auftritt, werden Fehlerinformationen an das Fehlerobjekt angefügt. Wenn eine Aufrufkette entladen wird, können mehrere Funktionen dem Fehlerobjekt Informationen hinzufügen, um zusätzlichen Kontext zum Fehler bereitzustellen. Verwenden Sie [**WsResetError**](/windows/desktop/api/WebServices/nf-webservices-wsreseterror), um den Inhalt des Fehlerobjekts zu löschen, bevor es wiederverwendet wird (nachdem ein Fehler aufgetreten ist). Wenn kein Fehler auftritt, ist es nicht erforderlich, das Fehlerobjekt zurückzusetzen, bevor es wiederverwendet wird.

Umfassende Fehlerinformationen umfassen Folgendes:

-   Ein Satz von Eigenschaftswerten, die zusätzliche Informationen zum Fehler bereitstellen, falls vorhanden. Weitere Informationen finden Sie unter WS ERROR PROPERTY ( [**\_ WS-FEHLEREIGENSCHAFT). \_**](/windows/desktop/api/WebServices/ns-webservices-ws_error_property)
-   Null oder mehr Fehlerzeichenfolgen. Die Zeichenfolgen werden mithilfe von [**WsAddErrorString**](/windows/desktop/api/WebServices/nf-webservices-wsadderrorstring)hinzugefügt und können mithilfe von [**WsGetErrorString**](/windows/desktop/api/WebServices/nf-webservices-wsgeterrorstring)abgefragt werden. Die Anzahl der Zeichenfolgen kann mithilfe von [**WS \_ ERROR PROPERTY STRING \_ \_ \_ COUNT**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id)abgefragt werden.

## <a name="faults-and-errors"></a>Fehler und Fehler

Informationen zur Beziehung zwischen Fehlern und Fehlern finden Sie unter [Fehler.](faults.md)

## <a name="language-sensitive-error-information"></a>Sprachbezogene Fehlerinformationen

Beim Erstellen eines Fehlerobjekts wird die LANGID der gewünschten Sprachübersetzung für Fehlerinformationen angegeben. Dies wird beim Hinzufügen von Fehlerinformationen zum Fehlerobjekt verwendet.

Dieser Sprachwert kann mit [**WS \_ ERROR \_ PROPERTY \_ LANGID**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id)abgerufen oder festgelegt werden.

## <a name="canonical-error-codes"></a>Kanonische Fehlercodes

Diese API stellt einen kanonischen Satz von Fehlercodes (WS E) bereit, mit denen \_ \_ \* verschiedene Kommunikationstechnologien verwendet werden können, ohne von den spezifischen Fehlercodes der spezifischen zugrunde liegenden Implementierung abhängig zu sein. Eine vollständige Liste dieser Fehlercodes finden Sie unter [Windows Web Services-Rückgabewerte.](windows-web-services-return-values.md)

Dies ermöglicht z. B. einem Programm, den Fehlercode **WS \_ E ENDPOINT NOT \_ \_ \_ FOUND** zu überprüfen, ob TCP, UDP oder HTTP verwendet wird, und einige Maßnahmen zu ergreifen (z. B. den Versuch, einen anderen Endpunkt zu verwenden).

Wenn ein implementierungsspezifischer Fehlercode einem kanonischen Fehler zugeordnet wird, wird der ursprüngliche Fehlercode im Fehlerobjekt gespeichert und kann zu Diagnosezwecken weiterhin verwendet werden. Weitere Informationen finden Sie unter [**WS \_ ERROR PROPERTY ORIGINAL ERROR \_ \_ \_ \_ CODE.**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id)

## <a name="invalid-api-usage"></a>Ungültige API-Nutzung

Die folgenden Fehlercodes sind für ungültige API-Nutzung reserviert und werden unter anderen Umständen nicht zurückgegeben. Wenn einer dieser Fehler zurückgegeben wird, kann dies ein Hinweis auf einen Anwendungsfehler sein.

-   **UNGÜLTIGER WS \_ \_ \_ E-VORGANG**
-   **E \_ INVALIDARG**

Die folgenden Enumerationen sind Teil der Ablaufverfolgung:

-   [**WS \_ ERROR PROPERTY ID (WS-FEHLEREIGENSCHAFTS-ID) \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id)
-   [**\_WS-AUSNAHMECODE \_**](/windows/desktop/api/WebServices/ne-webservices-ws_exception_code)

Die folgenden Fehlercodes sind Teil der Ablaufverfolgung:

-   **CERT \_ E \_ CN \_ NO \_ MATCH**
-   **CERT \_ E \_ EXPIRED**
-   **CERT \_ E \_ UNTRUSTEDROOT**
-   **CERT \_ E \_ WRONG \_ USAGE**
-   **CRYPT \_ E \_ REVOCATION \_ OFFLINE**
-   **E \_ INVALIDARG**
-   **E \_ OUTOFMEMORY**
-   **VERWENDETE \_ \_ WS-E-ADRESSE \_ \_**
-   **\_WS-E-ADRESSE \_ \_ NICHT \_ VERFÜGBAR**
-   **WS \_ E \_ ENDPOINT \_ ACCESS \_ DENIED**
-   **WS E ENDPOINT ACTION NOT SUPPORTED (WS \_ \_ E-ENDPUNKTAKTION \_ \_ NICHT \_ UNTERSTÜTZT)**
-   **WS \_ \_ E-ENDPUNKT \_ GETRENNT**
-   **FEHLER BEIM WS \_ \_ E-ENDPUNKT \_**
-   **EMPFANGENER WS \_ \_ E-ENDPUNKTFEHLER \_ \_**
-   **WS \_ \_ E-ENDPUNKT \_ NICHT \_ VERFÜGBAR**
-   **WS \_ \_ E-ENDPUNKT \_ NICHT \_ GEFUNDEN**
-   **WS \_ \_ E-ENDPUNKT \_ ZU \_ AUSGELASTET**
-   **WS \_ \_ E-ENDPUNKT \_ NICHT ERREICHBAR**
-   **WS \_ E \_ \_ UNGÜLTIGE \_ ENDPUNKT-URL**
-   **WS \_ E \_ UNGÜLTIGES \_ FORMAT**
-   **UNGÜLTIGER WS \_ \_ \_ E-VORGANG**
-   **WS \_ E WIRD NICHT \_ \_ UNTERSTÜTZT**
-   **WS \_ E KEINE ÜBERSETZUNG \_ \_ \_ VERFÜGBAR**
-   **WS \_ E \_ NUMERIC \_ OVERFLOW**
-   **FEHLER BEIM WS \_ \_ E-OBJEKT \_**
-   **WS \_ \_ E-VORGANG \_ ABGEBROCHEN**
-   **WS \_ \_ E-VORGANG \_ ABGEBROCHEN**
-   **TIME OUT FÜR WS \_ \_ E-VORGANG \_ \_**
-   **WS \_ E \_ OTHER**
-   **WS \_ E \_ PROXY \_ ACCESS \_ DENIED**
-   **WS \_ E \_ PROXY \_ FAILURE**
-   **WS \_ \_ E-PROXY \_ ERFORDERT \_ GRUNDLEGENDE \_ AUTHENTIFIZIERUNG**
-   **WS \_ \_ E-PROXY \_ ERFORDERT \_ \_ DIGESTAUTHENTIFIZIERUNG**
-   **WS \_ \_ E-PROXY \_ ERFORDERT \_ \_ NEGOTIATE-AUTHENTIFIZIERUNG**
-   **WS \_ \_ E-PROXY \_ ERFORDERT \_ \_ NTLM-AUTHENTIFIZIERUNG**
-   **WS \_ \_ E-KONTINGENT \_ ÜBERSCHRITTEN**
-   **WS \_ \_ E-SICHERHEITSSYSTEMFEHLER \_ \_**
-   **WS \_ \_ E-SICHERHEITSTOKEN \_ \_ ABGELAUFEN**
-   **WS \_ \_ E-SICHERHEITSÜBERPRÜFUNGSFEHLER \_ \_**
-   **WS \_ E SERVER ERFORDERT GRUNDLEGENDE \_ \_ \_ \_ AUTHENTIFIZIERUNG**
-   **WS \_ E SERVER ERFORDERT \_ \_ \_ \_ DIGESTAUTHENTIFIZIERUNG**
-   **WS \_ E SERVER ERFORDERT NEGOTIATE \_ \_ \_ \_ AUTH**
-   **WS \_ E SERVER ERFORDERT \_ \_ \_ \_ NTLM-AUTHENTIFIZIERUNG**
-   **WS \_ S \_ ASYNC**
-   **WS \_ S \_ END**

Die folgenden Funktionen sind Teil der Ablaufverfolgung:

-   [**\_ \_ WS-FEHLEREIGENSCHAFTS-ID \_**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id)
-   [**\_WS-AUSNAHMECODE \_**](/windows/desktop/api/WebServices/ne-webservices-ws_exception_code)

Das folgende Handle ist Teil der Ablaufverfolgung:

-   [\_WS-FEHLER](ws-error.md)

Die folgende Struktur ist Teil der Ablaufverfolgung:

-   [**\_WS-FEHLEREIGENSCHAFT \_**](/windows/desktop/api/WebServices/ns-webservices-ws_error_property)

## <a name="security"></a>Sicherheit

Es gibt eine Reihe von Sicherheitsüberlegungen, die der Benutzer des Fehlerobjekts beachten sollte:

-   Das Fehlerobjekt kann nicht vertrauenswürdige Daten enthalten. Beispiele hierfür sind der WS FAULT und die Fehlerzeichenfolgen, die beide im Fehlerobjekt gespeichert werden können, basierend auf Informationen, die über einen nicht vertrauenswürdigen \_ Kanal empfangen werden. Der Benutzer des Fehlerobjekts sollte vorsichtig sein, wenn er die Informationen im Fehlerobjekt überprüft und basierend auf seinen Werten Entscheidungen trifft.
-   Ein Benutzer des Fehlerobjekts sollte [**WsResetError**](/windows/desktop/api/WebServices/nf-webservices-wsreseterror) aufrufen, nachdem er die Informationen zum Fehler überprüft hat. Wenn dies nicht geschieht, kann dies zu einer Speicherakhämation führen.
-   Ein Benutzer des Fehlerobjekts sollte sehr vorsichtig sein, wenn er den WS FULL FAULT DISCLOSURE-Wert der \_ \_ \_ [**WS \_ FAULT \_ DISCLOSURE-Enumeration**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_disclosure) verwendet, da der generierte Fehler private Informationen enthalten kann, die im Rahmen des Fehleraufzeichnungsprozesses gesammelt wurden.

 

 




