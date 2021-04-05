---
description: Eine Komponenten Tabelle ist in jedem Mergemodul erforderlich.
ms.assetid: ef4a0678-bf6b-47c9-89e8-40e12da52d9b
title: Erstellen von Komponenten Tabellen für Mergemodule
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46557541b3a6b89841fe3e26cef7c00e59dc3911
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042155"
---
# <a name="authoring-merge-module-component-tables"></a>Erstellen von Komponenten Tabellen für Mergemodule

Eine [Komponenten Tabelle](component-table.md) ist in jedem Mergemodul erforderlich. Diese Tabelle enthält einen Datensatz für jede Komponente, die vom Mergemodul an die MSI-Datei des Ziels geliefert wird. Beachten Sie, dass jede dieser Komponenten auch in der [modulecomponents-Tabelle](modulecomponents-table.md) angegeben werden muss, die unter [Erstellen von modulecomponents-Tabellen](authoring-modulecomponents-tables.md)beschrieben wird.

Verwenden Sie die standardmäßige Benennungs Konvention, wenn Sie Namen in die Komponenten Spalte eingeben, um sicherzustellen, dass der Bezeichner für jede Komponente für alle Mergemodule und Installations Datenbanken eindeutig ist. Weitere Informationen finden Sie unter [Benennen von primär Schlüsseln in mergemoduldatenbanken](naming-primary-keys-in-merge-module-databases.md).

Füllen Sie die restlichen Felder in jedem Datensatz aus, wie für eine Installations Datenbank in der [Component-Tabelle](component-table.md)beschrieben. Die Komponenten, die von einem Mergemodul einem Paket hinzugefügt werden, müssen den Richtlinien für gültige Windows Installer Komponenten entsprechen, die in den folgenden Abschnitten beschrieben werden:

-   [Windows Installer Komponenten](windows-installer-components.md)
-   [Organisieren von Anwendungen in Komponenten](organizing-applications-into-components.md)

 

 



