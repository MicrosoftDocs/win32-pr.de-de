---
description: Mergemodule sind im wesentlichen vereinfachte MSI-Dateien, bei denen es sich um die Dateinamenerweiterung für ein Windows Installer Installationspaket handelt. Ein Standard-Mergemodul verfügt über die Dateinamenerweiterung. msm.
ms.assetid: 580fe58a-4636-4f9a-a68d-4fd0e281e949
title: Informationen zu Mergemodulen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70d416b89f0979d5651480a05052e95b4d32e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345169"
---
# <a name="about-merge-modules"></a>Informationen zu Mergemodulen

Mergemodule sind im wesentlichen vereinfachte MSI-Dateien, bei denen es sich um die Dateinamenerweiterung für ein Windows Installer Installationspaket handelt. Ein Standard-Mergemodul verfügt über die Dateinamenerweiterung. msm.

Ein Mergemodul kann nicht allein installiert werden, da es einige wichtige Datenbanktabellen enthält, die in einer Installations Datenbank vorhanden sind. Mergemodule enthalten auch zusätzliche Tabellen, die für sich selbst eindeutig sind. Um die von einem Mergemodul übermittelten Informationen mit einer Anwendung zu installieren, muss das Modul zuerst in der MSI-Datei der Anwendung zusammengeführt werden.

Ein Mergemodul besteht aus den folgenden Teilen:

-   Eine [mergemoduldatenbank](merge-module-database.md) mit den Installations Eigenschaften und der Setup Logik, die vom Mergemodul übermittelt werden.
-   Ein [Zusammenfassungs Daten-Datenstrom Verweis für Zusammenfassungs Module](merge-module-summary-information-stream-reference.md) , der das Modul
-   Eine [MergeModule.CABinet](mergemodule-cabinet.md) -CAB-Datei, die als Stream innerhalb des Mergemoduls gespeichert wird. Diese CAB-Datei enthält alle Dateien, die von den vom Mergemodul gelieferten Komponenten benötigt werden.

[Mehrere Language Merge-Module](multiple-language-merge-modules.md) können Komponenten an ein Installationspaket in mehreren Sprachen bereitzustellen. In einem Mergemodul mit mehreren Sprachen enthält die Datenbank die Installations Eigenschaften und die Logik für mehr als eine Sprache. das MergeModule.CABinet-CAB enthält alle Dateien, die zum Installieren von Komponenten mit allen vom Modul unterstützten Sprachen erforderlich sind.

 

 



