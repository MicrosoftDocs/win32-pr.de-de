---
description: Windows Installer installiert und entfernt eine Anwendung oder ein Produkt in Teilen, die als Komponenten bezeichnet werden.
ms.assetid: 949d8b8c-8f1a-4fde-9a7d-824d33436e62
title: Organisieren von Anwendungen in Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3fc2db794bef2a29025bf7ebc54c65691145ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864396"
---
# <a name="organizing-applications-into-components"></a>Organisieren von Anwendungen in Komponenten

Windows Installer installiert und entfernt eine Anwendung oder ein Produkt in Teilen, die als [Komponenten](windows-installer-components.md)bezeichnet werden. Bei Komponenten handelt es sich um Sammlungen von Ressourcen, die von einem Benutzersystem immer als Einheit installiert oder entfernt werden. Bei einer Ressource kann es sich um eine Datei, einen Registrierungsschlüssel, eine Verknüpfung oder etwas anderes handeln, das möglicherweise installiert ist. Jeder Komponente wird eine eindeutige Komponenten Code- [GUID](guid.md)zugewiesen.

Autoren von Installationspaketen sollten nur Komponenten und Versionen von Komponenten erstellen, die ohne Beschädigung anderer Komponenten installiert und entfernt werden können. Außerdem sollte das Entfernen einer Komponente nicht auf verwaiste Ressourcen auf dem Computer des Benutzers zurückgehen, wie z. b. nicht verwendete Dateien, Registrierungsschlüssel oder Verknüpfungen. Um dies zu gewährleisten, sollten die Autoren beim Organisieren von Ressourcen in-Komponenten die folgenden allgemeinen Regeln einhalten:

-   Erstellen Sie niemals zwei Komponenten, die eine Ressource unter dem gleichen Namen und Ziel Speicherort installieren. Wenn eine Ressource in mehreren Komponenten dupliziert werden muss, ändern Sie den Namen oder den Zielort in jeder Komponente. Diese Regel sollte auf Anwendungen, Produkte, Produktversionen und Unternehmen angewendet werden.
-   Beachten Sie, dass die vorherige Regel bedeutet, dass zwei Komponenten nicht dieselbe Schlüssel Pfad Datei aufweisen dürfen. Der Schlüssel Pfad Wert verweist auf eine bestimmte Datei oder einen Ordner, der zu der Komponente gehört, die das Installationsprogramm zum Erkennen der Komponente verwendet. Wenn zwei Komponenten dieselbe Schlüssel Pfad Datei aufweisen, kann das Installationsprogramm nicht unterscheiden, welche Komponente installiert ist. Zwei Komponenten können jedoch einen Schlüssel Pfad Ordner gemeinsam verwenden.
-   Erstellen Sie keine Version einer Komponente, die mit allen früheren Versionen der Komponente nicht kompatibel ist. Die Komponente kann von anderen Anwendungen, Produkten, Produktversionen und Unternehmen gemeinsam genutzt werden. Erstellen Sie stattdessen eine neue-Komponente.
-   Erstellen Sie keine Komponenten, die Ressourcen enthalten, die in mehr als einem Verzeichnis auf dem System des Benutzers installiert werden müssen. Das Installationsprogramm installiert alle Ressourcen in einer Komponente in demselben Verzeichnis. Einige Ressourcen können nicht in Unterverzeichnissen installiert werden.
-   Fügen Sie nicht mehr als einen com-Server pro Komponente ein. Wenn eine Komponente einen com-Server enthält, muss dies der Schlüssel Pfad für die Komponente sein.
-   Geben Sie nicht mehr als eine Datei pro Komponente als Ziel für das **Startmenü** oder eine Desktop Verknüpfung an.

Beim Organisieren einer Anwendung in-Komponenten müssen Paket Ersteller möglicherweise die Ressourcen in einer vorhandenen Installation hinzufügen, entfernen oder ändern. In diesem Fall muss der Autor entscheiden, ob die Ressourcen bereitgestellt werden sollen, indem eine neue Komponente eingeführt oder vorhandene Komponenten geändert und in eine neue Version der Komponente geändert werden. Da bei der Einführung einer neuen Komponente ein eindeutiger Komponenten Code zugewiesen werden muss, müssen Autoren ermitteln, ob Ihre Änderungen das Ändern des Komponenten Codes erfordern. Weitere Informationen finden Sie unter [Ändern des Komponenten Codes](changing-the-component-code.md), [Was geschieht, wenn die Komponenten Regeln beschädigt sind?](what-happens-if-the-component-rules-are-broken.md)und [Definieren von Installerkomponenten](defining-installer-components.md).

 

 



