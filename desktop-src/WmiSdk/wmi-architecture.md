---
description: WMI bietet eine einheitliche Schnittstelle für alle lokalen oder Remoteanwendungen oder Skripts, die Verwaltungsdaten von einem Computersystem, einem Netzwerk oder einem Unternehmen abrufen.
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
ms.openlocfilehash: e261459785fa4e0ccdce7337df788de007c6f335799bbe4778e80f551f5e519e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995524"
---
# <a name="wmi-architecture"></a>WMI-Architektur

WMI bietet eine einheitliche Schnittstelle für alle lokalen oder Remoteanwendungen oder Skripts, die Verwaltungsdaten von einem Computersystem, einem Netzwerk oder einem Unternehmen abrufen. Die einheitliche Schnittstelle ist so konzipiert, dass WMI-Clientanwendungen und -Skripts keine Vielzahl von ApIs (Application Programming Interfaces) des Betriebssystems aufrufen müssen. Viele APIs können nicht von Automatisierungsclients wie Skripts oder Visual Basic aufgerufen werden. Andere APIs rufen keine Remotecomputer auf.

Um Daten aus WMI zu erhalten, schreiben Sie ein Clientskript oder eine Anwendung, das auf [WMI-Klassen zutritt,](wmi-classes.md) oder stellen Sie Daten für WMI zur Verfügung, indem Sie einen [*WMI-Anbieter schreiben.*](gloss-p.md) Weitere Informationen finden Sie unter [Verwenden von WMI.](using-wmi.md)

## <a name="objects-consumers-and-infrastructure-of-wmi"></a>Objekte, Consumers und Infrastruktur von WMI

Das folgende Diagramm zeigt die Beziehung zwischen der WMI-Infrastruktur und den WMI-Anbietern und verwalteten Objekten sowie die Beziehung zwischen der WMI-Infrastruktur und den WMI-Consumers.

![Beziehung zwischen wmi-Infrastruktur, WMI-Anbietern und verwalteten Objekten](images/wmi-architecture.png)

## <a name="wmi-components"></a>WMI-Komponenten

In der folgenden Liste werden die wichtigsten WMI-Komponenten beschrieben:

-   Verwaltete Objekte und WMI-Anbieter

    Ein WMI-Anbieter ist ein COM-Objekt, das ein oder mehrere [*verwaltete Objekte für*](gloss-m.md) WMI überwacht. Ein verwaltetes Objekt ist eine logische oder physische Unternehmenskomponente, z. B. eine Festplatte, ein Netzwerkadapter, ein Datenbanksystem, ein Betriebssystem, ein Prozess oder ein Dienst.

    Ähnlich wie bei einem Treiber stellt ein Anbieter WMI Daten aus einem verwalteten Objekt zur Hand und verarbeitet Nachrichten von WMI an das verwaltete Objekt. WMI-Anbieter bestehen aus einer DLL-Datei und einer [*MOF-Datei (Managed Object Format),*](gloss-m.md) die die Klassen definiert, für die der Anbieter Daten zurückgibt und Vorgänge ausführt. Anbieter wie WMI-C++-Anwendungen verwenden die [COM-API für WMI.](com-api-for-wmi.md) Weitere Informationen finden Sie unter [Bereitstellen von Daten für WMI.](providing-data-to-wmi.md)

    Ein Beispiel für einen Anbieter ist der vorinstallierte [Registrierungsanbieter,](/previous-versions/windows/desktop/regprov/system-registry-provider)der auf Daten in der Systemregistrierung zugreift. Der Registrierungsanbieter verfügt über eine [*WMI-Klasse*](gloss-w.md), [**StdRegProv,**](/previous-versions/windows/desktop/regprov/stdregprov)mit vielen Methoden, aber ohne Eigenschaften. Andere vorinstallierte Anbieter, z. B. der [Win32-Anbieter,](/windows/desktop/CIMWin32Prov/win32-provider)verfügen in der Regel über Klassen mit vielen Eigenschaften, aber wenigen Methoden, z. B. [**Win32 \_ Process**](/windows/desktop/CIMWin32Prov/win32-process) oder [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk). Die DLL-Datei des Registrierungsanbieters, Stdprov.dll, enthält den Code, der Daten dynamisch zurückgibt, wenn dies von Clientskripts oder -anwendungen angefordert wird.

    WMI-MOF- und DLL-Dateien befinden sich in %WINDIR% \\ System32 Wbem, zusammen mit \\ [den WMI Command-Line Tools,](wmi-command-line-tools.md) [](winmgmt.md) z. B.Winmgmt.exe [**undMofcomp.exe**](mofcomp.md). Anbieterklassen wie [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)werden in MOF-Dateien definiert und dann beim Systemstart in das WMI-Repository kompiliert.

-   [WMI-Infrastruktur](wmi-infrastructure.md)

    Die WMI-Infrastruktur ist eine Microsoft Windows Betriebssystemkomponente, die als WMI-Dienst (winmgmt) bekannt ist. Die WMI-Infrastruktur verfügt über zwei Komponenten: WMI Core und [*WMI-Repository.*](gloss-w.md)

    Das WMI-Repository ist nach [*WMI-Namespaces organisiert.*](gloss-n.md) Der WMI-Dienst erstellt beim Systemstart einige Namespaces, z. B. Root Default, root cimv2 und root subscription, und installiert einen Standardsatz von Klassendefinitionen, einschließlich \\ \\ der \\ [Win32-Klassen,](/windows/desktop/CIMWin32Prov/win32-provider)der [WMI-Systemklassen](wmi-system-classes.md)und anderer. Die verbleibenden Namespaces auf Ihrem System werden von Anbietern für andere Teile des Betriebssystems oder der Produkte erstellt. Weitere Informationen und eine Liste der WMI-Anbieter in den meisten Betriebssystemversionen finden Sie unter [WMI-Anbieter](wmi-providers.md).

    Der WMI-Dienst fungiert als Vermittler zwischen den Anbietern, Verwaltungsanwendungen und dem WMI-Repository. Nur statische Daten zu Objekten werden im Repository gespeichert, z. B. die von Anbietern definierten Klassen. WMI erhält die meisten Daten dynamisch vom Anbieter, wenn ein Client sie an fordert. Sie können auch Abonnements für den Empfang von Ereignisbenachrichtigungen von einem Anbieter einrichten. Weitere Informationen finden Sie unter [Überwachen von Ereignissen.](monitoring-events.md)

-   WMI-Consumers

    Ein WMI-Consumer ist eine Verwaltungsanwendung oder ein Skript, die mit der WMI-Infrastruktur interagiert. Eine Verwaltungsanwendung kann Daten abfragen, aufzählen, Anbietermethoden ausführen oder Ereignisse abonnieren, indem sie entweder die [COM-API](com-api-for-wmi.md) für WMI oder die [Skript-API für WMI aufruft.](scripting-api-for-wmi.md) Die einzigen Daten oder Aktionen, die für ein verwaltetes Objekt verfügbar sind, z. B. ein Datenträgerlaufwerk oder ein Dienst, sind diejenigen, die ein Anbieter zur Verfügung stellt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von WMI](using-wmi.md)
</dt> <dt>

[WMI-Anbieter](wmi-providers.md)
</dt> <dt>

[Erstellen einer WMI-Anwendung oder eines Skripts](creating-a-wmi-application-or-script.md)
</dt> <dt>

[WMI-Aufgaben für Skripts und Anwendungen](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[Bereitstellen von Daten für WMI](providing-data-to-wmi.md)
</dt> <dt>

[WMI-Klassen](wmi-classes.md)
</dt> <dt>

[Überwachen von Ereignissen](monitoring-events.md)
</dt> <dt>

[Aufrufen einer Methode](calling-a-method.md)
</dt> </dl>

 

 
