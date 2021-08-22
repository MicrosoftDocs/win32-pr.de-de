---
description: Nachdem WMI mit einem Anbieter fertig ist, wird der Anbieter aus dem Arbeitsspeicher entladen.
ms.assetid: 6116769f-3402-42b3-835d-9bdb0fc27ce0
ms.tgt_platform: multiple
title: Entladen eines Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b831f69ba27ab3e173920cc57e7500ef543bb327a04dc5c04dc8b0b9cef31ad0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049958"
---
# <a name="unloading-a-provider"></a>Entladen eines Anbieters

Nachdem WMI mit einem Anbieter fertig ist, wird der Anbieter aus dem Arbeitsspeicher entladen. Der Hauptgrund für das Entladen eines Anbieters durch WMI ist die Einsparung von Systemressourcen. Daher müssen Sie Code hinzufügen, der es WMI ermöglicht, Ihren Anbieter effizient zu entladen. Es dauert von dem im Cachesteuerelement angegebenen Intervall bis zum doppelten Intervall, bis WMI einen Anbieter entlädt.

WMI entlädt einen Anbieter auf eine der folgenden Arten:

-   Entladen Sie einen Anbieter, nachdem der Anbieter die ihm übergebenen Aufgaben abgeschlossen hat.
-   Entladen Sie schnell alle Anbieter, wenn der Benutzer das System herunterfährt. Beachten Sie, dass WMI In-Process-Anbieter entlädt, wenn der WMI-Dienst über die Befehlszeile heruntergefahren wird.

Während das erste Szenario häufiger vorliegt, müssen Sie Ihren Anbieter für beide Möglichkeiten schreiben.

Die folgenden Abschnitte werden in diesem Thema erläutert:

-   [Entladen eines Leerlaufanbieters](#unloading-an-idle-provider)
-   [Zugreifen auf die Leerlaufzeit für einen Anbieter](#accessing-the-idle-time-for-a-provider)
-   [Entladen eines Anbieters, der auch ein WMI-Client ist](#unloading-a-provider-that-is-also-a-wmi-client)
-   [Entladen eines Anbieters während des Herunterfahrens](#unloading-a-provider-during-shutdown)
-   [Zugehörige Themen](#related-topics)

## <a name="unloading-an-idle-provider"></a>Entladen eines Leerlaufanbieters

WMI führt die folgenden Aktionen aus, wenn ein Leerlaufanbieter entladen wird:

-   Bestimmt, ob sich der Anbieter im Leerlauf befindet.

    WMI verwendet die **ClearAfter-Eigenschaft,** um zu bestimmen, wie lange ein Anbieter im Leerlauf bleiben kann, bevor dieser Anbieter entladen wird. Weitere Informationen finden Sie unter [Zugreifen auf die Leerlaufzeit für einen Anbieter.](#accessing-the-idle-time-for-a-provider)

-   Ruft die [**Release-Methode**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) des Anbieters auf.

    Wenn der Anbieter ein reiner Anbieter war, entfernt [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) den Anbieter vollständig aus dem aktiven Arbeitsspeicher. Allerdings kann ein nichtpure-Anbieter weiterhin ausgeführt werden, nachdem WMI **Release** aufruft.

## <a name="accessing-the-idle-time-for-a-provider"></a>Zugreifen auf die Leerlaufzeit für einen Anbieter

Die Mindestdauer, in der ein Anbieter aktiv bleibt, wird durch die **ClearAfter-Eigenschaft** bestimmt. **ClearAfter** befindet sich in Instanzen von Klassen, die von der WMI-Systemklasse [**\_ \_ CacheControl**](--cachecontrol.md) abgeleitet wurden, im \\ Stammnamespace.

In der folgenden Liste werden die Klassen beschrieben, die von [**\_ \_ CacheControl**](--cachecontrol.md)abgeleitet sind und das Entladen des Anbieters steuert:

-   [**\_\_EventConsumerProviderCacheControl**](--eventconsumerprovidercachecontrol.md)
-   [**\_\_EventProviderCacheControl**](--eventprovidercachecontrol.md)
-   [**\_\_EventSinkCacheControl**](--eventsinkcachecontrol.md)
-   [**\_\_ObjectProviderCacheControl**](--objectprovidercachecontrol.md)
-   [**\_\_PropertyProviderCacheControl**](--propertyprovidercachecontrol.md)

Sie können die Mindestdauer ändern, die WMI einem Anbieter ermöglicht, inaktiv zu bleiben, indem Sie die **ClearAfter-Eigenschaft** in der Cachesteuerelementinstanz für einen bestimmten Anbietertyp bearbeiten. Um beispielsweise die Zeitspanne einzuschränken, die ein Eigenschaftenanbieter im Leerlauf bleiben kann, würden Sie die **ClearAfter-Eigenschaft** einer [**\_ \_ PropertyProviderCacheControl-Instanz**](--propertyprovidercachecontrol.md) im \\ Stammnamespace bearbeiten.

## <a name="unloading-a-provider-that-is-also-a-wmi-client"></a>Entladen eines Anbieters, der auch ein WMI-Client ist

Ihr Anbieter muss möglicherweise ein WMI-Client bleiben, nachdem er die Anbieterfunktionen abgeschlossen hat, für die er aufgerufen wurde. Beispielsweise muss ein Pushanbieter möglicherweise Abfragen an WMI ausstellen. Weitere Informationen finden Sie unter [Bestimmen des Push- oder Pullstatus.](determining-push-or-pull-status.md) In diesem Fall sollte die **Pure-Eigenschaft** der [**\_ \_ Win32Provider-Instanz,**](--win32provider.md) die den Anbieter darstellt, auf **TRUE** festgelegt werden. Wenn die **Pure-Eigenschaft** auf **FALSE** festgelegt ist, bereitet der Anbieter das Entladen vor, indem [**er IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) auf allen ausstehenden Schnittstellenpunkten aufruft, wenn WMI die Release-Methode seiner primären Schnittstelle aufruft. Weitere Informationen finden Sie im Abschnitt "Hinweise" in [**\_ \_ Win32Provider.**](--win32provider.md)

Im folgenden Verfahren wird beschrieben, wie Sie eine Releasemethode für die primäre Schnittstelle Ihres Anbieters implementieren.

**So entladen Sie einen Anbieter**

1.  Geben Sie alle Schnittstellenzeiger frei, die für WMI gehalten werden, wenn WMI die [**Release-Methode**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) der primären Schnittstelle Ihres Anbieters aufruft.

    In der Regel enthält ein Anbieter Zeiger auf die [**IWbemServices-**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) und [**IWbemContext-Schnittstellen,**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) die in [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize)bereitgestellt werden.

2.  Wenn die **Pure-Eigenschaft** in der zugeordneten [**\_ \_ Win32Provider-Instanz**](--win32provider.md) auf **FALSE** festgelegt ist, kann der Anbieter auf die Rolle der Clientanwendung umsteigen, nachdem WMI [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)aufruft. WMI kann jedoch keinen Anbieter entladen, der als Clientsystem betrieben wird, was den Systemaufwand erhöht.

    Ein Anbieter, bei dem **Pure** auf **TRUE** festgelegt ist, ist nur für Dienstanforderungen vorhanden. Daher kann dieser Anbietertyp nicht die Rolle einer Clientanwendung übernehmen, und WMI kann sie entladen.

## <a name="unloading-a-provider-during-shutdown"></a>Entladen eines Anbieters während des Herunterfahrens

Unter normalen Umständen ermöglicht die Verwendung der Richtlinien unter Entladen eines Anbieters, bei dem es sich auch um [einen WMI-Client handelt,](#unloading-a-provider-that-is-also-a-wmi-client) das ordnungsgemäße Entladen Ihres Anbieters durch WMI. Es kann jedoch zu Situationen kommen, in denen WMI die normalen Entladevorgänge nicht einleiten kann, z. B. wenn der Benutzer das System herunterfahren möchte. Durch die Verwendung eines Transaktionsmodells des Datenspeichers können Sie zusätzlich zur Implementierung einer guten Bereinigungsstrategie sicherstellen, dass Ihr Anbieter ordnungsgemäß entladen wird.

Der Benutzer kann WMI jederzeit beenden. In einer solchen Situation entlädt WMI keine Anbieter und ruft den [**DllCanUnloadNow-Einstiegspunkt**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) auf keinem In-Process-Anbieter auf. Wenn sich ein In-Process-Anbieter zum Zeitpunkt des Herunterfahrens in der Mitte eines Methodenaufrufs befindet, kann WMI den ausgeführten Thread möglicherweise in der Mitte des Aufrufs beenden. In diesem Fall ruft WMI keine Routinen auf, die normalerweise die Bereinigung verarbeiten, z. B. einen Objektdetruktor. Höchstens ruft WMI [**nur DllMain**](/windows/desktop/Dlls/dllmain) auf.

Wenn das Betriebssystem WMI herunterfährt, gibt das System automatisch den gesamten Arbeitsspeicher frei, der einem Prozessanbieter zugeordnet ist. Das Betriebssystem schließt auch die meisten Vom Anbieter gehaltenen Ressourcen, z. B. Dateihandles, Fensterhandles usw. Der Anbieter muss keine bestimmten Maßnahmen ergreifen, um dies zu ermöglichen.

Da WMI während eines Aufrufs heruntergefahren werden kann, sollte ein Anbieter Datenquellen nicht in einem inkonsistenten Zustand belassen. Die Daten in einem inkonsistenten Zustand zu belassen, ist kein Problem für schreibgeschützte Anbieter. Anbieter mit Schreibfunktionen möchten jedoch möglicherweise ein Transaktionsmodell implementieren, um einen sicheren Rollback nach einer plötzlichen Beendigung zu ermöglichen.

Während das Betriebssystem möglicherweise einige allgemeine Systemressourcen freigibt, gibt das System nicht automatisch alle Ressourcen frei. Beispielsweise gibt das Betriebssystem möglicherweise keinen Socket oder eine Datenbankverbindung frei. Stattdessen muss der Anbieter solche Ressourcen möglicherweise manuell bereinigen. Um diese Probleme zu vermeiden, können Sie entweder ihren Anbieter prozessfrei implementieren oder Bereinigungscode hinzufügen.

Die einfachste Lösung ist die Out-of-Process-Implementierung Ihres Anbieters. Ein Out-of-Process-Anbieter wird nicht beendet, wenn WMI heruntergefahren wird, obwohl WMI den Anbieter nach einem COM-Timeout freigibt. Anbieter, für die Probleme mit der Bereinigungs- und Beendigungs robuster sind als die Leistung, sind möglicherweise nicht prozessbearbeitend.

Wenn Sie Bereinigungscode in Ihrem Anbieter platzieren müssen, haben Sie zwei Möglichkeiten. Ein Ort zum Durchführen dieser Art von Bereinigung ist [**DllMain.**](/windows/desktop/Dlls/dllmain)Die DLL-Einstiegspunktfunktion, die das Betriebssystem beim Entladen der DLL aufruft. Bereinigungscode kann direkt in **DllMain** hinzugefügt werden und als Reaktion auf **DLL PROCESS \_ \_ DETACH** ausgeführt werden. Das Implementieren von Bereinigungscode in **DllMain** kann etwas schwierig zu anordnen sein, insbesondere in Programmierumgebungen wie MFC oder ATL. Weitere Informationen finden Sie im Microsoft Knowledge Base Artikel Q148791,*" How to Provide Your Own DllMain in an MFC Regular DLL".* (Diese Ressource ist in einigen Sprachen und Ländern oder Regionen möglicherweise nicht verfügbar.)

Alternativ können Sie den Bereinigungscode auch im Destruktor einer globalen Klasse platzieren. Weitere Informationen finden Sie unter Entladen eines Anbieters. Das Windows Betriebssystem ordnet keine globalen Objekte auf dem Heap zu. Stattdessen ruft das Betriebssystem die Destruktoren beim Entladen der DLL auf.

Im Folgenden wird eine einfache Bereinigungsprozedur beschrieben, die in ein globales Objekt für WMI passen kann.


```C++
class CMyCleanup
{
    ~CMyCleanup()
    {
        CloseHandle(m_hOpenFile);
        CloseDatabaseConnection(g_hDatabase);
    }
} g_Cleanup;
```



Es gibt viele Einschränkungen hinsichtlich der Möglichkeiten, die im Bereinigungscode mit beiden Ansätzen ausgeführt werden können. Beispielsweise kann auf weder Threads noch DLLs, die nicht implizit verknüpft sind, in irgendeiner Weise zugegriffen werden. Darüber hinaus können Sie unter keinen Umständen COM-Aufrufe tätigen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen von Namepace-Sicherheitsbeschreibungen](setting-namespace-security-descriptors.md)
</dt> <dt>

[Schützen Ihres Anbieters](securing-your-provider.md)
</dt> <dt>

[Entwickeln eines WMI-Anbieters](developing-a-wmi-provider.md)
</dt> </dl>

 

 
