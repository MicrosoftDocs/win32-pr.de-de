---
description: WMI stellt über WMI-Anbieter Daten zu überschaubaren Windows-Objekten zur Verfügung.
ms.assetid: 74558c6e-28b6-479f-9de6-2fbad793ae26
ms.tgt_platform: multiple
title: Bereitstellen von Daten für WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60df0384bd6f512b931870775067d9d9e6d4077d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753681"
---
# <a name="providing-data-to-wmi"></a>Bereitstellen von Daten für WMI

WMI stellt über WMI- [*Anbieter*](gloss-p.md)Daten zu überschaubaren Windows-Objekten zur Verfügung. Ein Anbieter ruft Daten von einer Systemkomponente (z. b. einem Prozess) oder einer instrumentierten Anwendung (z. b. SNMP oder IIS) ab und übergibt diese Daten über WMI an eine Verwaltungs Anwendung. Wenn z. b. eine Anwendung oder ein Skript mithilfe der WMI- [**Win32- \_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process) Klasse Prozessinformationen anfordert, werden die Daten dynamisch über einen vorinstallierten Anbieter abgerufen.

In diesem Thema werden die folgenden Abschnitte erläutert:

-   [Erstellen eines Modells für ein verwaltbares Objekt](#creating-a-model-for-a-manageable-object)
-   [Implementieren eines Modells für ein verwaltbares Objekt](#implementing-a-model-for-a-manageable-object)
-   [Bestimmen eines zu implementierenden Anbieter Typs](#determining-a-provider-type-to-implement)
-   [Bestimmen eines Hostingmodells (Implementierung) für einen Anbieter](#determining-a-hosting-implementation-model-for-a-provider)
-   [Implementieren eines Anbieters](#implementing-a-provider)
-   [Registrieren eines Anbieters bei WMI und dem System](#registering-a-provider-with-wmi-and-the-system)
-   [Testen eines Anbieters](#testing-a-provider)
-   [Zugehörige Themen](#related-topics)

## <a name="creating-a-model-for-a-manageable-object"></a>Erstellen eines Modells für ein verwaltbares Objekt

Erstellen Sie vor der Entwicklung eines Anbieters ein Datenmodell, das das verwaltbare Objekt darstellt, das über WMI verfügbar gemacht werden soll. Sie planen, welche Datenobjekte der Anbieter verfügbar macht. Wenn Sie z. b. die Bildschirmauflösung des Desktop Hintergrunds verwalten möchten, müssen Sie entscheiden, wie der Desktop in einer [*MOF-Datei (Managed Object Format)*](gloss-m.md) modelliert werden soll.

So erstellen Sie ein nützliches Modell:

-   Ermitteln Sie reale Szenarien, und modellieren Sie die Informationen, die ein Kunde möglicherweise lesen und aktualisieren möchte (z. b. Ändern des Hintergrund Bilds) für jedes verwaltbare Objekt. Dies sind Ihre Klasseneigenschaften.
-   Bestimmen Sie, welche Art von Aktionen ein Kunde mit jedem verwaltbaren Objekt ausführen kann. Dabei handelt es sich um ihre Methoden.

## <a name="implementing-a-model-for-a-manageable-object"></a>Implementieren eines Modells für ein verwaltbares Objekt

Um ein Modell für verwaltbare Objekte zu implementieren, erstellen Sie eine MOF-Datei, die eine WMI-Klasse enthält, die jedes Objekt darstellt. Weitere Informationen zum Erstellen einer MOF-Datei zum Definieren von WMI-Klassen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](designing-managed-object-format--mof--classes.md). Die Registrierung des Anbieters und seiner Klassen ist in der Regel in der MOF-Datei enthalten, obwohl es möglich ist, die [com-API](com-api-for-wmi.md) zum Erstellen von Klassen und Methoden zu verwenden. Weitere Informationen finden Sie unter [Entwickeln eines WMI-Anbieters](developing-a-wmi-provider.md).

> [!Note]  
> Um sicherzustellen, dass alle ihre WMI-Klassendefinitionen für verwaltete Objekte im [*WMI-Repository*](gloss-w.md) wieder hergestellt werden, wenn WMI einen Fehler aufweist und neu gestartet wird, verwenden Sie die " [**\# pragma Auto Wiederherstellen**](pragma-autorecover.md) "-Präprozessoranweisung in der [*MOF-Datei (Managed Object Format)*](gloss-m.md) .

 

Nachdem Sie die MOF-Datei erstellt haben, kompilieren Sie Sie mit dem [**Mofcomp.exe**](mofcomp.md) Tool. Dies benachrichtigt Sie über Fehler in der MOF-Datei und fügt die WMI-Klasse, die in der MOF-Datei definiert ist, dem [*WMI-Repository*](gloss-w.md) hinzu, sodass die Klasse von einem Anbieter verwendet werden kann.

## <a name="determining-a-provider-type-to-implement"></a>Bestimmen eines zu implementierenden Anbieter Typs

WMI unterstützt eine bestimmte Anzahl von Anbieter Typen, die die Art der von den Anbietern unterstützten Informationen und Vorgänge bestimmt.

Die Anbieter Typen lauten wie folgt:

-   [*Instanzanbieter*](gloss-i.md)
-   [*Methoden Anbieter*](gloss-m.md)
-   [*Eigenschaften Anbieter*](gloss-p.md)
-   Klassen Anbieter
-   [*Ereignis Anbieter*](gloss-e.md)
-   [*Ereignisconsumeranbieter*](gloss-e.md)
-   [*Zuordnungs Anbieter*](gloss-a.md)

Die meisten Anbieter sind Instanzanbieter und Methoden Anbieter. Ein Instanzanbieter ist der häufigste Anbieter und stellt die Instanzen einer bestimmten Klasse bereit. Ein Methoden Anbieter implementiert die Methoden von einer oder mehreren Klassen. Weitere Informationen zu den Anbieter Typen finden Sie unter [Entwickeln eines WMI-Anbieters](developing-a-wmi-provider.md).

## <a name="determining-a-hosting-implementation-model-for-a-provider"></a>Bestimmen eines Hostingmodells (Implementierung) für einen Anbieter

WMI-Anbieter sind Binärdateien, die als COM-Objekte implementiert werden. Dies bedeutet, dass jeder Anbieter über eine DLL-Datei verfügt, die innerhalb eines bestimmten Prozesses und Sicherheits Kontexts ausgeführt werden kann. Dabei bezieht sich WMI auf das [*Hostingmodell*](gloss-h.md). WMI bietet verschiedene Möglichkeiten zum Hosten von Anbietern, die häufigste Methode ist jedoch, das gekoppelte Anbieter Modell (das unter dem WMI-Prozess ausgeführt wird) im networkservicehost-Sicherheitskontext zu verwenden. Ein WMI-Anbieter kann als gekoppelt oder [*entkoppelt*](gloss-d.md)klassifiziert werden.

Der Begriff gekoppelt oder entkoppelter Anbieter bestimmt, unter welchem Host Prozess der Anbieter in Bezug auf den WMIPRVSE.EXE Prozess bereitgestellten WMI ausgeführt wird. Eine bewährte Vorgehensweise besteht darin zu bestimmen, ob die vom Anbieter verfügbar gemachten Verwaltungsdaten und die API oder Anwendung, von der er abhängt, immer im System verfügbar sind. Wenn die API oder Anwendung, auf der der Anbieter basiert, immer verfügbar ist (auf dem System ausgeführt), sollte der Anbieter ein verbundener Anbieter sein. andernfalls muss er ein entkoppelter Anbieter sein. Weitere Informationen zum Hosting von Modellen finden Sie unter [Anbieter Hosting und-Sicherheit](provider-hosting-and-security.md).

Weitere Informationen zum Erstellen eines gekoppelten Anbieters finden [Sie unter Bereitstellen von Daten für WMI durch Schreiben eines Anbieters](supplying-data-to-wmi-by-writing-a-provider.md). Informationen zum Einbinden eines entkoppelten Anbieters in eine Anwendung finden Sie unter [Einbinden eines Anbieters in eine Anwendung](incorporating-a-provider-in-an-application.md).

Gekoppelte Anbieter können als Prozess intern (in-proc) oder außerhalb des Prozesses (Out-of-Process) beschrieben werden. Wenn ein verbundener Anbieter ein in-proc-Anbieter ist, wird er unter einem freigegebenen WMIPRVSE.EXE WMI-Hostingprozess ausgeführt und als com in-proc Server (. dll) implementiert. Wenn es sich bei einem Anbieter um einen Out-of-proc-Anbieter handelt, wird er von WMI auf Anforderung eines Clients oder Ereignisses gestartet. er wird jedoch als getrennter Prozess ausgeführt und als ausführbare Datei (. exe) implementiert.

## <a name="implementing-a-provider"></a>Implementieren eines Anbieters

Ein Anbieter kann auf folgende Weise implementiert werden:

-   Verwenden des ATL-Assistenten in Visual Studio

    Der ATL-Assistent generiert Anbieter Code, der einen verbundenen Anbieter implementiert. Während Sie den ATL-Assistenten verwenden, können Sie angeben, dass Sie ein in-proc-(. dll) oder out-of-proc-Anbieter-Lauf Zeitmodell (. exe) erstellen möchten.

-   Definieren eines COM-Objekts, das Ihren Anbieter enthalten soll.

    Der Anbieter Code ist in C++ geschrieben. Weitere Informationen finden Sie unter [Bereitstellen von Daten für WMI durch Schreiben eines Anbieters](supplying-data-to-wmi-by-writing-a-provider.md).

-   Verwenden Sie die Klassen im [**Microsoft. Management. Infrastructure**](/previous-versions//hh872326(v=vs.85)) -Namespace in der .NET Framework, um einen Anbieter mit verwaltetem Code zu erstellen. (Der **System. Management. Instrumentation** -Namespace wird nicht mehr unterstützt.)

    Bei diesem Vorgang wird ein entkoppelter Anbieter erstellt.

## <a name="registering-a-provider-with-wmi-and-the-system"></a>Registrieren eines Anbieters bei WMI und dem System

Bevor der Anbieter von einem Consumer verwendet wird, ist es wichtig, ihn beim WMI-System und dem Windows com-Subsystem zu registrieren.

Eine MOF-Datei kann mehrere Typen von Anbietern für die gleichen Klassen enthalten. Der gleiche Anbieter Name wird registriert, z. b. eine-Instanz oder ein-Methoden Anbieter. Weitere Informationen finden Sie unter [Registrieren eines Anbieters](registering-a-provider.md).

## <a name="testing-a-provider"></a>Testen eines Anbieters

Wenn der Anbieter Code registriert ist, ist es wichtig, den Anbieter ordnungsgemäß zu testen, indem er den Anbieter von unterschiedlichen Consumern verwendet (z. b. Skripts, verwalteten .NET-Code und C++-Consumer).

Führen Sie die folgenden Aufgaben aus, um den Anbieter zu testen:

-   Stellen Sie sicher, dass der Anbieter ordnungsgemäß geladen wird, indem Sie die Ereignis Benachrichtigungen für das [**MSFT \_ WMIProvider \_ operationevent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-operationevent) nachverfolgen Diese Ereignisse werden Sie über etwaige Anbieter Ladefehler informieren. Weitere Problem Behandlungs Klassen, die hilfreich sein können, sind [**Win32 \_ ProcessStartTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstarttrace) und [**Win32 \_ ProcessStopTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace). Weitere Informationen zur Problembehandlung bei Anbietern finden Sie unter [Debuggen von Anbietern](debugging-providers.md) und [Anbieter Konfiguration und Problem](provider-configuration-and-troubleshooting-classes.md)Behandlung von Klassen.
-   Wenn es sich bei dem Anbieter um eine Instanz oder einen Methoden Anbieter handelt, stellen Sie sicher, dass Sie jede Anbieter Funktion nacheinander testen, um Verwirrung in der folgenden Code Logik zu vermeiden.
-   Erstellen Sie für einen Instanzanbieter eine Client Anwendung oder ein Skript, das jede Schnittstelle des Anbieters aufruft (Enumeration, Get, Put und DELETE). Auch wenn der Anbieter nichts implementieren soll, sollte er eine Meldung "nicht unterstützt" zurückgeben. Sie finden die Rückgabewerte, die bereits in [WMI-Rückgabe Codes](wmi-return-codes.md)definiert sind.
-   Um sicherzustellen, dass der gewünschte Sicherheitskontext wie geplant funktioniert, rufen Sie die vom Anbieter unterstützten Vorgänge aus einem Sicherheitskontext ohne Administratorrechte auf. Der Anbieter muss Identitätswechsel unterstützen. Wenn ein Benutzer, der über die richtigen Sicherheits Anmelde Informationen verfügt, versucht, Daten zu aktualisieren oder einen Vorgang auszuführen, der eine Methode ausführt, sollte der Anbieter den Zugriff mit der entsprechenden Fehlermeldung verweigern.
-   Weitere Informationen zur Anbieter Sicherheit finden Sie unter [Sichern Ihres Anbieters](securing-your-provider.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwickeln eines WMI-Anbieters](developing-a-wmi-provider.md)
</dt> <dt>

[Anbieter Hosting und-Sicherheit](provider-hosting-and-security.md)
</dt> <dt>

[Bereitstellen von Daten für WMI durch Schreiben eines Anbieters](supplying-data-to-wmi-by-writing-a-provider.md)
</dt> <dt>

[Einbinden eines Anbieters in eine Anwendung](incorporating-a-provider-in-an-application.md)
</dt> <dt>

[Registrieren eines Anbieters](registering-a-provider.md)
</dt> <dt>

[Problembehandlung bei WMI-Client Anwendungen](troubleshooting-wmi-client-applications.md)
</dt> <dt>

[Sichern Ihres Anbieters](securing-your-provider.md)
</dt> <dt>

[Erhalten und Bereitstellen von Daten auf einer 64-Bit-Plattform](getting-and-providing-data-on-a-64-bit-computer.md)
</dt> </dl>

 

 
