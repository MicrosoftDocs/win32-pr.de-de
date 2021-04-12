---
description: In diesem Beispiel wird veranschaulicht, wie benutzerdefinierte Aktionen verwendet werden, um bei der Installation einer-Komponente Benutzerkonten auf einem lokalen Computer zu erstellen.
ms.assetid: fc06dd7b-46d7-45a0-85b3-26f808c64f89
title: Verwenden einer benutzerdefinierten Aktion zum Erstellen von Benutzerkonten auf einem lokalen Computer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfd3bf002c0fa1d661c6bfebb6d1a18cbc4b0652
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346578"
---
# <a name="using-a-custom-action-to-create-user-accounts-on-a-local-computer"></a>Verwenden einer benutzerdefinierten Aktion zum Erstellen von Benutzerkonten auf einem lokalen Computer

In diesem Beispiel wird veranschaulicht, wie benutzerdefinierte Aktionen verwendet werden, um bei der Installation einer-Komponente Benutzerkonten auf einem lokalen Computer zu erstellen. Beim Entfernen einer Komponente werden die von der benutzerdefinierten Aktion erstellten lokalen Benutzerkonten entfernt. Es werden mehrere benutzerdefinierte Aktionen veranschaulicht, z.b. [benutzerdefinierte Aktionen für die verzögerte Ausführung](deferred-execution-custom-actions.md) und [Rollback von benutzerdefinierten Aktionen](rollback-custom-actions.md)

Das Beispiel entspricht den folgenden Spezifikationen.

-   Bei der Installation werden Benutzerkonten nur erstellt, wenn Windows 2000 ausgeführt wird.
-   Bei der Installation werden Benutzerkonten nur dann erstellt, wenn die Komponente zur lokalen Installation installiert wird. Dies verhindert, dass Benutzerkonten während der Reparatur oder Neuinstallation der Komponente erstellt werden.
-   Der Installer entfernt die Konten, wenn die Komponente entfernt wird.
-   Benutzerkontoinformationen werden aus einer benutzerdefinierten Tabelle in der Installations Datenbank gelesen und sind nicht in den benutzerdefinierten Aktions Code hart codiert.
-   Da das Erstellen oder Entfernen von Benutzerkonten erhöhte Rechte erfordert, müssen einige benutzerdefinierte Aktionen in der Lage sein, Änderungen am System vorzunehmen, die erhöhte Rechte erfordern. Diese benutzerdefinierten Aktionen müssen verzögerte benutzerdefinierte Aktionen sein, die im Ausführungs Skript ausgeführt werden.
-   Jedes Konto verfügt über eine benutzerdefinierte Rollback-Aktion, um sicherzustellen, dass das Konto bei einem Rollback der Komponenteninstallation entfernt wird. Dies schließt nicht das Rollback eines Kontos ein, das beim Entfernen einer Komponente gelöscht wird.
-   Benutzerdefinierte Aktionen senden Aktions Daten Meldungen für jedes erstellte oder entfernte Konto. Dies schließt keine Bereitstellung von Statusmeldungen für die ProgressBar ein.
-   Benutzerdefinierte Aktionen melden einen Fehler, wenn ein Konto nicht erstellt werden kann.
-   Das Kennwort für das Konto wird durch die Benutzerinteraktion mit der Benutzeroberfläche oder bei einer Installation auf der Standardbenutzer Oberfläche oder auf keiner [Benutzeroberflächen Ebene](user-interface-levels.md)abgerufen, als eine Eigenschaft, die in der Befehlszeile angezeigt wird.
-   Sensible Daten werden in der Protokolldatei ausgeblendet.

Das Beispiel enthält eine hypothetische Komponente mit dem Namen "Testaccount". Bei der Erörterung in den folgenden Abschnitten wird davon ausgegangen, dass Sie bereits die für Testaccount benötigten Ressourcen erstellt und die Tabellen [Feature](feature-table.md), [Component](component-table.md), [File](file-table.md), [Directory](directory-table.md)und [FeatureComponents](featurecomponents-table.md) in der-Beispieldatenbank erstellt haben, die für die Installation dieser Komponente erforderlich ist. Weitere Informationen finden Sie unter [einem Installations Beispiel](an-installation-example.md).

Die folgenden Themen enthalten Informationen zum Erstellen erforderlicher benutzerdefinierter Aktionen und zum Hinzufügen zu einem-Installationspaket.

-   [Erstellen der benutzerdefinierten Aktionen](authoring-the-custom-actions.md)
-   [Hinzufügen einer benutzerdefinierten customuseraccounts-Tabelle](adding-a-custom-customuseraccounts-table.md)
-   [Erstellen der Tabelle "CustomAction"](authoring-the-customaction-table.md)
-   [Erstellen der Aktions Text-und Fehler Tabellen](authoring-the-actiontext-and-error-tables.md)
-   [Erstellen der InstallExecuteSequence-Tabelle](authoring-the-installexecutesequence-table.md)
-   [Erstellen der Benutzeroberfläche für die Kenn Wort Eingabe](authoring-the-user-interface-for-password-input.md)
-   [Sichern der Installation](securing-the-installation.md)

 

 



