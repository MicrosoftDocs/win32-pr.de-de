---
description: WMI stellt Daten zu Windows verwalteten Objekten über WMI-Anbieter zur Verfügung.
ms.assetid: 74558c6e-28b6-479f-9de6-2fbad793ae26
ms.tgt_platform: multiple
title: Bereitstellen von Daten für WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f22fbff46959c001f589587f21b8b2b50ab5c5187d387338f407bf45e3e1a29d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316574"
---
# <a name="providing-data-to-wmi"></a>Bereitstellen von Daten für WMI

WMI stellt Daten zu Windows verwalteten Objekten über WMI-Anbieter [*zur Verfügung.*](gloss-p.md) Ein Anbieter ruft Daten aus einer Systemkomponente wie einem Prozess oder einer instrumentierten Anwendung wie SNMP oder IIS ab und übergibt diese Daten über WMI an eine Verwaltungsanwendung. Wenn beispielsweise eine Anwendung oder ein Skript Prozessinformationen mithilfe der WMI [**Win32 \_ Process-Klasse**](/windows/desktop/CIMWin32Prov/win32-process) an fordert, werden die Daten dynamisch über einen vorinstallierten Anbieter erhalten.

In diesem Thema werden die folgenden Abschnitte erläutert:

-   [Erstellen eines Modells für ein verwaltbares Objekt](#creating-a-model-for-a-manageable-object)
-   [Implementieren eines Modells für ein verwaltbares Objekt](#implementing-a-model-for-a-manageable-object)
-   [Bestimmen eines zu implementierenden Anbietertyps](#determining-a-provider-type-to-implement)
-   [Bestimmen eines Hostingmodells (Implementierung) für einen Anbieter](#determining-a-hosting-implementation-model-for-a-provider)
-   [Implementieren eines Anbieters](#implementing-a-provider)
-   [Registrieren eines Anbieters bei WMI und dem System](#registering-a-provider-with-wmi-and-the-system)
-   [Testen eines Anbieters](#testing-a-provider)
-   [Zugehörige Themen](#related-topics)

## <a name="creating-a-model-for-a-manageable-object"></a>Erstellen eines Modells für ein verwaltbares Objekt

Erstellen Sie vor der Entwicklung eines Anbieters ein Datenmodell, das das verwaltbare Objekt darstellen soll, das über WMI verfügbar gemacht werden soll. Sie planen, welche Datenobjekte ihr Anbieter verfügbar macht. Wenn Sie z. B. die Bildschirmauflösung des Desktophintergrunds verwalten möchten, müssen Sie entscheiden, wie der Desktop in einer [*MOF-Datei (Managed Object Format) modelliert werden*](gloss-m.md) soll.

So erstellen Sie ein nützliches Modell:

-   Bestimmen Sie reale Szenarien, und modellieren Sie die Informationen, die ein Kunde möglicherweise lesen und aktualisieren möchte (z. B. das Ändern des Hintergrundbilds) für jedes verwaltbare Objekt. Dies sind Ihre Klasseneigenschaften.
-   Bestimmen Sie, welche Art von Aktionen ein Kunde mit jedem verwaltbaren Objekt ausführen möchte. Dies sind Ihre Methoden.

## <a name="implementing-a-model-for-a-manageable-object"></a>Implementieren eines Modells für ein verwaltbares Objekt

Um ein Modell für verwaltbare Objekte zu implementieren, erstellen Sie eine MOF-Datei, die eine WMI-Klasse enthält, die jedes Objekt darstellt. Weitere Informationen zum Erstellen einer MOF-Datei zum Definieren von WMI-Klassen finden Sie unter Entwerfen Managed Object Format [-Klassen (MOF).](designing-managed-object-format--mof--classes.md) Die Registrierung des Anbieters und seiner Klassen ist in der Regel in der MOF-Datei enthalten, obwohl es möglich ist, die [COM-API](com-api-for-wmi.md) zum Erstellen von Klassen und Methoden zu verwenden. Weitere Informationen finden Sie unter [Entwickeln eines WMI-Anbieters.](developing-a-wmi-provider.md)

> [!Note]  
> Um sicherzustellen, dass alle WMI-Klassendefinitionen für verwaltete Objekte im [*WMI-Repository*](gloss-w.md) wiederhergestellt werden, wenn WMI einen Fehler auftrat und neu gestartet wird, verwenden Sie die [**\# Präprozessoranweisung pragma autorecover**](pragma-autorecover.md) in Der [*Managed Object Format-Datei (MOF).*](gloss-m.md)

 

Nachdem Sie die MOF-Datei erstellt haben, kompilieren Sie sie mit dem [**Mofcomp.exe**](mofcomp.md) Tool. Dadurch werden Sie über Fehler in der MOF-Datei benachrichtigt, und die in der MOF-Datei definierte WMI-Klasse wird dem [*WMI-Repository*](gloss-w.md) so hinzufügt, dass die Klasse von einem Anbieter verwendet werden kann.

## <a name="determining-a-provider-type-to-implement"></a>Bestimmen eines zu implementierenden Anbietertyps

WMI unterstützt eine bestimmte Anzahl von Anbietertypen, die die Art der bereitgestellten Informationen und der von den Anbietern unterstützten Vorgänge bestimmen.

Die Anbietertypen sind:

-   [*Instanzanbieter*](gloss-i.md)
-   [*Methodenanbieter*](gloss-m.md)
-   [*Eigenschaftenanbieter*](gloss-p.md)
-   Klassenanbieter
-   [*Ereignisanbieter*](gloss-e.md)
-   [*Ereignisverbraucheranbieter*](gloss-e.md)
-   [*Zuordnungsanbieter*](gloss-a.md)

Die große Mehrheit der Anbieter sind Instanzanbieter und Methodenanbieter. Ein Instanzanbieter ist der gängigste Anbieter und stellt die Instanzen einer bestimmten Klasse zur Hand. Ein Methodenanbieter implementiert die Methoden einer oder mehrere Klassen. Weitere Informationen zu den Anbietertypen finden Sie unter [Entwickeln eines WMI-Anbieters.](developing-a-wmi-provider.md)

## <a name="determining-a-hosting-implementation-model-for-a-provider"></a>Bestimmen eines Hostingmodells (Implementierung) für einen Anbieter

WMI-Anbieter sind Binärdateien, die als COM-Objekte implementiert werden. Dies bedeutet, dass jeder Anbieter über eine DLL-Datei verfügt, die innerhalb eines bestimmten Prozesses und Sicherheitskontexts ausgeführt werden kann. WMI bezeichnet dies als [*Hostingmodell.*](gloss-h.md) WMI bietet verschiedene Möglichkeiten zum Hosten von Anbietern, aber der gängigste Ansatz ist die Verwendung des gekoppelten Anbietermodells (das unter dem WMI-Prozess ausgeführt wird) im NetworkServiceHost-Sicherheitskontext. Ein WMI-Anbieter kann entweder als gekoppelt oder [*entkoppelt klassifiziert werden.*](gloss-d.md)

Der Begriff gekoppelter oder entkoppelter Anbieter bestimmt, unter welchem Hostprozess der Anbieter in Bezug auf den WMI-WMIPRVSE.EXE wird. Eine bewährte Methode besteht in der Ermittlung, ob die vom Anbieter verfügbar gestellten Verwaltungsdaten und die API oder Anwendung, auf der bzw. der er basiert, immer im System verfügbar sind oder nicht. Wenn die API oder Anwendung, auf die sich der Anbieter stützt, immer verfügbar ist (wird auf dem System ausgeführt), sollte der Anbieter ein gekoppelter Anbieter sein. Ander denn, er muss ein entkoppelter Anbieter sein. Weitere Informationen zum Hosten von Modellen finden Sie unter [Anbieterhosting und Sicherheit.](provider-hosting-and-security.md)

Weitere Informationen zum Erstellen eines gekoppelten Anbieters finden Sie unter [Supplying Data to WMI by Writing a Provider](supplying-data-to-wmi-by-writing-a-provider.md)(Bereitstellung von Daten für WMI durch Schreiben eines Anbieters). Informationen zum Integrieren eines entkoppelten Anbieters in eine Anwendung finden Sie unter Integrieren eines Anbieters in eine [Anwendung.](incorporating-a-provider-in-an-application.md)

Gekoppelte Anbieter können als in-process (in-proc) oder out-of-process (out-of-proc) beschrieben werden. Wenn ein gekoppelter Anbieter ein In-Proc-Anbieter ist, wird er unter einem freigegebenen WMIPRVSE.EXE-WMI-Hostingprozess ausgeführt und als COM-In-Proc-Server (.dll) implementiert. Wenn ein Anbieter ein Out-of-Proc-Anbieter ist, wird er von WMI auf Anforderung eines Clients oder Ereignisses gestartet, aber als separater Prozess ausgeführt und als ausführbare Datei (.exe) implementiert.

## <a name="implementing-a-provider"></a>Implementieren eines Anbieters

Ein Anbieter kann auf folgende Weise implementiert werden:

-   Verwenden des ATL-Assistenten in Visual Studio.

    Der ATL-Assistent generiert Anbietercode, der einen gekoppelten Anbieter implementiert. Bei Verwendung des ATL-Assistenten können Sie angeben, dass Sie ein In-Proc- (.dll) oder out-of-proc (.exe)-Anbieter-Laufzeitmodell erstellen möchten.

-   Definieren eines COM-Objekts, das Ihren Anbieter enthalten soll.

    Der Anbietercode ist in C++ geschrieben. Weitere Informationen finden Sie unter [Supplying Data to WMI by Writing a Provider](supplying-data-to-wmi-by-writing-a-provider.md).

-   Verwenden sie die Klassen im [**Namespace Microsoft.Management.Infrastructure**](/previous-versions//hh872326(v=vs.85)) im .NET Framework, um einen Anbieter mithilfe von verwaltetem Code zu erstellen. (Der **System.Management.Instrumentation-Namespace** wird nicht mehr unterstützt.)

    Bei diesem Prozess wird ein entkoppelter Anbieter erstellt.

## <a name="registering-a-provider-with-wmi-and-the-system"></a>Registrieren eines Anbieters bei WMI und dem System

Bevor Sie den Anbieter eines Consumers verwenden, ist es wichtig, ihn beim WMI-System und dem Windows COM-Subsystem zu registrieren.

Eine MOF-Datei kann mehrere Anbietertypen für die gleichen Klassen enthalten. Der gleiche Anbietername wird z. B. als Instanz oder Methodenanbieter registriert. Weitere Informationen finden Sie unter [Registrieren eines Anbieters.](registering-a-provider.md)

## <a name="testing-a-provider"></a>Testen eines Anbieters

Wenn der Anbietercode registriert ist, ist es wichtig, den Anbieter ordnungsgemäß zu testen, indem Sie den Anbieter von verschiedenen Consumers (z. B. Skripts, verwalteten .NET-Code und C++-Consumers) verwenden.

Führen Sie die folgenden Aufgaben aus, um Ihren Anbieter zu testen:

-   Stellen Sie sicher, dass Ihr Anbieter ordnungsgemäß geladen wird, indem Sie die [**MSFT \_ WmiProvider \_ OperationEvent-Ereignisbenachrichtigungen**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-operationevent) nachverfolgen. Diese Ereignisse informieren Sie über alle Fehler beim Laden des Anbieters. Weitere Problembehandlungsklassen, die hilfreich sein können, sind [**Win32 \_ ProcessStartTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstarttrace) und [**Win32 \_ ProcessStopTrace.**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace) Weitere Informationen zu Problembehandlungsanbietern finden Sie unter [Debuggen von Anbietern und](debugging-providers.md) [Anbieterkonfiguration und Problembehandlungsklassen.](provider-configuration-and-troubleshooting-classes.md)
-   Wenn der Anbieter ein Instanz- oder Methodenanbieter ist, stellen Sie sicher, dass Sie jede Anbieterfunktion nacheinander testen, um Verwirrung bei der Einhaltung Ihrer Codelogik zu vermeiden.
-   Erstellen Sie für einen Instanzanbieter eine Clientanwendung oder ein Skript, die jede Schnittstelle des Anbieters aufruft (Enumeration, Get, Put und Delete). Auch wenn der Anbieter nichts implementieren soll, sollte er die Meldung "Nicht unterstützt" zurückgeben. Sie finden die Rückgabewerte, die bereits in [WMI-Rückgabecodes definiert sind.](wmi-return-codes.md)
-   Um sicherzustellen, dass der gewünschte Sicherheitskontext wie geplant funktioniert, rufen Sie die vom Anbieter unterstützten Vorgänge aus einem Nichtadministrator-Sicherheitskontext auf. Der Anbieter muss Identitätswechsel unterstützen. Wenn ein Benutzer, der die richtigen Sicherheitsanmeldeinformationen nicht hat, versucht, Daten zu aktualisieren oder einen Vorgang auszuführen, bei dem eine Methode ausgeführt wird, sollte Ihr Anbieter den Zugriff mit der entsprechenden Fehlermeldung verweigern.
-   Weitere Informationen zur Anbietersicherheit finden Sie unter [Securing Your Provider](securing-your-provider.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwickeln eines WMI-Anbieters](developing-a-wmi-provider.md)
</dt> <dt>

[Anbieterhosting und -sicherheit](provider-hosting-and-security.md)
</dt> <dt>

[Bereitstellung von Daten für WMI durch Schreiben eines Anbieters](supplying-data-to-wmi-by-writing-a-provider.md)
</dt> <dt>

[Integrieren eines Anbieters in eine Anwendung](incorporating-a-provider-in-an-application.md)
</dt> <dt>

[Registrieren eines Anbieters](registering-a-provider.md)
</dt> <dt>

[Problembehandlung bei WMI-Clientanwendungen](troubleshooting-wmi-client-applications.md)
</dt> <dt>

[Schützen Ihres Anbieters](securing-your-provider.md)
</dt> <dt>

[Abrufen und Bereitstellen von Daten auf einer 64-Bit-Plattform](getting-and-providing-data-on-a-64-bit-computer.md)
</dt> </dl>

 

 
