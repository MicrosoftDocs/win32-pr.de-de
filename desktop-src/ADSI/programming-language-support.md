---
title: Unterstützung für Programmiersprachen
description: Sie können in vielen Sprachen ADSI-Client Anwendungen schreiben.
ms.assetid: 47460d57-936d-4c5f-8ff6-a4d9d60d0b68
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4946f05806a6e24ff466d08dc141aadf9c995e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855264"
---
# <a name="programming-language-support"></a>Unterstützung für Programmiersprachen

Sie können in vielen Sprachen ADSI-Client Anwendungen schreiben. Bei den meisten administrativen Aufgaben definiert ADSI Schnittstellen und Objekte, auf die von mit Automation kompatiblen Sprachen zugegriffen werden kann. Beispielsweise das Microsoft Visual Basic Development System, Microsoft Visual Basic Scripting Edition (VBScript) und Java sowie weitere Leistungs-und Effizienz bewusste Sprachen wie C und C++.

Die reibungslose Integration mit Active Server Seiten und VBScript erleichtert das Schreiben von Internet Anwendungen, die auf Verzeichnisdienste zugreifen. Für die Integration mit OLE DB-Anwendungen stellt ADSI einen OLE DB Anbieter bereit, indem er eine Teilmenge der OLE DB Abfrageschnittstellen unterstützt. Der OLE DB-Anbieter unterstützt den schreibgeschützten Zugriff auf Active Directory.

Bei Internet Anwendungen kann das Verwenden von Skripts in Active Server Page-Dateien (ASP) zum Erstellen und Bearbeiten von ADSI-Objekten auf dem Server und zum Anzeigen der Ergebnisse auf einer Webseite verwendet werden. In der Microsoft Management Console können Snap-Ins für die Verzeichnisdienst Verwaltung ADSI verwenden, um die gewünschten Verzeichnisdienste zu finden. Kurz gesagt können Active Directory Dienst Schnittstellen den Zugriff auf eine Breite und vielfältige Gruppe von Verzeichnisdiensten ermöglichen – einschließlich derjenigen, die noch nicht erstellt wurden.

Für den Zugriff auf Strukturen mit herkömmlichen APIs definiert die ADSI-Architektur Low-Level-Schnittstellen, die keine Automatisierung unterstützen, auf die von Sprachen wie C und C++ aus zugegriffen werden kann. Diese Schnittstellen sind wenig mehr als COM-Wrapper für Netzwerkprotokolle für einen Verzeichnisdienst.

Das Schreiben von Code in die veröffentlichten Schnittstellen ermöglicht es Ihrer Anwendung, Verzeichnisdienste für alle installierten ADSI-Anbieter zu erreichen und die resultierenden Daten zu integrieren. Wenn Sie nur wenige oder gar keine Änderungen an Ihrem Code vorgenommen haben, kann Ihre Anwendung weiterhin auf zusätzliche Verzeichnisdienste in Ihrem Netzwerk zugreifen, wenn neue ADSI-Anbieter installiert werden.

In der folgenden Abbildung wird gezeigt, wie ADSI in eine Anwendungsumgebung passt. Unabhängig davon, ob die Anwendung in Visual Basic, C/C++, VBScript, Microsoft JScript Development System oder als Webanwendung mithilfe von Active Server Seiten geschrieben ist, bieten Active Directory Dienst Schnittstellen einen sauberen und leicht zu verwendenden Zugriff auf die zugrunde liegenden Verzeichnisdienste, ohne die nativen Netzwerk-APIs verwenden zu müssen.

![ADSI-Unterstützung für Programmiersprachen](images/ds2layr.png)

Wie in der obigen Abbildung gezeigt, haben Clients, die keine Automatisierung unterstützen, Zugriff auf alle ADSI-Schnittstellen, einschließlich der reinen com-Schnittstellen mit der Benennungs Konvention **idirectoryxxx** und der Automatisierungs-com-Schnittstelle mit der Benennungs Konvention **iadsxxx**. Da von Clients überwiegend Informationen von Verzeichnisdiensten angefordert werden, ist das flexible ADSI-Abfrage Modell durch OLE DB und [**idirector ysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) effektiv.

 

 




