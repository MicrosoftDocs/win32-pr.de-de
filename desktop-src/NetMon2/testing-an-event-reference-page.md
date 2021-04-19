---
description: Der letzte Schritt beim Erstellen einer Ereignis Referenzseite (ERP) ist das Testen.
ms.assetid: 12690317-1cd2-496c-8a0d-ba6caca58b86
title: Testen einer Ereignis Referenzseite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6afaaec279403922abde578b9e73931e607680f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346975"
---
# <a name="testing-an-event-reference-page"></a>Testen einer Ereignis Referenzseite

Der letzte Schritt beim Erstellen einer Ereignis Referenzseite (ERP) ist das Testen. Sie können ein ERP testen, indem Sie die Datei in einem HTML-Browser wie z. b. Microsoft Internet Explorer anzeigen. Oder Sie können das ERP und seine Experten-dll installieren, um es für den Ereignis Aufruf zu testen und in der Netzwerkmonitor Ereignisanzeige anzuzeigen.

## <a name="viewing-erps-that-have-no-dll"></a>Anzeigen von Erps ohne dll

Öffnen Sie die Datei mit einem HTML-Viewer, der Ihre eingebetteten Quellen unterstützt, um das abgeschlossene ERP ohne eine installierte Experte-dll anzuzeigen. Die folgende Abbildung zeigt die ERP-Beispieldatei, die in [Schreiben eines ERP](writing-an-event-reference-page.md) -Dokuments beschrieben wird, wie es mit Microsoft Internet Explorer Version 4,01 angezeigt wird.

![Beispiel-ERP-Datei](images/ie-erp.png)

Testen von Erps mit einer dll

Nachdem die ERP-Dateien und die [**Experten-**](experts.md) dll erstellt wurden, können Sie die gesamte Funktionalität Ihrer Erps mit Netzwerkmonitor testen. Es wird davon ausgegangen, dass die dll debuggten ist und gültige Ereignisse generieren kann.

**So testen Sie Erps, die eine DLL haben**

1.  Vergewissern Sie sich, dass die richtige Experten-dll im entsprechenden Verzeichnis installiert ist. Weitere Informationen finden Sie unter [Installieren eines Experten in Netzwerkmonitor 2,1](installing-an-expert-to-network-monitor-2-1.md).
2.  Überprüfen Sie den [richtigen Namen](naming-an-event-reference-page.md) der ERP-Datei.
3.  Überprüfen Sie den [richtigen Speicherort](installing-existing-erps-to-network-monitor-2-1.md) der Erps im Netzwerkmonitor Verzeichnis.
4.  Testen von Experten Erps in der Netzwerkmonitor-Benutzeroberfläche.
5.  Generieren Sie ein Test Ereignis.
6.  Überprüfen Sie, ob das ERP in der Netzwerkmonitor Ereignisanzeige angezeigt wird.

Weitere Informationen zum Erstellen eines ERP finden Sie unter:

-   [Erstellen von Referenzseiten für Experten und Überwachungs Ereignisse](creating-expert-and-monitor-event-reference-pages.md)
-   [Schreiben einer Ereignis Referenzseite](writing-an-event-reference-page.md)
-   [Benennen einer Ereignis Referenzseite](naming-an-event-reference-page.md)

 

 



