---
description: 'So erstellen Sie eine Anwendung für WMI mithilfe von C++: Sie müssen com initialisieren, auf WMI-Protokolle zugreifen und diese festlegen und eine manuelle Bereinigung durchführen.'
ms.assetid: 0b9b7990-6982-4ba9-8dba-7470990405f7
ms.tgt_platform: multiple
title: Erstellen einer WMI-Anwendung mithilfe von C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baaa4f7e79828b2cb6cb496254d906182ff611ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348408"
---
# <a name="creating-a-wmi-application-using-c"></a>Erstellen einer WMI-Anwendung mithilfe von C++

So erstellen Sie eine Anwendung für WMI mithilfe von C++: Sie müssen com initialisieren, auf WMI-Protokolle zugreifen und diese festlegen und eine manuelle Bereinigung durchführen. C++ bietet jedoch den Vorteil von Flexibilität und Leistung. Obwohl Sie in der Verwendung von Visual Basic Scripting Edition (VBScript) oder Windows PowerShell für einfache Prozesse besser tätig sind, funktioniert C++ besser für anspruchsvollere Anwendungen und ist für das Schreiben von [Anbietern](providing-data-to-wmi.md)erforderlich.

Im folgenden Verfahren wird beschrieben, wie eine WMI-Anwendung erstellt wird.

**So erstellen Sie eine WMI-Anwendung**

1.  [Initialisieren von com](initializing-com-for-a-wmi-application.md).

    Da WMI auf der com-Technologie basiert, müssen Sie Aufrufe an die Funktionen [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) und [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) ausführen, um auf WMI zuzugreifen.

2.  [Erstellen Sie eine Verbindung mit einem WMI-Namespace](creating-a-connection-to-a-wmi-namespace.md).

    Definitionsgemäß wird WMI in einem anderen Prozess ausgeführt als die Anwendung. Daher müssen Sie eine Verbindung zwischen Ihrer Anwendung und WMI herstellen.

3.  [Legen Sie die Sicherheitsstufen für die WMI-Verbindung fest](setting-the-security-levels-on-a-wmi-connection.md).

    Um die Verbindung zu verwenden, die Sie mit WMI erstellt haben, müssen Sie die Identitätswechsel-und Authentifizierungs Ebenen für die Anwendung festlegen.

4.  Implementieren Sie den Zweck Ihrer Anwendung.

    WMI macht eine Vielzahl von COM-Schnittstellen verfügbar, die für den Zugriff und die Bearbeitung von Daten im gesamten Unternehmen Weitere Informationen finden Sie unter Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md), [empfangen eines WMI-Ereignisses](receiving-a-wmi-event.md)und [com-API für WMI](com-api-for-wmi.md).

    An dieser Stelle sollte der Großteil der WMI-Client Anwendung vorhanden sein, z. b. der Zugriff auf WMI-Objekte oder die Datenbearbeitung.

5.  [Bereinigen Sie Ihre Anwendung, und](cleaning-up-and-shutting-down-a-wmi-application.md)fahren Sie Sie herunter.

    Nachdem Sie die WMI-Abfragen durchgeführt haben, sollten Sie alle com-Zeiger zerstören und die Anwendung ordnungsgemäß herunterfahren.

Weitere Informationen und ein Codebeispiel zum Erstellen einer WMI-Anwendung finden Sie unter [Beispiel: Erstellen einer WMI-Anwendung](example-creating-a-wmi-application.md).

 

 
