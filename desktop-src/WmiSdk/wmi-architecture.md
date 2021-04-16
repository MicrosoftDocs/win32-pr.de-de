---
description: WMI bietet eine einheitliche Schnittstelle für lokale oder Remote Anwendungen oder Skripts, die Verwaltungsdaten von einem Computersystem, einem Netzwerk oder einem Unternehmen erhalten.
ms.assetid: 41ba2a64-3322-48b8-a6ea-e468bfac06e2
ms.tgt_platform: multiple
title: WMI-Architektur
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b90ee4f81c2afdfc222dd7d5d824f88bda122b73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104563799"
---
# <a name="wmi-architecture"></a>WMI-Architektur

WMI bietet eine einheitliche Schnittstelle für lokale oder Remote Anwendungen oder Skripts, die Verwaltungsdaten von einem Computersystem, einem Netzwerk oder einem Unternehmen erhalten. Die einheitliche Schnittstelle ist so konzipiert, dass WMI-Client Anwendungen und-Skripts keine Vielzahl von Betriebssystem-Anwendungs Programmierschnittstellen (APIs) aufzurufen müssen. Viele APIs können nicht von Automatisierungs Clients wie Skripts oder Visual Basic Anwendungen aufgerufen werden. Von anderen APIs werden keine Aufrufe an Remote Computer durchführen.

Zum Abrufen von Daten aus WMI schreiben Sie ein Client Skript oder eine Anwendung, die auf [WMI-Klassen](wmi-classes.md) zugreift oder WMI-Daten bereitstellt, indem Sie einen [*WMI-Anbieter*](gloss-p.md)schreiben. Weitere Informationen finden Sie unter [Verwenden von WMI](using-wmi.md).

## <a name="objects-consumers-and-infrastructure-of-wmi"></a>Objekte, Consumer und Infrastruktur von WMI

Das folgende Diagramm zeigt die Beziehung zwischen der WMI-Infrastruktur und den WMI-Anbietern und den verwalteten Objekten und zeigt außerdem die Beziehung zwischen der WMI-Infrastruktur und den WMI-Consumern.

![Beziehung zwischen WMI-Infrastruktur, WMI-Anbietern und verwalteten Objekten](images/wmi-architecture.png)

## <a name="wmi-components"></a>WMI-Komponenten

In der folgenden Liste werden die wichtigsten WMI-Komponenten beschrieben:

-   Verwaltete Objekte und WMI-Anbieter

    Ein WMI-Anbieter ist ein COM-Objekt, das ein oder mehrere [*verwaltete Objekte*](gloss-m.md) für WMI überwacht. Ein verwaltetes Objekt ist eine logische oder physische Unternehmens Komponente, z. b. ein Festplattenlaufwerk, ein Netzwerkadapter, ein Datenbanksystem, ein Betriebssystem, ein Prozess oder ein Dienst.

    Ähnlich wie bei einem Treiber stellt ein Anbieter WMI mit Daten aus einem verwalteten Objekt bereit und verarbeitet die Nachrichten von WMI an das verwaltete Objekt. WMI-Anbieter bestehen aus einer DLL-Datei und einer [*Managed Object Format (MOF)*](gloss-m.md) -Datei, die die Klassen definiert, für die der Anbieter Daten zurückgibt und Vorgänge ausführt. Anbieter, wie z. b. WMI C++-Anwendungen, verwenden die [com-API für WMI](com-api-for-wmi.md). Weitere Informationen finden Sie unter [Bereitstellen von Daten für WMI](providing-data-to-wmi.md).

    Ein Beispiel für einen-Anbieter ist der vorinstallierte [Registrierungs Anbieter](/previous-versions/windows/desktop/regprov/system-registry-provider), der auf Daten in der Systemregistrierung zugreift. Der Registrierungs Anbieter verfügt über eine [*WMI-Klasse*](gloss-w.md), [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), mit vielen Methoden, aber ohne Eigenschaften. Andere vorinstallierte Anbieter, z. b. der [Win32-Anbieter](/windows/desktop/CIMWin32Prov/win32-provider), verfügen normalerweise über Klassen mit vielen Eigenschaften, aber nur wenige Methoden, z. b. [**Win32- \_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process) oder [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk). Die DLL-Datei des Registrierungs Anbieters (Stdprov.dll) enthält den Code, der Daten dynamisch zurückgibt, wenn Sie von Client Skripts oder Anwendungen angefordert werden.

    Die WMI-MOF-und dll-Dateien befinden sich in% windir% \\ system32 \\ WBEM, zusammen mit den [WMI-Command-Line Tools](wmi-command-line-tools.md)wie [**Winmgmt.exe**](winmgmt.md) und [**Mofcomp.exe**](mofcomp.md). Anbieter Klassen, wie z. b. [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), werden in MOF-Dateien definiert und beim Systemstart in das WMI-Repository kompiliert.

-   [WMI-Infrastruktur](wmi-infrastructure.md)

    Die WMI-Infrastruktur ist eine Komponente des Microsoft Windows-Betriebssystems, die als WMI-Dienst (Winmgmt) bekannt ist. Die WMI-Infrastruktur verfügt über zwei Komponenten: den WMI-Kern und das [*WMI-Repository*](gloss-w.md).

    Das WMI-Repository ist nach WMI- [*Namespaces*](gloss-n.md)organisiert. Der WMI-Dienst erstellt beim Systemstart einige Namespaces, z. b. root \\ Default, root \\ CIMV2 und root- \\ Abonnement und führt eine Vorinstallation eines Standardsatzes von Klassendefinitionen durch, einschließlich der [Win32-Klassen](/windows/desktop/CIMWin32Prov/win32-provider), der [WMI-System Klassen](wmi-system-classes.md)und anderer. Die verbleibenden Namespaces, die auf Ihrem System gefunden werden, werden von Anbietern für andere Teile des Betriebssystems oder der Produkte erstellt. Weitere Informationen und eine Liste der WMI-Anbieter, die in den meisten Betriebssystemversionen gefunden werden, finden Sie unter [WMI-Anbieter](wmi-providers.md).

    Der WMI-Dienst fungiert als Vermittler zwischen den Anbietern, den Verwaltungs Anwendungen und dem WMI-Repository. Nur statische Daten über Objekte werden im Repository gespeichert, z. b. die von Anbietern definierten Klassen. Die meisten Daten werden von WMI dynamisch vom Anbieter abgerufen, wenn Sie von einem Client angefordert werden. Sie können auch Abonnements einrichten, um Ereignis Benachrichtigungen von einem Anbieter zu empfangen. Weitere Informationen finden Sie unter über [Wachen von Ereignissen](monitoring-events.md).

-   WMI-Consumer

    Ein WMI-Consumer ist eine Verwaltungs Anwendung oder ein Skript, das mit der WMI-Infrastruktur interagiert. Eine Verwaltungs Anwendung kann Daten Abfragen, aufzählen, Anbieter Methoden ausführen oder Ereignisse abonnieren, indem Sie entweder die [com-API für WMI](com-api-for-wmi.md) oder die [Skript-API für WMI](scripting-api-for-wmi.md)aufrufen. Die einzigen Daten oder Aktionen, die für ein verwaltetes Objekt, z. b. ein Laufwerk oder einen Dienst, verfügbar sind, sind die von einem Anbieter bereitgestellten Daten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von WMI](using-wmi.md)
</dt> <dt>

[WMI-Anbieter](wmi-providers.md)
</dt> <dt>

[Erstellen einer WMI-Anwendung oder eines Skripts](creating-a-wmi-application-or-script.md)
</dt> <dt>

[WMI-Tasks für Skripts und Anwendungen](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[Bereitstellen von Daten für WMI](providing-data-to-wmi.md)
</dt> <dt>

[WMI-Klassen](wmi-classes.md)
</dt> <dt>

[Überwachen von Ereignissen](monitoring-events.md)
</dt> <dt>

[Aufrufen einer Methode](calling-a-method.md)
</dt> </dl>

 

 
