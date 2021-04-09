---
description: Wenn eine Benutzeranwendung Daten von Objekten auf dem System über einen WMI-Anbieter anfordert, bedeutet der Identitätswechsel, dass der Anbieter Anmelde Informationen anzeigt, die die Sicherheitsstufe des Clients anstelle der Anbieter darstellen.
ms.assetid: 6d54f234-45aa-445b-ad50-7d5a9946c134
ms.tgt_platform: multiple
title: Annehmen der Identität eines Clients
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 162857d90c8bddb70d90eb2e10efbc08537299d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866888"
---
# <a name="impersonating-a-client"></a>Annehmen der Identität eines Clients

Wenn eine Benutzeranwendung Daten von Objekten auf dem System über einen WMI-Anbieter anfordert, bedeutet der Identitätswechsel, dass der Anbieter Anmelde Informationen anzeigt, die die Sicherheitsstufe des Clients anstelle des Anbieters darstellen. Durch den Identitätswechsel wird verhindert, dass ein Client nicht autorisierten Zugriff auf Informationen auf dem System erhält.

In diesem Thema werden die folgenden Abschnitte erläutert:

-   [Registrieren eines Anbieters für den Identitätswechsel](#registering-a-provider-for-impersonation)
-   [Festlegen von Identitätswechsel Ebenen innerhalb eines Anbieters](#setting-impersonation-levels-within-a-provider)
-   [Beibehalten von Sicherheitsstufen in einem Anbieter](#maintaining-security-levels-in-a-provider)
-   [Behandeln von Zugriffen auf Abgelehnte Nachrichten in einem Anbieter](#handling-access-denied-messages-in-a-provider)
-   [Teil Instanzen der Berichterstellung](#reporting-partial-instances)
-   [Partielle Enumerationen für Berichte](#reporting-partial-enumerations)
-   [Debuggen des Zugriffs verweigerten Codes](#debugging-your-access-denied-code)
-   [Zugehörige Themen](#related-topics)

WMI wird in der Regel unter Verwendung des Sicherheits Kontexts LocalServer als administrativer Dienst mit hoher Sicherheitsstufe ausgeführt. Durch die Verwendung eines administrativen Dienstanbieter erhält WMI die Möglichkeit, auf privilegierte Informationen zuzugreifen. Wenn Sie einen Anbieter für Informationen aufrufen, übergibt WMI seine Sicherheits-ID (Security Identifier, SID) an den Anbieter, sodass der Anbieter auf Informationen mit der gleichen hohen Sicherheitsstufe zugreifen kann.

Während des Startvorgangs der WMI-Anwendung gibt das Windows-Betriebssystem der WMI-Anwendung den Sicherheitskontext des Benutzers, der den Vorgang begonnen hat. Der Sicherheitskontext des Benutzers ist in der Regel eine niedrigere Sicherheitsstufe als LocalServer, sodass der Benutzer möglicherweise nicht über die Berechtigung verfügt, auf alle Informationen zuzugreifen, die für WMI verfügbar sind. Wenn die Benutzeranwendung dynamische Informationen anfordert, übergibt WMI die SID des Benutzers an den entsprechenden Anbieter. Bei entsprechender Schreibweise versucht der Anbieter, auf Informationen mit der Benutzer-SID und nicht mit der Anbieter-SID zuzugreifen.

Damit der Anbieter die Identität der Client Anwendung erfolgreich annehmen kann, müssen die Client Anwendung und der Anbieter die folgenden Kriterien erfüllen:

-   Die Client Anwendung muss WMI mit einer com-Verbindungs Sicherheitsstufe von RPC-c-IMP-Ebene Identitätswechsel oder **RPC- \_ c- \_ IMP- \_ Ebene \_**- **\_ \_ \_ \_ Delegaten** aufruft. Weitere Informationen finden Sie unter Verwalten der [WMI-Sicherheit](maintaining-wmi-security.md).
-   Der Anbieter muss sich bei WMI als Identitätswechsel Anbieter registrieren. Weitere Informationen finden Sie unter [Registrieren eines Anbieters für](#registering-a-provider-for-impersonation)den Identitätswechsel.
-   Der Anbieter muss vor dem Zugriff auf privilegierte Informationen zur Sicherheitsebene der Client Anwendung wechseln. Weitere Informationen finden Sie unter [Festlegen von Identitätswechsel Ebenen innerhalb eines Anbieters](#setting-impersonation-levels-within-a-provider).
-   Der Anbieter muss Fehlerbedingungen ordnungsgemäß behandeln, wenn der Zugriff auf diese Informationen verweigert wird. Weitere Informationen finden Sie unter [Behandeln von Zugriffen auf Abgelehnte Nachrichten in einem Anbieter](#handling-access-denied-messages-in-a-provider).

## <a name="registering-a-provider-for-impersonation"></a>Registrieren eines Anbieters für den Identitätswechsel

WMI übergibt die SID einer Client Anwendung nur an Anbieter, die als Identitäts Anbieter registriert sind. Zum Aktivieren eines Anbieters für die Durchführung des Identitäts Wechsels ist es erforderlich, dass Sie den Anbieter Registrierungsprozess ändern.

Im folgenden Verfahren wird beschrieben, wie ein Anbieter für den Identitätswechsel registriert wird. In diesem Verfahren wird davon ausgegangen, dass Sie den Registrierungsprozess bereits verstanden haben. Weitere Informationen zum Registrierungsprozess finden Sie unter [Registrieren eines Anbieters](registering-a-provider.md).

**So registrieren Sie einen Anbieter für den Identitätswechsel**

1.  Legen Sie die Eigenschaft "Identitätswechsel [**Ebene**](swbemsecurity-impersonationlevel.md) " der [**\_ \_ Win32Provider**](--win32provider.md) -Klasse, die den Anbieter darstellt, auf 1 fest.

    Die Eigenschaft "Identitätswechsel [**Ebene**](swbemsecurity-impersonationlevel.md) " dokumentiert, ob der Anbieter Identitätswechsel unterstützt. Das Festlegen von "Identitätswechsel **Ebene** " auf "0" gibt an, dass der Anbieter die Identität des Clients nicht annimmt und alle angeforderten Vorgänge im gleichen Benutzer Kontext wie WMI ausführt. Das Festlegen von "Identitätswechsel **Ebene** " auf 1 gibt an, dass der Anbieter Identitätswechsel Aufrufe verwendet, um im Auftrag des Clients ausgeführte Vorgänge zu überprüfen.

2.  Legen Sie die Eigenschaft " **peruserinitialization** " der [**\_ \_ Win32Provider**](--win32provider.md) -Klasse auf " **true**" fest.

> [!Note]  
> Wenn Sie einen Anbieter registrieren, bei dem die [**\_ \_ Win32Provider**](--win32provider.md) -Eigenschaft **initializeasadminfirst** auf **true** festgelegt ist, verwendet der Anbieter das Thread Sicherheits Token auf Verwaltungsebene nur während der Initialisierungsphase. Während ein Anrufe an " [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) " nicht fehlschlägt, verwendet der Anbieter den Sicherheitskontext von WMI und nicht den Client.

 

Im folgenden Codebeispiel wird gezeigt, wie ein Anbieter für den Identitätswechsel registriert wird.

``` syntax
instance of __Win32Provider
{
    CLSID = "{FD4F53E0-65DC-11d1-AB64-00C04FD9159E}";
    ImpersonationLevel = 1;
    Name = "MS_NT_EVENTLOG_PROVIDER";
    PerUserInitialization = TRUE;
};
```

## <a name="setting-impersonation-levels-within-a-provider"></a>Festlegen von Identitätswechsel Ebenen innerhalb eines Anbieters

Wenn Sie einen Anbieter registrieren, bei dem die [**\_ \_ Win32Provider**](--win32provider.md) -Klassen Eigenschaft Identitätswechsel [**Ebene**](swbemsecurity-impersonationlevel.md) auf 1 festgelegt ist, ruft WMI Ihren Anbieter auf, um die Identität verschiedener Clients anzunehmen. Um diese Aufrufe zu verarbeiten, verwenden Sie die Funktionen " [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) " und " [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) com" in ihrer Implementierung der [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Schnittstelle.

Die Funktion " [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) " ermöglicht einem Server, die Identität des Clients anzunehmen, der den-Befehl durchgeführt hat. Durch das Platzieren eines Aufrufes von **CoImpersonateClient** in Ihre Implementierung von [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)ermöglichen Sie dem Anbieter, das Thread Token des Anbieters so festzulegen, dass es dem Thread Token des Clients entspricht, und die Identität des Clients anzunehmen. Wenn Sie " **CoImpersonateClient**" nicht aufzurufen, führt Ihr Anbieter Code auf Administratorebene aus, um ein potenzielles Sicherheitsrisiko zu schaffen. Wenn Ihr Anbieter temporär als Administrator fungieren oder die Zugriffs Überprüfung manuell ausführen muss, wenden Sie sich an [**corevertstoself**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself).

Im Gegensatz zu " [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient)" ist [**corevertteself**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) eine com-Funktion, die Thread Identitätswechsel Ebenen behandelt. In diesem Fall ändert **coreverttself** die Identitätswechsel Ebene zurück in die ursprüngliche Identitätswechsel Einstellung. Im Allgemeinen ist der Anbieter anfänglich ein Administrator und wechselt zwischen " **CoImpersonateClient** " und " **corevertstoself** ", je nachdem, ob er einen Aufruf durchführen soll, der den Aufrufer oder seine eigenen Aufrufe darstellt. Es liegt in der Verantwortung des Anbieters, diese Aufrufe ordnungsgemäß zu platzieren, damit keine Sicherheitslücke für den Endbenutzer verfügbar gemacht wird. Der Anbieter sollte z. b. nur native Windows-Funktionen innerhalb der Code Sequenz mit Identitätswechsel aufzurufen.

> [!Note]  
> Der Zweck von " [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) " und " [**corevertstoself**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) " ist das Festlegen der Sicherheit für einen Anbieter. Wenn Sie feststellen, dass Ihr Identitätswechsel fehlgeschlagen ist, sollten Sie über [**iwbewbjectsink:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus)einen passenden Vervollständigungs Code an WMI zurückgeben. Weitere Informationen finden Sie unter [Behandeln von Zugriffen auf Abgelehnte Nachrichten in einem Anbieter](#handling-access-denied-messages-in-a-provider).

 

## <a name="maintaining-security-levels-in-a-provider"></a>Beibehalten von Sicherheitsstufen in einem Anbieter

Anbieter können " [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) " nicht einmal in einer Implementierung von " [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) " abrufen und davon ausgehen, dass die Identitätswechsel-Anmelde Informationen für die Dauer des Anbieters vorhanden sind. Verwenden Sie stattdessen " **CoImpersonateClient** " mehrmals im Verlauf einer Implementierung, damit WMI die Anmelde Informationen nicht ändert.

Der Hauptgrund für das Festlegen des Identitäts Wechsels für einen Anbieter ist das erneute eintreten. In diesem Zusammenhang ist das erneute eintreten, wenn ein Anbieter WMI für Informationen aufruft und wartet, bis WMI einen Rückruf an den Anbieter sendet. Im wesentlichen verlässt der Ausführungs Thread den Anbieter Code, nur um den Code zu einem späteren Zeitpunkt erneut einzugeben. Reentry ist ein Bestandteil des Entwurfs von com und ist in der Regel kein Problem. Wenn der Ausführungs Thread jedoch in WMI wechselt, übernimmt der Thread die Identitätswechsel Ebenen von WMI. Wenn der Thread an den Anbieter zurückgegeben wird, müssen Sie die Identitätswechsel Ebenen mit einem weiteren aufrufungsebene von [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient)zurücksetzen.

Wenn Sie sich vor Sicherheitslücken in Ihrem Anbieter schützen möchten, sollten Sie nur dann wieder eintretende Aufrufe von WMI ausführen, während Sie die Identität des Clients annehmen. Das heißt, dass Aufrufe von WMI erfolgen sollten, nachdem Sie " [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) " und vor dem Aufruf von " [**corevertdeself**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself)" aufgerufen haben. Da **CoRevertToSelf** bewirkt, dass der Identitätswechsel auf die Benutzerebene festgelegt wird, die von WMI ausgeführt wird, werden im allgemeinen "LocalSystem", Wiedereintritts fähige Aufrufe an WMI nach dem Aufruf von " **CoRevertToSelf** " dem Benutzer und allen Anbietern mit dem Namen sehr viel mehr Funktionen zugewiesen, als Sie hätten.

> [!Note]  
> Wenn Sie eine Systemfunktion oder eine andere Schnittstellen Methode aufzurufen, wird der Kontext des aufrufskontexts nicht garantiert beibehalten.

 

## <a name="handling-access-denied-messages-in-a-provider"></a>Behandeln von Zugriffen auf Abgelehnte Nachrichten in einem Anbieter

Die meisten Zugriffs Verweigerungs Fehlermeldungen werden angezeigt, wenn ein Client eine Klasse oder Informationen anfordert, auf die Sie keinen Zugriff haben. Wenn der Anbieter die Fehlermeldung "Zugriff verweigert" an WMI zurückgibt und diese an den Client weitergegeben wird, kann der Client ableiten, dass die Informationen vorhanden sind. In einigen Fällen kann dies ein Sicherheits Verstoß sein. Daher sollte der Anbieter die Nachricht nicht an den Client weitergeben. Stattdessen sollte der Satz von Klassen, den der Anbieter bereitgestellt hätte, nicht verfügbar gemacht werden. Entsprechend sollte ein dynamischer Instanzanbieter die zugrunde liegende Datenquelle aufrufen, um zu bestimmen, wie die Nachrichten vom Typ "Zugriff verweigert" behandelt werden. Es liegt in der Verantwortung des Anbieters, diese Philosophie in der WMI-Umgebung zu replizieren. Weitere Informationen finden Sie unter [Reporting partieller Instanzen](#reporting-partial-instances) und [melden partieller Enumerationen](#reporting-partial-enumerations).

Wenn Sie bestimmen, wie der Anbieter zugriffverweigerungs-Nachrichten behandeln soll, müssen Sie den Code schreiben und Debuggen. Beim Debuggen ist es häufig sinnvoll, eine Verweigerung aufgrund von geringem Identitätswechsel und eine Verweigerung aufgrund eines Fehlers im Code zu unterscheiden. Sie können einen einfachen Test in Ihrem Code verwenden, um den Unterschied zu bestimmen. Weitere Informationen finden Sie unter [Debuggen des Codes für den Zugriff verweigert](#debugging-your-access-denied-code).

## <a name="reporting-partial-instances"></a>Teil Instanzen der Berichterstellung

Ein häufiges Vorkommen einer Nachricht vom Typ "Zugriff verweigert" besteht darin, dass WMI nicht alle Informationen zum Ausfüllen einer Instanz bereitstellen kann. Ein Client kann z. b. über die Berechtigung zum Anzeigen eines Festplatten Laufwerks verfügen, aber möglicherweise nicht über die Berechtigung, zu sehen, wie viel Speicherplatz auf dem Festplattenlaufwerk selbst verfügbar ist. Der Anbieter muss festlegen, wie jede Situation behandelt werden soll, wenn der Anbieter eine Instanz aufgrund einer Zugriffsverletzung nicht vollständig mit Eigenschaften auffüllen kann.

WMI erfordert keine einzige Antwort an Clients, die partiellen Zugriff auf eine Instanz haben. Stattdessen ermöglicht WMI Version 1. x dem Anbieter eine der folgenden Optionen:

-   Fehler beim gesamten Vorgang mit **WBEM \_ E \_ Access \_ verweigert** und gibt keine Instanzen zurück.

    Geben Sie zusammen mit **WBEM \_ E \_ Access \_ denied** ein Fehler Objekt zurück, um den Grund für die Verweigerung zu beschreiben.

-   Geben Sie alle verfügbaren Eigenschaften zurück, und füllen Sie nicht verfügbare Eigenschaften mit **null**.

> [!Note]  
> Stellen Sie sicher, dass das Zurückgeben von **WBEM \_ E \_ Access \_ denied** keine Sicherheitslücke in Ihrem Unternehmen erzeugt.

 

## <a name="reporting-partial-enumerations"></a>Partielle Enumerationen für Berichte

Ein weiteres häufiges Vorkommen einer Zugriffsverletzung ist, wenn WMI keine Enumeration zurückgeben kann. Beispielsweise kann ein Client auf alle lokalen Netzwerk Computer Objekte zugreifen, aber möglicherweise nicht auf die Anzeige von Computer Objekten außerhalb seiner Domäne zugreifen. Der Anbieter muss festlegen, wie jede Situation behandelt werden soll, in der eine Enumeration aufgrund einer Zugriffsverletzung nicht abgeschlossen werden kann.

Wie bei einem Instanzanbieter erfordert WMI keine einzige Antwort auf eine partielle Enumeration. Stattdessen ermöglicht WMI Version 1. x einem Anbieter eine der folgenden Optionen:

-   Gibt **WBEM \_ S \_ keinen \_ Fehler** für alle Instanzen zurück, auf die der Anbieter zugreifen kann.

    Wenn Sie diese Option verwenden, weiß der Benutzer nicht, dass einige Instanzen nicht verfügbar waren. Eine Reihe von Anbietern, z. b. solche, die Structured Query Language (SQL) mit Sicherheit auf Zeilenebene verwenden, geben erfolgreiche partielle Ergebnisse zurück, indem die Sicherheitsstufe des Aufrufers zum Definieren des Resultsets verwendet wird.

-   Fehler beim gesamten Vorgang mit **WBEM \_ E \_ Access \_ verweigert** und gibt keine Instanzen zurück.

    Der Anbieter kann optional ein Fehler Objekt einschließen, das die Situation für den Client beschreibt. Beachten Sie, dass einige Anbieter möglicherweise serialisiert auf Datenquellen zugreifen und bis auf die Enumeration keine Verweigerungen auftreten.

-   Gibt alle Instanzen zurück, auf die zugegriffen werden kann, gibt jedoch auch den nicht Fehlerstatus Code " **WBEM \_ S \_ Access \_ denied**" zurück.

    Der Anbieter sollte die Verweigerung während der Enumeration beachten und die Bereitstellung von Instanzen fortsetzen, wobei der Statuscode nicht Fehler beendet wird. Der Anbieter kann die Enumeration bei der ersten Verweigerung auch beenden. Die Begründung für diese Option besteht darin, dass unterschiedliche Anbieter unterschiedliche Abruf Paradigmen haben. Ein Anbieter hat möglicherweise bereits Instanzen übermittelt, bevor er eine Zugriffsverletzung entdeckt. Einige Anbieter haben möglicherweise die Möglichkeit, weitere Instanzen bereitzustellen, die andere möglicherweise beenden möchten.

Aufgrund der com-Struktur können Sie keine Informationen während eines Fehlers mit Ausnahme eines Fehler Objekts zurück Mars Hallen. Daher können Sie nicht sowohl Informationen als auch einen Fehlercode zurückgeben. Wenn Sie Informationen zurückgeben möchten, müssen Sie stattdessen einen nicht Fehlerstatus Code verwenden.

## <a name="debugging-your-access-denied-code"></a>Debuggen des Zugriffs verweigerten Codes

Einige Anwendungen verwenden möglicherweise Identitätswechsel Ebenen, die niedriger als die Identitätswechsel **Ebene der RPC- \_ C- \_ \_ Ebene \_** sind. In diesem Fall tritt bei den meisten Identitätswechsel Aufrufen des Anbieters für die Client Anwendung ein Fehler auf. Zum erfolgreichen entwerfen und Implementieren eines Anbieters müssen Sie diese Idee beachten.

Standardmäßig ist die einzige andere Identitätswechsel Ebene, die auf einen Anbieter zugreifen kann, der **RPC- \_ C- \_ IMP- \_ Ebene \_**. In Fällen, in denen eine Client Anwendung die **RPC- \_ C-Ebene " \_ IMP- \_ Ebene \_**" verwendet, gibt " [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) " keinen Fehlercode zurück. Stattdessen nimmt der Anbieter den Client nur zu Identifizierungs Zwecken an. Daher geben die meisten vom Anbieter aufgerufenen Windows-Methoden eine Meldung "Zugriff verweigert" zurück. Dies ist in der Praxis harmlos, da Benutzer keine ungeeigneten Aktionen ausführen dürfen. Allerdings kann es bei der Anbieter Entwicklung nützlich sein, um zu ermitteln, ob der Client tatsächlich einen Identitätswechsel durchgeführt hat.

Der Code erfordert, dass die folgenden Verweise und \# include-Anweisungen ordnungsgemäß kompiliert werden.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
```



Im folgenden Codebeispiel wird veranschaulicht, wie bestimmt wird, ob ein Anbieter erfolgreich eine Client Anwendung angenommen hat.


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

[Festlegen von namepace-Sicherheits Deskriptoren](setting-namespace-security-descriptors.md)
</dt> <dt>

[Sichern Ihres Anbieters](securing-your-provider.md)
</dt> </dl>

 

 
