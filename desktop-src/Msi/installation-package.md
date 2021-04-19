---
description: Ein-Installationspaket enthält alle Informationen, die die Windows Installer zum Installieren oder Deinstallieren einer Anwendung oder eines Produkts und zum Ausführen der Setup-Benutzeroberfläche benötigt.
ms.assetid: 532b3492-919f-4999-b86c-e3c210876141
title: Installationspaket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe5e5ff79d0c868036dd12ed533b1cd18f9f70d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349281"
---
# <a name="installation-package"></a>Installationspaket

Ein-Installationspaket enthält alle Informationen, die die Windows Installer zum Installieren oder Deinstallieren einer Anwendung oder eines Produkts und zum Ausführen der Setup-Benutzeroberfläche benötigt. Jedes Installationspaket enthält eine MSI-Datei, die eine Installations Datenbank, einen Zusammenfassungs Datenstrom und Datenströme für verschiedene Teile der Installation enthält. Die MSI-Datei kann auch eine oder mehrere Transformationen, interne Quelldateien und externe Quelldateien oder CAB-Dateien enthalten, die für die Installation erforderlich sind.

Anwendungsentwickler müssen eine Installation erstellen, um das Installationsprogramm zu verwenden. Da das Installationsprogramm Installationen im Zusammenhang mit dem Konzept der [Komponenten und Features](components-and-features.md)organisiert und alle Informationen zur Installation in einer relationalen Datenbank speichert, umfasst der Prozess der Erstellung eines Installationspakets im Allgemeinen die folgenden Schritte:

-   Identifizieren Sie die Features, die Benutzern angezeigt werden sollen.
-   Organisieren Sie die Anwendung in Komponenten.
-   Füllen Sie die Installations Datenbank mit Informationen auf.
-   Überprüfen Sie das Installationspaket.

Im nächsten Abschnitt werden die Installationsprogramm Komponenten und-Funktionen erläutert. Weitere Informationen finden Sie unter [Komponenten und Features](components-and-features.md). Die Auswahl der Features hängt häufig von der Funktionalität der Anwendung aus der Sicht des Benutzers ab.

Es wird empfohlen, dass Entwickler ein Standardverfahren zum Auswählen von-Komponenten verwenden. Weitere Informationen finden Sie unter [Organisieren von Anwendungen in Komponenten](organizing-applications-into-components.md).

Paket Autoren können Paket Erstellungs Tools von Drittanbietern oder einen Tabellen-Editor und das Windows Installer SDK zum Auffüllen der Installations Datenbank verwenden. Alle Installationspakete müssen auf interne Konsistenz überprüft werden. Weitere Informationen finden Sie unter [Paket Validierung](package-validation.md).

 

 



