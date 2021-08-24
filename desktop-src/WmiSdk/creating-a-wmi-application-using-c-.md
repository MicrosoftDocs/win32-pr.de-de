---
description: Um eine Anwendung für WMI mit C++ zu erstellen, müssen Sie COM initialisieren, auf WMI-Protokolle zugreifen und diese festlegen und eine manuelle Bereinigung durchführen.
ms.assetid: 0b9b7990-6982-4ba9-8dba-7470990405f7
ms.tgt_platform: multiple
title: Erstellen einer WMI-Anwendung mit C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fc68bfb9b7c17967de3142c3e431b51fc340a32acfb94484030e8fe744bf067
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612400"
---
# <a name="creating-a-wmi-application-using-c"></a>Erstellen einer WMI-Anwendung mit C++

Um eine Anwendung für WMI mit C++ zu erstellen, müssen Sie COM initialisieren, auf WMI-Protokolle zugreifen und diese festlegen und eine manuelle Bereinigung durchführen. C++ bietet jedoch den Vorteil von Flexibilität und Leistungsfähigkeit. Daher ist C++ zwar besser für die Verwendung von Visual Basic Scripting Edition (VBScript) oder Windows PowerShell für einfache Prozesse geeignet, aber C++ funktioniert besser für anspruchsvollere Anwendungen und ist für das Schreiben von [Anbietern](providing-data-to-wmi.md)erforderlich.

Im folgenden Verfahren wird beschrieben, wie Sie eine WMI-Anwendung erstellen.

**So erstellen Sie eine WMI-Anwendung**

1.  [Initialisieren Sie COM](initializing-com-for-a-wmi-application.md).

    Da WMI auf COM-Technologie basiert, müssen Sie Aufrufe der Funktionen [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) und [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) ausführen, um auf WMI zuzugreifen.

2.  [Erstellen Sie eine Verbindung mit einem WMI-Namespace.](creating-a-connection-to-a-wmi-namespace.md)

    Definitionsgemäß wird WMI in einem anderen Prozess als Ihre Anwendung ausgeführt. Daher müssen Sie eine Verbindung zwischen Ihrer Anwendung und WMI herstellen.

3.  [Legen Sie die Sicherheitsstufen für die WMI-Verbindung](setting-the-security-levels-on-a-wmi-connection.md)fest.

    Um die verbindung zu verwenden, die Sie mit WMI erstellen, müssen Sie den Identitätswechsel und die Authentifizierungsebenen für Ihre Anwendung festlegen.

4.  Implementieren Sie den Zweck Ihrer Anwendung.

    WMI macht eine Vielzahl von COM-Schnittstellen verfügbar, die für den Zugriff auf und die Bearbeitung von Daten im gesamten Unternehmen verwendet werden. Weitere Informationen finden Sie unter [Bearbeiten von Klassen- und Instanzinformationen,](manipulating-class-and-instance-information.md) [Empfangen eines WMI-Ereignisses](receiving-a-wmi-event.md)und [COM-API für WMI.](com-api-for-wmi.md)

    Hier sollte der Großteil Ihrer WMI-Clientanwendung vorhanden sein, z. B. der Zugriff auf WMI-Objekte oder das Bearbeiten von Daten.

5.  [Bereinigen sie Ihre Anwendung, und fahren Sie sie herunter.](cleaning-up-and-shutting-down-a-wmi-application.md)

    Nachdem Sie Ihre Abfragen an WMI abgeschlossen haben, sollten Sie alle COM-Zeiger zerstören und Ihre Anwendung ordnungsgemäß herunterfahren.

Weitere Informationen und ein Codebeispiel zum Erstellen einer WMI-Anwendung finden Sie unter [Beispiel: Erstellen einer WMI-Anwendung.](example-creating-a-wmi-application.md)

 

 
