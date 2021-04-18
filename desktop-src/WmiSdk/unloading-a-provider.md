---
description: Nachdem der WMI-Dienst mit einem Anbieter fertig ist, entlädt er den Anbieter aus dem Arbeitsspeicher.
ms.assetid: 6116769f-3402-42b3-835d-9bdb0fc27ce0
ms.tgt_platform: multiple
title: Entladen eines Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 123d8c4f6b9d9155cdc22dc435635466956bdb0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528466"
---
# <a name="unloading-a-provider"></a>Entladen eines Anbieters

Nachdem der WMI-Dienst mit einem Anbieter fertig ist, entlädt er den Anbieter aus dem Arbeitsspeicher. Der Hauptgrund, warum WMI einen Anbieter entlädt, besteht darin, Systemressourcen zu sparen. Aus diesem Grund müssen Sie Code hinzufügen, der es WMI ermöglicht, den Anbieter auf effiziente Weise zu entladen. Das Intervall, das im Cache Steuerelement angegeben ist, wird für das zweimalige Intervall von WMI zum Entladen eines Anbieters benötigt.

WMI entlädt einen Anbieter auf eine der folgenden Arten:

-   Entladen Sie einen Anbieter, nachdem der Anbieter die ihm gegebenen Aufgaben abgeschlossen hat.
-   Alle Anbieter schnell entladen, wenn der Benutzer das System herunterfährt. Beachten Sie, dass WMI in-Process-Anbieter entladen wird, wenn der WMI-Dienst von der Befehlszeile aus heruntergefahren wird.

Während das erste Szenario häufiger ist, müssen Sie Ihren Anbieter für beide Möglichkeiten schreiben.

In diesem Thema werden die folgenden Abschnitte erläutert:

-   [Entladen eines Leerlauf Anbieters](#unloading-an-idle-provider)
-   [Zugreifen auf die Leerlaufzeit eines Anbieters](#accessing-the-idle-time-for-a-provider)
-   [Entladen eines Anbieters, der auch ein WMI-Client ist](#unloading-a-provider-that-is-also-a-wmi-client)
-   [Entladen eines Anbieters beim Herunterfahren](#unloading-a-provider-during-shutdown)
-   [Zugehörige Themen](#related-topics)

## <a name="unloading-an-idle-provider"></a>Entladen eines Leerlauf Anbieters

WMI führt beim Entladen eines inaktiven Anbieters die folgenden Aktionen aus:

-   Bestimmt, ob sich der Anbieter im Leerlauf befindet.

    WMI verwendet die **clearafter** -Eigenschaft, um zu bestimmen, wie lange ein Anbieter im Leerlauf bleiben kann, bevor der Anbieter entladen wird. Weitere Informationen finden Sie unter [zugreifen auf die Leerlaufzeit eines Anbieters](#accessing-the-idle-time-for-a-provider).

-   Ruft die [**releasemethode**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) des Anbieters auf.

    Wenn es sich bei dem Anbieter um einen reinen Anbieter handelt, wird der Anbieter durch [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) vollständig aus dem aktiven Speicher entfernt. Ein nicht reiner Anbieter kann jedoch nach der **Veröffentlichung** von WMI weiterhin ausgeführt werden.

## <a name="accessing-the-idle-time-for-a-provider"></a>Zugreifen auf die Leerlaufzeit eines Anbieters

Die minimale Zeitspanne, für die ein Anbieter aktiv bleibt, hängt von der **clearafter** -Eigenschaft ab. **Clearafter** finden Sie in Instanzen von Klassen, die von der WMI-System Klasse [**\_ \_ CacheControl**](--cachecontrol.md) im \\ Root-Namespace abgeleitet sind.

In der folgenden Liste werden die Klassen beschrieben, die von [**\_ \_ CacheControl**](--cachecontrol.md)abgeleitet werden und das Entladen des Anbieters steuert:

-   [**\_\_Eventconsumerprovidercachecontrol**](--eventconsumerprovidercachecontrol.md)
-   [**\_\_Eventprovidercachecontrol**](--eventprovidercachecontrol.md)
-   [**\_\_EventSink Cache econtrol**](--eventsinkcachecontrol.md)
-   [**\_\_Objectprovidercachecontrol**](--objectprovidercachecontrol.md)
-   [**\_\_Propertyprovidercachecontrol**](--propertyprovidercachecontrol.md)

Sie können die minimale Zeitspanne ändern, in der ein Anbieter von WMI inaktiv bleiben kann, indem Sie die **clearafter** -Eigenschaft in der Cache Steuerungs Instanz für einen bestimmten Anbietertyp bearbeiten. Um z. b. die Zeitspanne zu begrenzen, in der sich ein Eigenschaften Anbieter im Leerlauf befinden kann, bearbeiten Sie die **clearafter** -Eigenschaft einer [**\_ \_ propertyprovidercachecontrol**](--propertyprovidercachecontrol.md) -Instanz im \\ Root-Namespace.

## <a name="unloading-a-provider-that-is-also-a-wmi-client"></a>Entladen eines Anbieters, der auch ein WMI-Client ist

Der Anbieter muss möglicherweise einen WMI-Client erhalten, nachdem er die von ihm aufgerufenen Anbieter Funktionen abgeschlossen hat. Beispielsweise muss ein pushanbieter möglicherweise Abfragen an WMI ausgeben. Weitere Informationen finden Sie unter [bestimmen des Push-oder Pull-Status](determining-push-or-pull-status.md). In diesem Fall sollte die **Pure** -Eigenschaft der [**\_ \_ Win32Provider**](--win32provider.md) -Instanz, die den Anbieter darstellt, auf **true** festgelegt werden. Wenn die **Pure** -Eigenschaft auf **false** festgelegt ist, bereitet der Anbieter die Entladung vor, indem er [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) für alle ausstehenden Schnittstellen Punkte aufruft, wenn WMI die releasemethode der primären Schnittstelle aufruft. Weitere Informationen finden Sie im Abschnitt "Hinweise" unter [**\_ \_ Win32Provider**](--win32provider.md).

Im folgenden Verfahren wird beschrieben, wie eine releasemethode für die primäre Schnittstelle des Anbieters implementiert wird.

**So entladen Sie einen Anbieter**

1.  Gibt alle für WMI gespeicherten Schnittstellen Zeiger frei, wenn WMI die [**releasemethode**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) der primären Schnittstelle des Anbieters aufruft.

    In der Regel enthält ein Anbieter Zeiger auf die Schnittstellen " [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) " und " [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) ", die in [**iwbemproviderinit:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize)bereitgestellt werden.

2.  Wenn die **Pure** -Eigenschaft in der zugeordneten [**\_ \_ Win32Provider**](--win32provider.md) -Instanz auf **false** festgelegt ist, kann der Anbieter nach der [**Freigabe**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)von WMI auf die Rolle der Client Anwendung umstellen. WMI kann jedoch keinen Anbieter entladen, der als Client System betrieben wird, was den System Aufwand erhöht.

    Ein Anbieter, bei dem **Pure** auf **true** festgelegt ist, ist nur für Service Requests vorhanden. Daher kann diese Art von Anbieter die Rolle einer Client Anwendung nicht annehmen, und Sie kann von WMI entladen werden.

## <a name="unloading-a-provider-during-shutdown"></a>Entladen eines Anbieters beim Herunterfahren

Unter normalen Umständen ermöglicht die Verwendung der Richtlinien zum [Entladen eines Anbieters, der auch ein WMI-Client ist](#unloading-a-provider-that-is-also-a-wmi-client) , das ordnungsgemäße Entladen des Anbieters durch WMI. Es kann jedoch vorkommen, dass WMI die normalen Entlade Prozeduren nicht initiieren kann, z. b. wenn der Benutzer das System heruntergefahren hat. Wenn Sie ein Transaktionsmodell der Datenspeicherung verwenden, können Sie zusätzlich zur Implementierung einer guten Bereinigungs Strategie sicherstellen, dass der Anbieter ordnungsgemäß entladen wurde.

Der Benutzer kann WMI jederzeit abbrechen. In einer solchen Situation werden von WMI keine Anbieter entladen oder der [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) -Einstiegspunkt auf einem in-Process-Anbieter aufgerufen. Wenn ein Prozess interner Anbieter zum Zeitpunkt des herunter Fahrens in der Mitte eines Methoden Aufrufes ist, kann WMI den ausgeführten Thread in der Mitte des Aufrufes möglicherweise beenden. In diesem Fall ruft WMI keine Routinen auf, die normalerweise Cleanup verarbeiten, z. b. einen objektdekonstruktor. WMI ruft höchstens [**DllMain**](/windows/desktop/Dlls/dllmain) auf.

Wenn das Betriebssystem WMI herunterfährt, gibt das System automatisch den gesamten Arbeitsspeicher frei, der einem in-Process-Anbieter zugeordnet ist. Das Betriebssystem schließt außerdem die meisten Ressourcen des Anbieters, z. b. Datei Handles, Fenster Handles usw. Der Anbieter muss eine bestimmte Aktion nicht durchführen, um dies zu erreichen.

Da WMI in der Mitte eines Aufrufes heruntergefahren werden kann, sollte ein Anbieter die Datenquellen nicht in einem inkonsistenten Status belassen. Wenn Sie Ihre Daten in einem inkonsistenten Zustand belassen, ist dies für schreibgeschützte Anbieter kein Problem. Anbieter mit Schreibfunktionen möchten jedoch möglicherweise eine beliebige Art von Transaktionsmodell implementieren, um nach einer abrupten Beendigung ein sicheres Rollback zu ermöglichen.

Das Betriebssystem kann zwar einige allgemeine Systemressourcen freigeben, das System gibt jedoch nicht automatisch alle Ressourcen frei. Beispielsweise kann das Betriebssystem keine Socket-oder Datenbankverbindung freigeben. Der Anbieter muss diese Ressourcen stattdessen manuell bereinigen. Um diese Probleme zu vermeiden, können Sie den Anbieter entweder außerhalb des Prozesses implementieren, oder Sie können Bereinigungs Code hinzufügen.

Die einfachste Lösung ist die Implementierung des Anbieters außerhalb des Prozesses. Ein Out-of-Process-Anbieter wird nicht beendet, wenn WMI heruntergefahren wird, obwohl WMI den Anbieter nach einem com-Timeout freigibt. Anbieter, für die Probleme mit der Bereinigungs-und Beendigungs Stabilität wichtiger sind als die Leistung ist möglicherweise außerhalb des Prozesses.

Wenn Sie Bereinigungs Code in Ihrem Anbieter platzieren müssen, stehen Ihnen zwei Optionen zur Verfügung. Ein Ort zum Ausführen dieser Bereinigungs Art ist " [**DllMain**](/windows/desktop/Dlls/dllmain)", die DLL-Einstiegspunkt Funktion, die das Betriebssystem beim Entladen der DLL aufruft. Der Bereinigungs Code kann direkt in " **DllMain**" eingefügt werden und als Reaktion auf das **Trennen des DLL- \_ Prozesses \_** ausgeführt werden. Das Implementieren von Bereinigungs Code in **DllMain** kann etwas schwierig zu gestalten sein, insbesondere in Programmierumgebungen wie MFC oder ATL. Weitere Informationen finden Sie im Microsoft Knowledge Base-Artikel Q148791, "*How to Add your own DllMain in a MFC Regular dll".* (Diese Ressource ist möglicherweise in einigen Sprachen und Ländern oder Regionen nicht verfügbar.)

Alternativ dazu können Sie auch den Bereinigungs Code im Dekonstruktor einer globalen Klasse platzieren. Weitere Informationen finden Sie unter Entladen eines Anbieters. Das Windows-Betriebssystem weist dem Heap keine globalen Objekte zu. Stattdessen ruft das Betriebssystem beim Entladen der dll die Dekonstruktoren auf.

Im folgenden wird eine einfache Bereinigungs Prozedur beschrieben, die in ein globales WMI-Objekt passen könnte.


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



Es gibt zahlreiche Einschränkungen hinsichtlich der Vorgänge, die im Bereinigungs Code mit beiden Ansätzen durchgeführt werden können. Beispielsweise kann auf beliebige Threads und DLLs, die nicht implizit verknüpft sind, auf beliebige Weise zugegriffen werden. Außerdem können Sie unter keinen Umständen COM-Aufrufe durchführen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen von namepace-Sicherheits Deskriptoren](setting-namespace-security-descriptors.md)
</dt> <dt>

[Sichern Ihres Anbieters](securing-your-provider.md)
</dt> <dt>

[Entwickeln eines WMI-Anbieters](developing-a-wmi-provider.md)
</dt> </dl>

 

 
