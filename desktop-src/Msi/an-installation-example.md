---
description: In diesem Beispiel wird veranschaulicht, wie ein einfaches Windows Installer Paket erstellt wird, mit dem eine Anwendung installiert wird.
ms.assetid: eee1e3e6-74e9-41d0-b732-1f792a4df423
title: Ein Installations Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11eefaab2977bf7cc31e86ac7541b21b345c1aa1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864492"
---
# <a name="an-installation-example"></a>Ein Installations Beispiel

In diesem Beispiel wird veranschaulicht, wie ein einfaches Windows Installer Paket erstellt wird, mit dem eine Anwendung installiert wird. Das Beispiel installiert Notepad, einen Text-Editor, der in Windows enthalten ist, und mehrere Textdateien, die Ereignisse und Eintritte in der imaginären roten Park Arena beschreiben.

Das Beispiel verfügt über die folgenden Spezifikationen:

-   Die Anwendung wird Benutzern als selbst installierendes Windows Installer Paket bereitgestellt, mit dem alle erforderlichen Dateien, Verknüpfungen und Registrierungsinformationen installiert werden.
-   Das Installationspaket stellt dem Benutzer während des Setups möglicherweise einen Benutzeroberflächen-Assistenten zur Verfügung, um Benutzerinformationen zu sammeln.
-   Während des Setups haben Benutzer die Möglichkeit, einzelne Funktionen auszuwählen, die für die lokale Installation, die aus der Quelle auszuwählende oder nicht installiert werden sollen.
-   Eines der Features kann Benutzern als Funktion zum Installieren nach Bedarf angezeigt werden.
-   Mit demselben Paket wird die Anwendung deinstalliert, und alle Anwendungs Dateien und Registrierungsinformationen werden auf dem Computer des Benutzers entfernt.
-   Das Paket ist darauf vorbereitet, ein umfangreiches Upgrade zu erhalten, das das Ändern des Produktcodes umfasst.

Um das Beispiel zu reproduzieren, benötigen Sie ein Software Tool, das eine leere Windows Installer Datenbank erstellen und bearbeiten kann. Mehrere Tools zur Paket Erstellung sind von unabhängigen Softwareanbietern verfügbar. Ein Windows Installer Datenbank-Editor namens Orca wird in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt.

Um das Beispiel abzuschließen, führen Sie die folgenden Schritte aus:

[Planen der Installation](planning-the-installation.md)

[Importieren einer leeren Datenbank](importing-a-blank-database.md)

[Angeben der Verzeichnisstruktur](specifying-directory-structure.md)

[Angeben von Komponenten](specifying-components.md)

[Angeben von Dateien und Dateiattributen](specifying-files-and-file-attributes.md)

[Angeben von Quell Medien](specifying-source-media.md)

[Angeben von Features](specifying-features.md)

[Angeben von Feature-Component Beziehungen](specifying-feature-component-relationships.md)

[Registrierungsinformationen werden hinzugefügt](adding-registry-information.md)

[Angeben von Verknüpfungen](specifying-shortcuts.md)

[Angeben von Eigenschaften](specifying-properties.md)

[Importieren von InstallExecuteSequence](importing-the-installexecutesequence.md)

[Importieren der InstallUISequence-Sequenz](importing-the-installuisequence.md)

[Importieren von "AdminExecuteSequence"](importing-the-adminexecutesequence.md)

[Importieren der AdminUISequence](importing-the-adminuisequence.md)

[Importieren von AdvtExecuteSequence](importing-the-advtexecutesequence.md)

[Hinzufügen von Übersichts Informationen](adding-summary-information.md)

[Importieren der Benutzeroberfläche](importing-the-user-interface.md)

[Überprüfen einer Installations Datenbank](validating-an-installation-database.md)

 

 



