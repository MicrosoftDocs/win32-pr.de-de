---
description: Ein Installationspaket enthält alle Informationen, die der Windows Installer benötigt, um eine Anwendung oder ein Produkt zu installieren oder zu deinstallieren und die Benutzeroberfläche für das Setup auszuführen.
ms.assetid: 532b3492-919f-4999-b86c-e3c210876141
title: Installationspaket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61daf878a7933353382a52acd9a7172e87b97b14cdf41a047279360342ca768b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633820"
---
# <a name="installation-package"></a>Installationspaket

Ein Installationspaket enthält alle Informationen, die der Windows Installer benötigt, um eine Anwendung oder ein Produkt zu installieren oder zu deinstallieren und die Benutzeroberfläche für das Setup auszuführen. Jedes Installationspaket enthält eine .msi-Datei, die eine Installationsdatenbank, einen Zusammenfassungsinformationsdatenstrom und Datenströme für verschiedene Teile der Installation enthält. Die .msi-Datei kann auch eine oder mehrere Transformationen, interne Quelldateien und externe Quelldateien oder Cab-Dateien enthalten, die für die Installation erforderlich sind.

Anwendungsentwickler müssen eine Installation erstellen, um das Installationsprogramm zu verwenden. Da das Installationsprogramm Installationen rund um das Konzept von [Komponenten und Features](components-and-features.md)organisiert und alle Informationen zur Installation in einer relationalen Datenbank speichert, umfasst der Prozess der Erstellung eines Installationspakets im Wesentlichen die folgenden Schritte:

-   Identifizieren Sie die Features, die Benutzern angezeigt werden sollen.
-   Organisieren Sie die Anwendung in Komponenten.
-   Füllen Sie die Installationsdatenbank mit Informationen auf.
-   Überprüfen Sie das Installationspaket.

Im nächsten Abschnitt werden Komponenten und Features des Installationsprogramms erläutert. Weitere Informationen finden Sie unter [Komponenten und Features.](components-and-features.md) Die Auswahl der Features wird häufig durch die Funktionalität der Anwendung aus Sicht des Benutzers bestimmt.

Es wird empfohlen, dass Entwickler ein Standardverfahren zum Auswählen von Komponenten verwenden. Weitere Informationen finden Sie unter [Organisieren von Anwendungen in Komponenten.](organizing-applications-into-components.md)

Paketautoren können Tools zum Erstellen von Paketen von Drittanbietern oder einen Tabellen-Editor und das Windows Installer SDK verwenden, um die Installationsdatenbank aufzufüllen. Alle Installationspakete müssen auf interne Konsistenz überprüft werden. Weitere Informationen finden Sie unter [Paketvalidierung.](package-validation.md)

 

 



