---
description: Eine Komponente ist ein Teil der zu installierenden Anwendung oder des Produkts.
ms.assetid: f1c9696d-3267-44be-a904-ab26250fae2e
title: Windows Installer Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad90f2fb576d0333a26fc92f9cf951e4da06bab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960031"
---
# <a name="windows-installer-components"></a>Windows Installer Komponenten

Eine Komponente ist ein Teil der zu installierenden Anwendung oder des Produkts. Beispiele für Komponenten sind einzelne Dateien, eine Gruppe verwandter Dateien, com-Objekte, Registrierungen, Registrierungsschlüssel, Verknüpfungen, Ressourcen, in einem Verzeichnis gruppierte Bibliotheken oder freigegebene Code Elemente wie MFC oder DAO.

Der Installer-Dienst installiert oder entfernt eine Komponente als einzelner zusammenhängendes Element. Alle Komponenten werden nach der jeweiligen Komponenten-ID-GUID, die in der ComponentID-Spalte der [Component-Tabelle](component-table.md)angegeben ist, nachverfolgt.

> [!Note]  
> Zwei Komponenten, die dieselbe Komponenten-ID verwenden, werden unabhängig von Ihrem tatsächlichen Inhalt als mehrere Instanzen derselben Komponente behandelt. Auf dem Computer eines Benutzers ist nur eine einzelne Instanz einer Komponente installiert. Mehrere Features oder Anwendungen können daher einige Komponenten gemeinsam nutzen.

 

Da Komponenten im allgemeinen gemeinsam genutzt werden, muss der Autor eines Installationspakets strenge Regeln befolgen, wenn die Komponenten eines Features oder einer Anwendung angegeben werden. Dies ist für den ordnungsgemäßen Betrieb des Windows Installer Verweis Zählmechanismus entscheidend. Weitere Informationen finden Sie unter [Organisieren von Anwendungen in Komponenten](organizing-applications-into-components.md).

Diese Regeln sind:

-   Jede Komponente muss in einem einzelnen Ordner gespeichert werden.
-   Es sollten nie Dateien, Registrierungseinträge, Verknüpfungen oder andere Ressourcen als Mitglied von mehr als einer Komponente ausgeliefert werden. Dies gilt für Produkte, Produktversionen und Unternehmen.

Weitere Informationen zur Verwendung von-Komponenten finden Sie unter.

-   [Installieren einer fehlenden Komponente](installing-a-missing-component.md)
-   [Installieren von permanenten Komponenten, Dateien, Schriftarten, Registrierungs Schlüsseln](installing-permanent-components-files-fonts-registry-keys.md)
-   [Verwenden qualifizierter Komponenten](using-qualified-components.md)
-   [Verwenden transitiv Komponenten](using-transitive-components.md)
-   [Arbeiten mit Features und Komponenten](working-with-features-and-components.md)
-   [Erstellen eines großen Pakets](authoring-a-large-package.md)
-   [Überprüfen der Installation von Features, Komponenten, Dateien](checking-the-installation-of-features-components-files.md)
-   [Suchen nach einer unterbrochenen Funktion oder Komponente](searching-for-a-broken-feature-or-component.md)
-   [Veröffentlichen von Produkten, Features und Komponenten](publishing-products-features-and-components.md)

 

 



