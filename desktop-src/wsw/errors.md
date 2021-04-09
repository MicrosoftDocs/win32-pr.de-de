---
title: Errors
description: In diesem Abschnitt wird ein Fehler beschrieben, der von Windows-Webdienst Funktionen verursacht werden kann, da der Befehl nicht ausgeführt werden kann.
ms.assetid: 2e5b853f-589c-4f89-9d7e-cd02263a2247
keywords:
- Fehler-Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e70f10d673bf8f37664d792d8cf969f0329dc363
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855699"
---
# <a name="errors"></a>Errors

In diesem Abschnitt wird ein Fehler beschrieben, der von Windows-Webdienst Funktionen verursacht werden kann, da der Befehl nicht ausgeführt werden kann.

-   [Out-Parameter](#out-parameters)
-   [Fehlercodes](#error-codes)
-   [Rich-Error](#rich-errors)
-   [Fehler und Fehler](#faults-and-errors)
-   [Informationen zu sprach sensiblen Fehlern](#language-sensitive-error-information)
-   [Kanonische Fehler Codes](#canonical-error-codes)
-   [Ungültige API-Verwendung](#invalid-api-usage)
-   [Security](#security)

## <a name="out-parameters"></a>Out-Parameter

Als allgemeine Regel wird der Wert von out-Parametern nicht geändert, wenn eine Funktion fehlschlägt.

Es gibt einige Instanzen, bei denen out-Parameter geändert werden, wenn die Funktion fehlschlägt. Diese Fälle werden explizit in der Dokumentation für jeden Parameter genannt. Wenn in der Dokumentation nichts zum Ändern von Parametern im Fall eines Fehlers erwähnt wird, können Sie sicher davon ausgehen, dass Sie von der Funktion nicht geändert werden.

## <a name="error-codes"></a>Fehlercodes

Alle Fehlerrückgabe Codes sind HRESULTs. Diese API definiert einen Satz von HRESULTs im Bereich " \_ Webdienste" der Einrichtung, gibt jedoch auch Fehler zurück, die an anderer Stelle in der Windows-API definiert sind.

Informationen dazu, welche Fehlercodes zurückgegeben werden, finden Sie in der Dokumentation zu bestimmten APIs. Die Liste ist nicht für jede API vollständig vorgesehen, sondern eine Liste von Fehlercodes, für die häufige Szenarien für die explizite Behandlung vorhanden sind. Ein Aufrufer sollte immer davon ausgehen, dass andere Fehlercodes von jeder API aus möglich sind.

Diese API definiert eine relativ kleine Anzahl von Fehlercodes, die den Szenarien entsprechen, in denen ein Programm auf der Grundlage des Fehlers Maßnahmen ergreifen soll. Fehlercodes allein sind möglicherweise nicht ausreichend, um zu ermitteln, was schief gelaufen ist, oder um eine gute Beschreibung des Problems für den Benutzer bereitzustellen. Das beste Verständnis des Problems ist die Verwendung von Rich-Fehlern, wie unten beschrieben.

## <a name="rich-errors"></a>Rich-Error

Zusätzlich zur Rückgabe eines Fehlercodes kann ein Aufrufer optional umfassende Fehlerinformationen für jeden API-Aufruf anfordern, indem er ein[WS- \_ Fehler](ws-error.md) Objekt ungleich NULL übergibt. Verwenden Sie [**wscreateerror**](/windows/desktop/api/WebServices/nf-webservices-wscreateerror), um ein Fehler Objekt zu erstellen. Wenn ein Fehler auftritt, wird das Fehler Objekt von der API, die den Fehler verursacht hat, mit zusätzlichem Kontext zur Fehlersituation aufgefüllt. Wenn kein Fehler vorliegt, wird das Fehler Objekt nicht geändert. Das Übergeben eines **null** -Fehler Objekts gibt an, dass der Aufrufer nicht an umfangreichen Fehlerinformationen interessiert ist. Callees (einschließlich Rückrufe) müssen für die Behandlung von **null** -Fehler Objekten vorbereitet werden.

Beachten Sie, dass das gleiche Fehler Objekt für mehrere API-Aufrufe verwendet werden kann. es kann jedoch nur für einen API-Aufruf gleichzeitig verwendet werden (da es sich um einen Single Thread handelt). Jedes Mal, wenn ein Fehler auftritt, werden Fehlerinformationen an das Fehler Objekt angehängt. Wenn eine Aufrufkette entladen wird, können mehrere Funktionen dem Fehler Objektinformationen hinzufügen, um zusätzlichen Kontext zum Fehler bereitzustellen. Um den Inhalt des Error-Objekts vor der erneuten Verwendung zu löschen (nachdem ein Fehler aufgetreten ist), verwenden Sie [**wsreseterror**](/windows/desktop/api/WebServices/nf-webservices-wsreseterror). Wenn kein Fehler auftritt, muss das Fehler Objekt vor der erneuten Verwendung nicht zurückgesetzt werden.

Umfassende Fehlerinformationen bestehen aus folgendem:

-   Ein Satz von Eigenschafts Werten, die zusätzliche Informationen über den Fehler bereitstellen, falls vorhanden. Siehe [**WS \_ Error- \_ Eigenschaft**](/windows/desktop/api/WebServices/ns-webservices-ws_error_property).
-   NULL oder mehr Fehler Zeichenfolgen. Die Zeichen folgen werden mithilfe von [**wsadderrorstring**](/windows/desktop/api/WebServices/nf-webservices-wsadderrorstring)hinzugefügt und können mithilfe von [**wsgeterrorstring**](/windows/desktop/api/WebServices/nf-webservices-wsgeterrorstring)abgefragt werden. Die Anzahl der Zeichen folgen kann mithilfe der WS- [**\_ Fehler \_ Eigenschaft \_ Zeichen \_**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id)folgen Anzahl abgefragt werden.

## <a name="faults-and-errors"></a>Fehler und Fehler

Weitere Informationen zur Beziehung zwischen Fehlern und Fehlern finden Sie unter [Fehler](faults.md) .

## <a name="language-sensitive-error-information"></a>Informationen zu sprach sensiblen Fehlern

Beim Erstellen eines Fehler Objekts wird die langid der gewünschten Sprachübersetzung für Fehlerinformationen angegeben. Diese wird verwendet, wenn dem Fehler Objekt Fehlerinformationen hinzugefügt werden.

Dieser sprach Wert kann mithilfe der [**WS \_ Error- \_ Eigenschaft \_ LangID**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id)abgerufen oder festgelegt werden.

## <a name="canonical-error-codes"></a>Kanonische Fehler Codes

Diese API bietet eine kanonische Reihe von Fehlercodes (WS \_ E \_ \* ), mit denen unterschiedliche Kommunikationstechnologien verwendet werden können, ohne von den spezifischen Fehlercodes der spezifischen zugrunde liegenden Implementierung abhängig zu sein. Eine umfassende Liste dieser Fehlercodes finden Sie unter [Rückgabewerte für Windows-Webdienste](windows-web-services-return-values.md).

Dies ermöglicht beispielsweise einem Programm, zu überprüfen, ob der Fehlercode der **WS \_ E- \_ Endpunkt \_ nicht \_ gefunden** wurde, ob TCP, UDP oder http verwendet wird, und einige Aktionen auszuführen (z. b. der Versuch, einen anderen Endpunkt zu verwenden).

Wenn ein Implementierungs spezifischer Fehlercode einem kanonischen Fehler zugeordnet ist, wird der ursprüngliche Fehlercode im Error-Objekt gespeichert, und es kann weiterhin zu Diagnose Zwecken auf Sie zugegriffen werden. Weitere Informationen finden Sie im [**\_ \_ \_ ursprünglichen \_ Fehler \_ Code der WS Error-Eigenschaft**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id) .

## <a name="invalid-api-usage"></a>Ungültige API-Verwendung

Die folgenden Fehlercodes sind für eine ungültige API-Verwendung reserviert und werden in anderen Fällen nicht zurückgegeben. Wenn einer dieser Fehler zurückgegeben wird, ist dies möglicherweise ein Hinweis auf einen Anwendungsfehler.

-   **\_Ungültiger WS E- \_ \_ Vorgang**
-   **E \_ invalidArg**

Die folgenden Enumerationen sind Teil der Ablauf Verfolgung:

-   [**WS- \_ Fehler- \_ Eigenschaften- \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id)
-   [**WS- \_ Ausnahme \_ Code**](/windows/desktop/api/WebServices/ne-webservices-ws_exception_code)

Die folgenden Fehlercodes sind Teil der Ablauf Verfolgung:

-   **CERT \_ E \_ CN \_ No \_ Match**
-   **Zertifikat \_ E \_ abgelaufen**
-   **Zertifikat \_ E \_ nicht Treuhänder**
-   **\_ \_ falsche \_ Verwendung von CERT E**
-   **Crypt-Sperre \_ \_ \_ Offline**
-   **E \_ invalidArg**
-   **E \_ outo-Memory**
-   **\_verwendete WS E- \_ Adresse \_ \_**
-   **WS \_ E- \_ Adresse \_ nicht \_ verfügbar**
-   **WS \_ E- \_ Endpunkt \_ Zugriff \_ verweigert**
-   **WS \_ E \_ - \_ Endpunkt \_ Aktion \_ wird nicht unterstützt.**
-   **WS \_ E- \_ Endpunkt \_ getrennt**
-   **WS \_ E- \_ Endpunkt \_ Fehler**
-   **WS \_ E- \_ Endpunkt \_ Fehler \_ empfangen**
-   **WS \_ E- \_ Endpunkt \_ nicht \_ verfügbar**
-   **WS \_ E- \_ Endpunkt \_ nicht \_ gefunden**
-   **der WS \_ E- \_ Endpunkt ist \_ \_ ausgelastet.**
-   **WS \_ E- \_ Endpunkt \_ nicht erreichbar**
-   **\_ \_ ungültige \_ Endpunkt- \_ URL für WS E**
-   **\_Ungültiges WS E- \_ \_ Format**
-   **\_Ungültiger WS E- \_ \_ Vorgang**
-   **WS \_ E \_ \_ wird nicht unterstützt.**
-   **WS \_ E \_ keine \_ Übersetzung \_ verfügbar**
-   **\_numerischer WS E- \_ \_ Überlauf**
-   **Fehler beim WS \_ E- \_ Objekt. \_**
-   **WS \_ E- \_ Vorgang \_ abgebrochen**
-   **WS \_ E- \_ Vorgang \_ abgebrochen**
-   **Timeout bei WS \_ E- \_ Vorgang. \_ \_**
-   **\_sonstige WS E \_**
-   **WS \_ E- \_ Proxy \_ Zugriff \_ verweigert**
-   **WS \_ E- \_ Proxy \_ Fehler**
-   **der WS \_ E- \_ Proxy erfordert die Standard Authentifizierung \_ \_ \_ .**
-   **der WS \_ E- \_ Proxy erfordert eine Digest-Authentifizierung \_ \_ \_ .**
-   **WS \_ E- \_ Proxy \_ erfordert \_ Aushandlungs Authentifizierung \_ .**
-   **der WS \_ E- \_ Proxy erfordert die \_ \_ NTLM-Authentifizierung \_ .**
-   **WS \_ E- \_ Kontingent \_ überschritten**
-   **WS \_ E- \_ Sicherheits \_ System \_ Fehler**
-   **WS \_ E- \_ Sicherheits \_ Token \_ abgelaufen**
-   **WS \_ E-Fehler bei der \_ Sicherheits \_ Überprüfung \_**
-   **WS \_ E \_ Server \_ erfordert Standard Authentifizierung \_ \_ .**
-   **WS \_ E \_ Server \_ erfordert \_ Digest-Authentifizierung \_ .**
-   **WS \_ E \_ Server \_ erfordert \_ Aushandlungs Authentifizierung \_ .**
-   **WS \_ E \_ Server \_ erfordert \_ NTLM-Authentifizierung \_ .**
-   **WS \_ S \_ Async**
-   **WS \_ S- \_ Ende**

Die folgenden Funktionen sind Teil der Ablauf Verfolgung:

-   [**WS- \_ Fehler- \_ Eigenschaften- \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id)
-   [**WS- \_ Ausnahme \_ Code**](/windows/desktop/api/WebServices/ne-webservices-ws_exception_code)

Das folgende Handle ist Teil der Ablauf Verfolgung:

-   [WS- \_ Fehler](ws-error.md)

Die folgende Struktur ist Teil der Ablauf Verfolgung:

-   [**WS \_ Error- \_ Eigenschaft**](/windows/desktop/api/WebServices/ns-webservices-ws_error_property)

## <a name="security"></a>Sicherheit

Es gibt eine Reihe von Sicherheitsüberlegungen, die der Benutzer des Error-Objekts beachten sollte:

-   Das Error-Objekt enthält möglicherweise nicht vertrauenswürdige Daten. Beispiele hierfür sind: der WS \_ -Fehler und die Fehler Zeichenfolgen, die beide im Fehler Objekt gespeichert werden können, basierend auf Informationen, die über einen nicht vertrauenswürdigen Kanal empfangen werden. Der Benutzer des Error-Objekts sollte bei der Überprüfung der Informationen im Error-Objekt und beim Treffen von Entscheidungen auf Grundlage seiner Werte vorsichtig sein.
-   Ein Benutzer des Error-Objekts sollte [**wsreseterror**](/windows/desktop/api/WebServices/nf-webservices-wsreseterror) anrufen, nachdem er die Informationen zu dem Fehler überprüft hat. Wenn dies nicht der Fall ist, kann dies zu einer Speicher Akkumulation führen.
-   Ein Benutzer des Error-Objekts sollte sehr vorsichtig sein, wenn der WS- \_ Wert für die vollständige Fehler Veröffentlichung der \_ WS- \_ [**\_ \_ fehleroffenlegungs**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_disclosure) -Enumeration verwendet wird, da der generierte Fehler möglicherweise private Informationen enthalten kann, die im Rahmen des Fehler Aufzeichnungsprozesses gesammelt wurden.

 

 




