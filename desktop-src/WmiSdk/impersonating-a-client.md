---
description: Wenn eine Benutzeranwendung Daten von Objekten im System über einen WMI-Anbieter anfordert, bedeutet Identitätswechsel, dass der Anbieter Anmeldeinformationen angibt, die die Sicherheitsstufe des Clients und nicht die Anbieter darstellen.
ms.assetid: 6d54f234-45aa-445b-ad50-7d5a9946c134
ms.tgt_platform: multiple
title: Annehmen der Identität eines Clients
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04b6d1fe931a9e0620643d8b3f8a77c63d031a41f1dac9d17301e11c03d21bfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757940"
---
# <a name="impersonating-a-client"></a>Annehmen der Identität eines Clients

Wenn eine Benutzeranwendung Daten von Objekten im System über einen WMI-Anbieter anfordert, bedeutet Identitätswechsel, dass der Anbieter Anmeldeinformationen angibt, die die Sicherheitsstufe des Clients und nicht die des Anbieters darstellen. Der Identitätswechsel verhindert, dass ein Client nicht autorisierten Zugriff auf Informationen auf dem System erhält.

Die folgenden Abschnitte werden in diesem Thema erläutert:

-   [Registrieren eines Anbieters für den Identitätswechsel](#registering-a-provider-for-impersonation)
-   [Festlegen von Identitätswechselebenen innerhalb eines Anbieters](#setting-impersonation-levels-within-a-provider)
-   [Verwalten von Sicherheitsebenen in einem Anbieter](#maintaining-security-levels-in-a-provider)
-   [Behandeln von Nachrichten vom Anbieter "Zugriff verweigert"](#handling-access-denied-messages-in-a-provider)
-   [Melden von Teilinstanzen](#reporting-partial-instances)
-   [Melden von partiellen Enumerationen](#reporting-partial-enumerations)
-   [Debuggen des Zugriffs verweigerten Codes](#debugging-your-access-denied-code)
-   [Zugehörige Themen](#related-topics)

WMI wird in der Regel mithilfe des Sicherheitskontexts LocalServer als Verwaltungsdienst auf hoher Sicherheitsebene ausgeführt. Die Verwendung eines Verwaltungsdiensts bietet WMI die Möglichkeit, auf privilegierte Informationen zuzugreifen. Beim Aufrufen eines Anbieters für Informationen übergibt WMI seine Sicherheits-ID (SID) an den Anbieter, sodass der Anbieter auf derselben hohen Sicherheitsstufe auf Informationen zugreifen kann.

Während des Startvorgangs der WMI-Anwendung gibt das Windows Betriebssystem der WMI-Anwendung den Sicherheitskontext des Benutzers, der den Prozess gestartet hat. Der Sicherheitskontext des Benutzers ist in der Regel eine niedrigere Sicherheitsstufe als LocalServer, sodass der Benutzer möglicherweise nicht über die Berechtigung zum Zugriff auf alle für WMI verfügbaren Informationen verfügt. Wenn die Benutzeranwendung dynamische Informationen anfragt, übergibt WMI die SID des Benutzers an den entsprechenden Anbieter. Wenn der Anbieter entsprechend geschrieben ist, versucht er, mit der Benutzer-SID und nicht mit der Anbieter-SID auf Informationen zuzugreifen.

Damit der Anbieter erfolgreich die Identität der Clientanwendung annehmen kann, müssen die Clientanwendung und der Anbieter die folgenden Kriterien erfüllen:

-   Die Clientanwendung muss WMI mit der **COM-Verbindungssicherheitsstufe RPC \_ C \_ IMP \_ LEVEL \_ IMPERSONATE** oder **RPC C \_ \_ IMP LEVEL \_ \_ DELEGATE** aufrufen. Weitere Informationen finden Sie unter [Verwalten der WMI-Sicherheit.](maintaining-wmi-security.md)
-   Der Anbieter muss sich bei WMI als Identitätswechselanbieter registrieren. Weitere Informationen finden Sie unter [Registrieren eines Anbieters für Identitätswechsel.](#registering-a-provider-for-impersonation)
-   Der Anbieter muss zur Sicherheitsstufe der Clientanwendung wechseln, bevor er auf privilegierte Informationen zugreifen kann. Weitere Informationen finden Sie unter [Festlegen von Identitätswechselebenen innerhalb eines Anbieters.](#setting-impersonation-levels-within-a-provider)
-   Der Anbieter muss Fehlerbedingungen ordnungsgemäß behandeln, wenn der Zugriff auf diese Informationen verweigert wird. Weitere Informationen finden Sie unter [Handling Access Denied Messages in a Provider](#handling-access-denied-messages-in-a-provider).

## <a name="registering-a-provider-for-impersonation"></a>Registrieren eines Anbieters für den Identitätswechsel

WMI übergibt die SID einer Clientanwendung nur an Anbieter, die sich als Identitätswechselanbieter registriert haben. Um einem Anbieter das Ausführen eines Identitätswechsels zu ermöglichen, müssen Sie den Anbieterregistrierungsprozess ändern.

Im folgenden Verfahren wird beschrieben, wie Sie einen Anbieter für den Identitätswechsel registrieren. Bei diesem Verfahren wird davon ausgegangen, dass Sie den Registrierungsprozess bereits verstanden haben. Weitere Informationen zum Registrierungsvorgang finden Sie unter [Registrieren eines Anbieters.](registering-a-provider.md)

**So registrieren Sie einen Anbieter für den Identitätswechsel**

1.  Legen Sie die [**ImpersonationLevel-Eigenschaft**](swbemsecurity-impersonationlevel.md) der [**\_ \_ Win32Provider-Klasse,**](--win32provider.md) die Ihren Anbieter darstellt, auf 1 fest.

    Die [**ImpersonationLevel-Eigenschaft**](swbemsecurity-impersonationlevel.md) dokumentiert, ob der Anbieter Identitätswechsel unterstützt. Wenn **ImpersonationLevel** auf 0 festgelegt wird, gibt dies an, dass der Anbieter nicht die Identität des Clients annimmt und alle angeforderten Vorgänge im gleichen Benutzerkontext wie WMI ausführt. Das Festlegen von **ImpersonationLevel** auf 1 gibt an, dass der Anbieter Identitätswechselaufrufe verwendet, um Vorgänge zu überprüfen, die im Auftrag des Clients ausgeführt werden.

2.  Legen Sie die **PerUserInitialization-Eigenschaft** der gleichen [**\_ \_ Win32Provider-Klasse**](--win32provider.md) auf **TRUE** fest.

> [!Note]  
> Wenn Sie einen Anbieter registrieren, bei dem die [**\_ \_ Win32Provider-Eigenschaft**](--win32provider.md) **InitializeAsAdminFirst** auf **TRUE** festgelegt ist, verwendet der Anbieter das Threadsicherheitstoken auf Verwaltungsebene nur während der Initialisierungsphase. Während ein Aufruf von [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) nicht fehlschlägt, verwendet der Anbieter den Sicherheitskontext von WMI und nicht des Clients.

 

Das folgende Codebeispiel zeigt, wie ein Anbieter für den Identitätswechsel registriert wird.

``` syntax
instance of __Win32Provider
{
    CLSID = "{FD4F53E0-65DC-11d1-AB64-00C04FD9159E}";
    ImpersonationLevel = 1;
    Name = "MS_NT_EVENTLOG_PROVIDER";
    PerUserInitialization = TRUE;
};
```

## <a name="setting-impersonation-levels-within-a-provider"></a>Festlegen von Identitätswechselebenen innerhalb eines Anbieters

Wenn Sie einen Anbieter mit der [**\_ \_ Win32Provider-Klasseneigenschaft**](--win32provider.md) [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) registrieren, die auf 1 festgelegt ist, ruft WMI Ihren Anbieter auf, um die Identität verschiedener Clients zu übernehmen. Um diese Aufrufe zu verarbeiten, verwenden Sie die COM-Funktionen [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) und [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) in Ihrer Implementierung der [**IWbemServices-Schnittstelle.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)

Mit [**der CoImpersonateClient-Funktion**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) kann ein Server die Identität des Clients annehmen, der den Aufruf ausgeführt hat. Indem Sie **CoImpersonateClient** in Ihrer Implementierung von [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)aufrufen, ermöglichen Sie ihrem Anbieter, das Threadtoken des Anbieters so festzulegen, dass es mit dem Threadtoken des Clients übereinstimmt, und so die Identität des Clients annehmen. Wenn Sie **CoImpersonateClient** nicht aufrufen, führt Ihr Anbieter Code auf Administratorebene aus, wodurch ein potenzielles Sicherheitsrisiko entsteht. Wenn Ihr Anbieter vorübergehend als Administrator fungieren oder die Zugriffsüberprüfung manuell durchführen muss, rufen Sie [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself)auf.

Im Gegensatz zu [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient)ist [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) eine COM-Funktion, die Threadidentitätswechselebenen verarbeitet. In diesem Fall ändert **CoRevertToSelf** die Identitätswechselebene zurück in die ursprüngliche Identitätswechseleinstellung. Im Allgemeinen ist der Anbieter anfänglich ein Administrator und wechselt zwischen **CoImpersonateClient** und **CoRevertToSelf,** je nachdem, ob er einen Aufruf vornimmt, der den Aufrufer oder seine eigenen Aufrufe darstellt. Es liegt in der Verantwortung des Anbieters, diese Aufrufe ordnungsgemäß zu platzieren, damit keine Sicherheitslücke für den Endbenutzer entsteht. Der Anbieter sollte z. B. nur native Windows Funktionen innerhalb der Codesequenz aufrufen, für die ein Identitätswechsel erfolgt ist.

> [!Note]  
> [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) und [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) dienen zum Festlegen der Sicherheit für einen Anbieter. Wenn Sie feststellen, dass ihr Identitätswechsel fehlgeschlagen ist, sollten Sie über [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus)einen entsprechenden Vervollständigungscode an WMI zurückgeben. Weitere Informationen finden Sie unter [Handling Access Denied Messages in a Provider](#handling-access-denied-messages-in-a-provider).

 

## <a name="maintaining-security-levels-in-a-provider"></a>Verwalten von Sicherheitsebenen in einem Anbieter

Anbieter können [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) nicht einmal in einer Implementierung von [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) aufrufen und gehen davon aus, dass die Identitätswechselanmeldeinformationen für die Dauer des Anbieters vorhanden bleiben. Rufen Sie stattdessen **CoImpersonateClient** im Verlauf einer Implementierung mehrmals auf, um WMI daran zu hindern, die Anmeldeinformationen zu ändern.

Das Hauptanliegen beim Festlegen des Identitätswechsels für einen Anbieter ist die Wiederinvarianz. In diesem Kontext erfolgt die Eintrittsinvarianz, wenn ein Anbieter WMI zur Information aufruft und wartet, bis WMI den Anbieter zurückruft. Im Wesentlichen verlässt der Ausführungsthread den Anbietercode, nur um den Code zu einem späteren Zeitpunkt erneut ein zu verwenden. Der erneute Versuch ist Teil des Com-Entwurfs und im Allgemeinen kein Problem. Wenn der Ausführungsthread jedoch in WMI eintritt, übernimmt der Thread die Identitätswechselebenen von WMI. Wenn der Thread zum Anbieter zurückkehrt, müssen Sie die Identitätswechselebenen mit einem anderen Aufruf von [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient)zurücksetzen.

Um sich vor Sicherheitslücken in Ihrem Anbieter zu schützen, sollten Sie erneute Aufrufe an WMI nur beim Identitätswechsel des Clients vornehmen. Das heißt, dass WMI-Aufrufe erfolgen sollten, nachdem Sie [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) aufgerufen haben und bevor Sie [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself)aufrufen. Da **CoRevertToSelf** dazu führt, dass der Identitätswechsel auf die ausgeführte WMI-Benutzerebene festgelegt wird( im Allgemeinen LocalSystem), können erneute Aufrufe von WMI nach dem Aufruf von **CoRevertToSelf** dem Benutzer und allen aufgerufenen Anbietern deutlich mehr Funktionen bieten, als sie haben sollten.

> [!Note]  
> Wenn Sie eine Systemfunktion oder eine andere Schnittstellenmethode aufrufen, ist nicht garantiert, dass der Aufrufkontext beibehalten wird.

 

## <a name="handling-access-denied-messages-in-a-provider"></a>Behandeln von Nachrichten vom Anbieter "Zugriff verweigert"

Die meisten Access Denied-Fehlermeldungen werden angezeigt, wenn ein Client eine Klasse oder Informationen anfordert, auf die er keinen Zugriff hat. Wenn der Anbieter eine Fehlermeldung Vom Zugriff verweigert an WMI zurückgibt und WMI diese an den Client übergibt, kann der Client ableiten, dass die Informationen vorhanden sind. In einigen Situationen kann dies eine Sicherheitsverletzung sein. Daher sollte Ihr Anbieter die Nachricht nicht an den Client senden. Stattdessen sollte der Satz von Klassen, die der Anbieter bereitgestellt hätte, nicht verfügbar gemacht werden. Auf ähnliche Weise sollte ein dynamischer Instanzanbieter die zugrunde liegende Datenquelle aufrufen, um zu bestimmen, wie mit Meldungen vom Datentyp "Zugriff verweigert" umgegangen werden soll. Es liegt in der Verantwortung des Anbieters, diese Philosophie in die WMI-Umgebung zu replizieren. Weitere Informationen finden Sie unter [Reporting Partial Instances](#reporting-partial-instances) und [Reporting Partial Enumerations](#reporting-partial-enumerations).

Wenn Sie bestimmen, wie Ihr Anbieter Nachrichten vom Anbieter "Zugriff verweigert" behandeln soll, müssen Sie Ihren Code schreiben und debuggen. Beim Debuggen ist es oft praktisch, zwischen einer Verweigerung aufgrund eines niedrigen Identitätswechsels und einer Verweigerung aufgrund eines Fehlers im Code zu unterscheiden. Sie können einen einfachen Test in Ihrem Code verwenden, um den Unterschied zu ermitteln. Weitere Informationen finden Sie unter [Debuggen ihres Zugriffs verweigerten Codes.](#debugging-your-access-denied-code)

## <a name="reporting-partial-instances"></a>Melden von Teilinstanzen

Ein häufiges Vorkommen einer Access Denied-Nachricht ist, wenn WMI nicht alle Informationen zum Ausfüllen einer Instanz bereitstellen kann. Beispielsweise kann ein Client über die Berechtigung zum Anzeigen eines Festplattenlaufwerkobjekts verfügen, aber möglicherweise nicht über die Berechtigung, festzustellen, wie viel Speicherplatz auf dem Festplattenlaufwerk selbst verfügbar ist. Ihr Anbieter muss bestimmen, wie eine Situation behandelt werden soll, in der der Anbieter eine Instanz aufgrund einer Zugriffsverletzung nicht vollständig mit Eigenschaften füllen kann.

WMI erfordert keine einzelne Antwort auf Clients, die teilweise Zugriff auf eine Instanz haben. Stattdessen ermöglicht WMI Version 1.x dem Anbieter eine der folgenden Optionen:

-   Schlägt den gesamten Vorgang mit **WBEM \_ E \_ ACCESS \_ DENIED fehl** und gibt keine Instanzen zurück.

    Geben Sie ein Fehlerobjekt zusammen mit **WBEM \_ E \_ ACCESS \_ DENIED** zurück, um den Grund für die Verweigerung zu beschreiben.

-   Geben Sie alle verfügbaren Eigenschaften zurück, und füllen Sie nicht verfügbare Eigenschaften mit **NULL** aus.

> [!Note]  
> Stellen Sie sicher, dass die Rückgabe von **WBEM \_ E \_ ACCESS \_ DENIED** keine Sicherheitslücke in Ihrem Unternehmen schafft.

 

## <a name="reporting-partial-enumerations"></a>Melden von partiellen Enumerationen

Ein weiteres häufiges Vorkommen einer Zugriffsverletzung ist, wenn WMI nicht alle Enumerationen zurückgeben kann. Beispielsweise kann ein Client Zugriff haben, um alle Objekte des lokalen Netzwerkcomputers anzuzeigen, aber möglicherweise keinen Zugriff zum Anzeigen von Computerobjekten außerhalb seiner Domäne. Ihr Anbieter muss bestimmen, wie eine Situation behandelt werden soll, in der eine Enumeration aufgrund einer Zugriffsverletzung nicht abgeschlossen werden kann.

Wie bei einem Instanzanbieter erfordert WMI keine einzelne Antwort auf eine partielle Enumeration. Stattdessen lässt die WMI-Version 1.x einem Anbieter eine der folgenden Optionen zu:

-   Gibt **WBEM \_ S NO ERROR \_ \_ für** alle Instanzen zurück, auf die der Anbieter zugreifen kann.

    Wenn Sie diese Option verwenden, ist dem Benutzer nicht bewusst, dass einige Instanzen nicht verfügbar waren. Eine Reihe von Anbietern, z. B. anbieter, die strukturierte Abfragesprache (SQL) mit Sicherheit auf Zeilenebene verwenden, geben erfolgreiche Teilergebnisse zurück, indem sie die Sicherheitsebene des Aufrufers verwenden, um das Resultseset zu definieren.

-   Führen Sie den gesamten Vorgang mit **WBEM \_ E \_ ACCESS \_ DENIED** aus, und geben Sie keine Instanzen zurück.

    Der Anbieter kann optional ein Fehlerobjekt enthalten, das die Situation für den Client beschreibt. Beachten Sie, dass einige Anbieter möglicherweise seriell auf Datenquellen zugreifen und bis zum Teil der Enumeration nicht auf Denials stoßen.

-   Gibt alle Instanzen zurück, auf die zugegriffen werden kann, gibt aber auch den Nichtfehlerstatuscode **WBEM \_ S \_ ACCESS \_ DENIED zurück.**

    Der Anbieter sollte die Ablehnung während der Enumeration notieren und möglicherweise weiterhin Instanzen bereitstellen, um den Statuscode "Nonerror" zu beenden. Der Anbieter kann auch die Enumeration beim ersten Denial beenden. Die Begründung für diese Option ist, dass verschiedene Anbieter unterschiedliche Abrufparadigmen haben. Ein Anbieter hat möglicherweise bereits Instanzen übermittelt, bevor eine Zugriffsverletzung festgestellt wird. Einige Anbieter können weitere Instanzen bereitstellen, während andere möglicherweise beendet werden möchten.

Aufgrund der Com-Struktur können Sie während eines Fehlers keine Informationen mit Ausnahme eines Fehlerobjekts zurück marshallen. Daher können Sie nicht sowohl Informationen als auch einen Fehlercode zurückgeben. Wenn Sie Informationen zurückgeben möchten, müssen Sie stattdessen einen Statuscode ohne Fehler verwenden.

## <a name="debugging-your-access-denied-code"></a>Debuggen des Zugriffs verweigerten Codes

Einige Anwendungen verwenden möglicherweise Identitätswechselebenen, die niedriger als **RPC C IMP LEVEL \_ \_ \_ \_ IMPERSONATE sind.** In diesem Fall können die meisten Identitätswechselaufrufe, die vom Anbieter für die Clientanwendung ausgeführt werden, nicht ausgeführt werden. Um einen Anbieter erfolgreich zu entwerfen und zu implementieren, müssen Sie diese Idee berücksichtigen.

Standardmäßig ist rpc C IMP LEVEL IDENTIFY die einzige andere Ebene des Identitätswechsels, die auf einen Anbieter **\_ zugreifen \_ \_ \_ kann.** In Fällen, in denen eine Clientanwendung **RPC C IMP LEVEL IDENTIFY \_ \_ \_ \_ verwendet,** gibt [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) keinen Fehlercode zurück. Stattdessen wird die Identität des Clients nur zu Identifikationszwecken vom Anbieter angenommen. Daher geben die Windows methoden, die vom Anbieter aufgerufen werden, eine Meldung mit verweigerten Zugriffsberechtigungen zurück. Dies ist in der Praxis unbedenklich, da Benutzern nicht gestattet wird, ungeeignete Vorgehensweisen zu unternehmen. Es kann jedoch hilfreich sein, während der Anbieterentwicklung zu wissen, ob die Identität des Clients tatsächlich angenommen wurde.

Der Code erfordert die folgenden Verweise und \# include-Anweisungen, um ordnungsgemäß zu kompilieren.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
```



Im folgenden Codebeispiel wird veranschaulicht, wie Ermittelt wird, ob ein Anbieter erfolgreich die Identität einer Clientanwendung angenommen hat.


```C++
DWORD dwImp = 0;
HANDLE hThreadTok;
DWORD dwBytesReturned;
BOOL bRes;

// You must call this before trying to open a thread token!
CoImpersonateClient();

bRes = OpenThreadToken(
    GetCurrentThread(),
    TOKEN_QUERY,
    TRUE,
    &hThreadTok
);

if (bRes == FALSE)
{
    printf("Unable to read thread token (%d)\n", GetLastError());
    return 0;
}

bRes = GetTokenInformation(
    hThreadTok,
    TokenImpersonationLevel, 
    &dwImp,
    sizeof(DWORD),
    &dwBytesReturned
);

if (!bRes)
{
    printf("Unable to read impersonation level\n");
    CloseHandle(hThreadTok);
    return 0;
}

switch (dwImp)
{
case SecurityAnonymous:
    printf("SecurityAnonymous\n");
    break;

case SecurityIdentification:
    printf("SecurityIdentification\n");
    break;

case SecurityImpersonation:
    printf("SecurityImpersonation\n");
    break;

case SecurityDelegation:
    printf("SecurityDelegation\n");
    break;

default:
    printf("Error. Unable to determine impersonation level\n");
    break;
}

CloseHandle(hThreadTok);
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwickeln eines WMI-Anbieters](developing-a-wmi-provider.md)
</dt> <dt>

[Festlegen von Namepace-Sicherheitsdeskriptoren](setting-namespace-security-descriptors.md)
</dt> <dt>

[Schützen Ihres Anbieters](securing-your-provider.md)
</dt> </dl>

 

 
