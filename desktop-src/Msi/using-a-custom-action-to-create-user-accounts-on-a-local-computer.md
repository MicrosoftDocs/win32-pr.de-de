---
description: In diesem Beispiel wird veranschaulicht, wie benutzerdefinierte Aktionen verwendet werden, um Benutzerkonten auf einem lokalen Computer zu erstellen, wenn eine Komponente installiert wird.
ms.assetid: fc06dd7b-46d7-45a0-85b3-26f808c64f89
title: Verwenden einer benutzerdefinierten Aktion zum Erstellen von Benutzerkonten auf einem lokalen Computer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 408c80a5fbf32d9da758322bd6c5ebc881da73501d2b241c39f64cdd779d239d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499580"
---
# <a name="using-a-custom-action-to-create-user-accounts-on-a-local-computer"></a>Verwenden einer benutzerdefinierten Aktion zum Erstellen von Benutzerkonten auf einem lokalen Computer

In diesem Beispiel wird veranschaulicht, wie benutzerdefinierte Aktionen verwendet werden, um Benutzerkonten auf einem lokalen Computer zu erstellen, wenn eine Komponente installiert wird. Durch das Entfernen einer Komponente werden die lokalen Benutzerkonten entfernt, die von der benutzerdefinierten Aktion erstellt wurden. Es werden mehrere benutzerdefinierte Aktionen veranschaulicht, einschließlich benutzerdefinierte Aktionen für [verzögerte Ausführung](deferred-execution-custom-actions.md) und [Rollback für benutzerdefinierte Aktionen.](rollback-custom-actions.md)

Das Beispiel erfüllt die folgenden Spezifikationen.

-   Bei der Installation werden Benutzerkonten nur erstellt, wenn Windows 2000 ausgeführt wird.
-   Bei der Installation werden Benutzerkonten nur erstellt, wenn die Komponente installiert wird, um lokal ausgeführt zu werden. Dies schließt das Erstellen von Benutzerkonten während der Reparatur oder Neuinstallation der Komponente aus.
-   Das Installationsprogramm entfernt die Konten, wenn die Komponente entfernt wird.
-   Benutzerkontoinformationen werden aus einer benutzerdefinierten Tabelle in der Installationsdatenbank gelesen und nicht hart in den benutzerdefinierten Aktionscode codiert.
-   Da die Erstellung oder Entfernung von Benutzerkonten erhöhte Rechte erfordert, müssen einige der benutzerdefinierten Aktionen Änderungen am System vornehmen können, für die erhöhte Rechte erforderlich sind. Diese benutzerdefinierten Aktionen müssen benutzerdefinierte Aktionen zurückgestellt werden, die ausgeführt werden, wenn sie im Ausführungsskript enthalten sind.
-   Jedes Konto verfügt über eine benutzerdefinierte Rollbackaktion, um sicherzustellen, dass das Konto beim Rollback der Komponenteninstallation entfernt wird. Dies schließt nicht das Rollback eines Kontolöschvorgangs während des Entfernens einer Komponente ein.
-   Benutzerdefinierte Aktionen senden ActionData-Nachrichten für jedes Konto, das erstellt oder entfernt wird. Dies schließt nicht das Bereitstellen von Statusmeldungen für die ProgressBar ein.
-   Benutzerdefinierte Aktionen melden einen Fehler, wenn ein Konto nicht erstellt werden kann.
-   Das Kennwort für das Konto wird über die Benutzerinteraktion mit der Benutzeroberfläche oder im Fall einer Installation auf der Basic-Benutzeroberfläche oder none [Benutzeroberfläche Levels](user-interface-levels.md)als Eigenschaft abgerufen, die an die Befehlszeile übergeben wird.
-   Vertrauliche Daten werden in der Protokolldatei ausgeblendet.

Das Beispiel enthält eine hypothetische Komponente namens TestAccount. In den folgenden Abschnitten wird davon ausgegangen, dass Sie bereits die für TestAccount erforderlichen Ressourcen erstellt und die Tabellen [Feature](feature-table.md), [Component](component-table.md), [File](file-table.md), [Directory](directory-table.md)und [FeatureComponents](featurecomponents-table.md) in der Beispieldatenbank erstellt haben, die zum Installieren dieser Komponente erforderlich sind. Weitere Informationen finden Sie unter [Ein Installationsbeispiel.](an-installation-example.md)

Die folgenden Themen enthalten Informationen zum Erstellen erforderlicher benutzerdefinierter Aktionen und zum Hinzufügen zu einem Installationspaket.

-   [Erstellen der benutzerdefinierten Aktionen](authoring-the-custom-actions.md)
-   [Hinzufügen einer CustomUserAccounts-Tabelle](adding-a-custom-customuseraccounts-table.md)
-   [Erstellen der CustomAction-Tabelle](authoring-the-customaction-table.md)
-   [Erstellen der ActionText- und Error-Tabellen](authoring-the-actiontext-and-error-tables.md)
-   [Erstellen der Tabelle "InstallExecuteSequence"](authoring-the-installexecutesequence-table.md)
-   [Erstellen der Benutzeroberfläche für die Kennworteingabe](authoring-the-user-interface-for-password-input.md)
-   [Sichern der Installation](securing-the-installation.md)

 

 



