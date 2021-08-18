---
title: Programmiersprachenunterstützung
description: Sie können ADSI-Clientanwendungen in vielen Sprachen schreiben.
ms.assetid: 47460d57-936d-4c5f-8ff6-a4d9d60d0b68
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ebe355e3274821bf81a666380bfe70ca0f3f7b49e2bc9de10bf2aa4796b5288
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023302"
---
# <a name="programming-language-support"></a>Programmiersprachenunterstützung

Sie können ADSI-Clientanwendungen in vielen Sprachen schreiben. Für die meisten administrativen Aufgaben definiert ADSI Schnittstellen und Objekte, auf die über mit Automation kompatible Sprachen zugegriffen werden kann. Beispielsweise das Microsoft Visual Basic-Entwicklungssystem, Microsoft Visual Basic Scripting Edition (VBScript) und Java sowie leistungs- und effizienzbewusstere Sprachen wie C und C++.

Die nahtlose Integration mit Active Server Pages und VBScript erleichtert das Schreiben von Internetanwendungen, die auf Verzeichnisdienste zugreifen. Für die Integration in OLE DB Anwendungen stellt ADSI einen OLE DB-Anbieter bereit, indem eine Teilmenge der OLE DB Abfrageschnittstellen unterstützt wird. Der OLE DB-Anbieter unterstützt den schreibgeschützten Zugriff auf Active Directory.

Bei Internetanwendungen kann die Verwendung von Skripts in ASP-Dateien (Active Server Page) ADSI-Objekte auf dem Server erstellen und bearbeiten und die Ergebnisse auf einer Webseite anzeigen. In Microsoft Management Console können Snap-Ins für die Verzeichnisdienstverwaltung ADSI verwenden, um die für Sie interessanten Verzeichnisdienste zu finden. Kurz gesagt: Active Directory-Dienstschnittstellen können Zugriff auf eine breite und vielfältige Gruppe von Verzeichnisdiensten bieten– einschließlich derjenigen, die noch nicht erstellt wurden.

Für den Zugriff auf Strukturen, die herkömmliche APIs verwenden, definiert die ADSI-Architektur Low-Level-Schnittstellen, die keine Automatisierung unterstützen, auf die über Sprachen wie C und C++ zugegriffen werden kann. Diese Schnittstellen sind wenig mehr als COM-Wrapper für Netzwerkprotokolle zu einem Verzeichnisdienst.

Durch das Schreiben von Code in die veröffentlichten Schnittstellen kann Ihre Anwendung Verzeichnisdienste für alle installierten ADSI-Anbieter erreichen und die resultierenden Daten integrieren. Mit wenigen oder gar keinen Änderungen am Code kann Ihre Anwendung weiterhin auf zusätzliche Verzeichnisdienste in Ihrem Netzwerk zugreifen, wenn neue ADSI-Anbieter installiert werden.

Die folgende Abbildung zeigt, wie ADSI in eine Anwendungsumgebung passt. Unabhängig davon, ob die Anwendung in Visual Basic, C/C++, VBScript, Microsoft JScript Entwicklungssystem oder als Webanwendung mit Active Server Pages geschrieben ist, bieten Active Directory-Dienstschnittstellen einen sauberen und benutzerfreundlichen Zugriff auf die zugrunde liegenden Verzeichnisdienste, ohne die nativen Netzwerk-APIs verwenden zu müssen.

![Adsi-Unterstützung für Programmiersprachen](images/ds2layr.png)

Wie in der obigen Abbildung dargestellt, haben Clients, die Automation nicht unterstützen, Zugriff auf alle ADSI-Schnittstellen, einschließlich reiner COM-Schnittstellen mit der Namenskonvention **IDirectoryXXX** und Automation COM-Schnittstellen mit der Benennungskonvention **IADsXXX**. Da Clients hauptsächlich Informationen von Verzeichnisdiensten anfordern, ist das flexible ADSI-Abfragemodell über OLE DB und [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) effektiv.

 

 




