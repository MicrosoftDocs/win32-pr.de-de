---
description: Ein-Anbieter ist ein COM-Objekt (Component Object Model), das als Vermittler zwischen WMI und einem verwalteten Objekt fungiert.
ms.assetid: a4f537ba-9081-43b4-acff-4d206de3d9d7
ms.tgt_platform: multiple
title: Entwickeln eines WMI-Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9249c251f75f08f9e5142e70a507b0dced8f91df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368240"
---
# <a name="developing-a-wmi-provider"></a>Entwickeln eines WMI-Anbieters

Ein-Anbieter ist ein COM-Objekt (Component Object Model), das als Vermittler zwischen WMI und einem verwalteten Objekt fungiert. Wenn beispielsweise eine Anwendung oder ein Skript Datenträger Daten mithilfe der WMI [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse anfordert, werden die Daten dynamisch über den vorinstallierten [Win32-Anbieter](/windows/desktop/CIMWin32Prov/win32-provider)abgerufen.

Wenn Sie Daten über WMI für andere Anwendungen bereitstellen möchten, können Sie einen nicht verwalteten Code Anbieter erstellen, indem Sie einen com-Server oder die **WMI-ATL-Assistenten** in Visual Studio schreiben. Sie können einen Anbieter für verwalteten Code mithilfe von WMI in der .NET Framework schreiben. In den Themen in diesem Abschnitt wird beschrieben, wie ein nicht verwalteter com-Anbieter geschrieben wird.

> [!Note]  
> Um sicherzustellen, dass alle ihre WMI-Klassendefinitionen für verwaltete Objekte im [*WMI-Repository*](gloss-w.md) wieder hergestellt werden, wenn WMI einen Fehler aufweist und neu gestartet wird, verwenden Sie die " [**\# pragma Auto Wiederherstellen**](pragma-autorecover.md) "-Präprozessoranweisung in der MOF-Datei (Managed Object Format).

 

Ein Anbieter besteht aus Klassen, die im [*MOF-Schema (Managed Object Format)*](gloss-m.md) und einer DLL-Datei definiert sind, die die Funktionen des Anbieters ausführt. Beispielsweise ist die MOF-Datei, die die Klassen des Win32-Anbieters definiert, cimwin32. MOF, und die dll wird CIMWin32.dll. beide befinden sich in% windir% \\ system32 \\ WBEM.

Das MOF-Schema für den Anbieter kann mehrere Anbieter Typen enthalten. Der [Ereignisprotokoll Anbieter](/previous-versions/windows/desktop/eventlogprov/event-log-provider) enthält z. b. in einer MOF-Datei mit dem Namen "ntevt. mof" Instanzen-, Methoden-und Ereignis Anbieter Typen. Es wird empfohlen, alle Klassen und das Registrierungs Schema für Verwandte Anbieter in einer Datei zusammenzustellen, anstatt eine Datei pro Klasse zu erstellen.

Zusätzlich zur Verwendung von vorinstallierten Anbietern können Sie auch einen eigenen Anbieter erstellen, um Informationen über ein Hardware Gerät oder den Betrieb der Software bereitzustellen.

In der folgenden Tabelle sind die grundlegenden Aufgaben aufgeführt, mit denen ein Anbieter erstellt wird.



| Aufgabe                                                                                                                                                            | BESCHREIBUNG                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Entwerfen von Managed Object Format-Klassen (MOF)](designing-managed-object-format--mof--classes.md)                                                              | Entwickeln Sie ein Modell für die Entitäten, die Sie über WMI verwalten möchten, und erstellen Sie eine Managed Object Format Datei (MOF), um das Schema zu beschreiben.<br/> |
| [Bereitstellen von Daten für WMI durch Schreiben eines Anbieters](supplying-data-to-wmi-by-writing-a-provider.md)                                                                  | Erstellen Sie den grundlegendsten Anbieter, der mit WMI gekoppelt ist.<br/>                                                                                |
| [Einbinden eines Anbieters in eine Anwendung](incorporating-a-provider-in-an-application.md)                                                                    | Fügen Sie den Anbieter als Komponente in eine Anwendung ein, wenn er nicht immer ausgeführt wird.<br/>                                         |
| [Registrieren eines Anbieters](registering-a-provider.md)                                                                                                            | Registrieren Sie den Anbieter bei com und WMI.<br/>                                                                                               |
| [Initialisieren eines Anbieters](initializing-a-provider.md)                                                                                                          | Implementieren Sie die Schnittstellen [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) und [**iwbemproviderinitsink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinitsink) .<br/>   |
| [Aufrufen von WMI](making-calls-to-wmi.md)                                                                                                                  | Ruft WMI-Schnittstellen von einem Anbieter auf.<br/>                                                                                                  |
| [Annehmen der Identität eines Clients](impersonating-a-client.md)                                                                                                            | Legen Sie Sicherheit für den Zugriff auf eine Client Anwendung fest.<br/>                                                                                          |
| [Aktualisieren eines Anbieters](updating-a-provider.md)                                                                                                                  | Verbessern Sie den Anbieter nach Bedarf.<br/>                                                                                                       |
| [Entladen eines Anbieters](unloading-a-provider.md)                                                                                                                | Entfernen Sie den Anbieter beim Herunterfahren oder bei Leerlauf des Anbieters aus dem Arbeitsspeicher.<br/>                                                         |
| [Debuggen von Anbietern](debugging-providers.md) und [Anbieter Konfiguration und Problem Behandlungs Klassen](provider-configuration-and-troubleshooting-classes.md) | Debuggen Sie Ihren Anbieter mithilfe der von WMI bereitgestellten Funktionen.<br/>                                                                                 |
| [Erhalten und Bereitstellen von Daten auf einem 64-Bit-Computer](getting-and-providing-data-on-a-64-bit-computer.md)                                                          | Evaluieren Sie, ob Sie einen 32-Bit-Anwendungskompatibilitäts-Anbieter benötigen oder ob der 64-Bit-Anbieter Daten für beide Clients bereitstellen kann.<br/>      |



 

In den folgenden Themen werden die Schritte erläutert, die zum Schreiben verschiedener Anbieter Typen erforderlich sind:

-   [Schreiben eines Instanzanbieters](writing-an-instance-provider.md)
-   [Schreiben eines Methoden Anbieters](writing-a-method-provider.md)
-   [Schreiben eines Ereignis Anbieters](writing-an-event-provider.md)
-   [Schreiben eines Ereignisconsumeranbieters](writing-an-event-consumer-provider.md)
-   [Schreiben eines Klassen Anbieters](writing-a-class-provider.md)
-   [Schreiben eines Eigenschaften Anbieters](writing-a-property-provider.md)
-   [Erstellen eines Instanzanbieters in einen High-Performance-Anbieter](making-an-instance-provider-into-a-high-performance-provider.md)

 

