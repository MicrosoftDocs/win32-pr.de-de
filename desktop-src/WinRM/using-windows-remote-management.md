---
title: Verwenden von Windows-Remoteverwaltung
description: Windows-Remoteverwaltung ist für die Verbesserung der Hardware Verwaltung in einer Netzwerkumgebung mit verschiedenen Geräten vorgesehen, auf denen eine Vielzahl von Betriebssystemen ausgeführt wird.
ms.assetid: 6ee2b238-5bc2-4274-b7ca-49dbc728d8f1
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0c2934694de5913b467521510179fffdb220b601
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101999"
---
# <a name="using-windows-remote-management"></a>Verwenden von Windows-Remoteverwaltung

Windows-Remoteverwaltung ist für die Verbesserung der Hardware Verwaltung in einer Netzwerkumgebung mit verschiedenen Geräten vorgesehen, auf denen eine Vielzahl von Betriebssystemen ausgeführt wird. Das gesamte Design des Diensts ist auf die Überwachung und Verwaltung von Remotecomputern ausgerichtet. Zu diesem Zweck wird ein interoperables Standardprotokoll implementiert.

Da die [WinRM-Skript-API](winrm-scripting-api.md) und die [WinRM-C++-API](winrm-c---api.md) die für das WS-Management-Protokoll definierten Vorgänge implementieren und genau modellieren, empfangen Skripts und Anwendungen XML-Datenströme als Antwort auf Anforderungen. Eingabeparameter für Methodenaufrufe müssen in XML erstellt werden. Sie können die Methoden der [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) -API verwenden, um XML-Zeichen folgen anzuzeigen oder zu konstruieren. Ein Beispiel finden Sie unter [Anzeigen der XML-Ausgabe von WinRM-Skripts](displaying-xml-output-from-winrm-scripts.md).

Die folgende Liste enthält Themen, in denen die Verwendung der WinRM-Skripterstellung beschrieben wird:

-   [Erkennen, ob ein Remote Computer WS-Management Protokoll unterstützt](detecting-whether-a-remote-computer-supports-ws-management-protocol.md)
-   [Abrufen von Daten vom lokalen Computer](obtaining-data-from-the-local-computer.md)
-   [Abrufen von Daten von einem Remote Computer](obtaining-data-from-a-remote-computer.md)
-   [Auflisten oder Auflisten aller Instanzen einer Ressource](enumerating-or-listing-all-instances-of-a-resource.md)
-   [Abfragen für bestimmte Instanzen einer Ressource](querying-for-specific-instances-of-a-resource.md)
-   [Anzeigen der XML-Ausgabe von WinRM-Skripts](displaying-xml-output-from-winrm-scripts.md)

## <a name="tracing-winrm-activity"></a>Ablauf Verfolgung für WinRM-Aktivität

Da WinRM Daten über [Windows-Verwaltungsinstrumentation (WMI)](/windows/desktop/WmiSdk/wmi-start-page)abruft, können Sie die WMI-Aktivität nachverfolgen, die sich aus WinRM-Meldungen ergibt. Ab Windows Vista verwendet der WMI-Dienst nicht mehr die [WMI-Protokolldateien](/windows/desktop/WmiSdk/wmi-log-files). Stattdessen werden [Ereignis Ablauf Verfolgung](/windows/desktop/ETW/event-tracing-portal) (ETW) verwendet, und Ereignisse sind über die **Ereignisanzeige** -Benutzeroberfläche oder das Befehlszeilen Tool evtutil verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Remoteverwaltung](portal.md)
</dt> <dt>

[Informationen zu Windows-Remoteverwaltung](about-windows-remote-management.md)
</dt> <dt>

[Windows-Remoteverwaltung Referenz](windows-remote-management-reference.md)
</dt> <dt>

[Skripterstellung in Windows-Remoteverwaltung](scripting-in-windows-remote-management.md)
</dt> </dl>

 

 