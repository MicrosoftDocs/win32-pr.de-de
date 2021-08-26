---
description: Windows Das Installationsprogramm installiert und entfernt eine Anwendung oder ein Produkt in Teilen, die als Komponenten bezeichnet werden.
ms.assetid: 949d8b8c-8f1a-4fde-9a7d-824d33436e62
title: Organisieren von Anwendungen in Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1398bbbacbdb15df148576ebf0904f7aec98354a4d417681a81f2195535f08d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129190"
---
# <a name="organizing-applications-into-components"></a>Organisieren von Anwendungen in Komponenten

Windows Das Installationsprogramm installiert und entfernt eine Anwendung oder ein Produkt in Teilen, die als [Komponenten](windows-installer-components.md)bezeichnet werden. Komponenten sind Sammlungen von Ressourcen, die immer als Einheit aus dem System eines Benutzers installiert oder entfernt werden. Eine Ressource kann eine Datei, ein Registrierungsschlüssel, eine Verknüpfung oder eine andere Ressource sein, die installiert werden kann. Jeder Komponente wird eine eindeutige [Komponentencode-GUID](guid.md)zugewiesen.

Autoren von Installationspaketen sollten nur Komponenten und Versionen von Komponenten erstellen, die ohne Beeinträchtigung anderer Komponenten installiert und entfernt werden können. Außerdem sollte das Entfernen einer Komponente keine verwaisten Ressourcen auf dem Computer des Benutzers zurücklassen, z. B. nicht verwendete Dateien, Registrierungsschlüssel oder Verknüpfungen. Um dies sicherzustellen, sollten Autoren beim Organisieren von Ressourcen in Komponenten die folgenden allgemeinen Regeln einhalten:

-   Erstellen Sie niemals zwei Komponenten, die eine Ressource unter dem gleichen Namen und Zielspeicherort installieren. Wenn eine Ressource in mehreren Komponenten dupliziert werden muss, ändern Sie ihren Namen oder Zielspeicherort in jeder Komponente. Diese Regel sollte auf Anwendungen, Produkte, Produktversionen und Unternehmen angewendet werden.
-   Beachten Sie, dass die vorherige Regel bedeutet, dass zwei Komponenten nicht über die gleiche Schlüsselpfaddatei verfügen dürfen. Der Schlüsselpfadwert verweist auf eine bestimmte Datei oder einen Bestimmten Ordner, die bzw. der zu der Komponente gehört, die vom Installationsprogramm zum Erkennen der Komponente verwendet wird. Wenn zwei Komponenten über die gleiche Schlüsselpfaddatei verfügen, kann das Installationsprogramm nicht unterscheiden, welche Komponente installiert ist. Zwei Komponenten können jedoch einen Schlüsselpfadordner gemeinsam verwenden.
-   Erstellen Sie keine Version einer Komponente, die nicht mit allen früheren Versionen der Komponente kompatibel ist. Die Komponente kann von anderen Anwendungen, Produkten, Produktversionen und Unternehmen gemeinsam genutzt werden. Erstellen Sie stattdessen eine neue Komponente.
-   Erstellen Sie keine Komponenten, die Ressourcen enthalten, die in mehreren Verzeichnissen auf dem System des Benutzers installiert werden müssen. Das Installationsprogramm installiert alle Ressourcen in einer Komponente im gleichen Verzeichnis. Es ist nicht möglich, einige Ressourcen in Unterverzeichnissen zu installieren.
-   Schließen Sie nicht mehr als einen COM-Server pro Komponente ein. Wenn eine Komponente einen COM-Server enthält, muss dies der Schlüsselpfad für die Komponente sein.
-   Geben Sie nicht mehr als eine Datei pro Komponente als Ziel für das **Startmenü** oder eine Desktopverknüpfung an.

Beim Organisieren einer Anwendung in Komponenten müssen Paketautoren möglicherweise die Ressourcen in einer vorhandenen Installation hinzufügen, entfernen oder ändern. In diesem Fall muss der Autor entscheiden, ob die Ressourcen durch Einführung einer neuen Komponente oder durch Ändern vorhandener Komponenten und Ändern in eine neue Version der Komponente zur Verfügung gestellt werden sollen. Da beim Einführen einer neuen Komponente ein eindeutiger Komponentencode zugewiesen werden muss, müssen Autoren bestimmen, ob ihre Änderungen eine Änderung des Komponentencodes erfordern. Weitere Informationen finden Sie unter [Ändern des Komponentencodes,](changing-the-component-code.md) [Was geschieht, wenn die Komponentenregeln verletzt werden?](what-happens-if-the-component-rules-are-broken.md)und [Definieren von Installerkomponenten.](defining-installer-components.md)

 

 



