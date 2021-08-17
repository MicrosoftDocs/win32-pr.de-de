---
description: Mergemodule sind im Wesentlichen .msi Dateien vereinfacht. Dies ist die Dateierweiterung für Windows Installer-Installationspaket. Ein Standardzusammenführungsmodul hat die Dateinamenerweiterung MSM.
ms.assetid: 580fe58a-4636-4f9a-a68d-4fd0e281e949
title: Informationen zu Mergemodulen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca3e6c0ec1d4d7073d85984539ce54b47de92885a64570bc1de709be64748b22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118640162"
---
# <a name="about-merge-modules"></a>Informationen zu Mergemodulen

Mergemodule sind im Wesentlichen .msi Dateien vereinfacht. Dies ist die Dateierweiterung für Windows Installer-Installationspaket. Ein Standardzusammenführungsmodul hat die Dateinamenerweiterung MSM.

Ein Mergemodul kann nicht allein installiert werden, da es nicht über einige wichtige Datenbanktabellen verfügt, die in einer Installationsdatenbank vorhanden sind. Mergemodule enthalten auch zusätzliche Tabellen, die für sich selbst eindeutig sind. Um die informationen zu installieren, die von einem Mergemodul mit einer Anwendung bereitgestellt werden, muss das Modul zuerst in der Anwendungsdatei .msi werden.

Ein Mergemodul besteht aus den folgenden Teilen:

-   Eine [Mergemoduldatenbank mit](merge-module-database.md) den Installationseigenschaften und der Setuplogik, die vom Mergemodul bereitgestellt werden.
-   Eine [Zusammenfassungsinformationsstreamreferenz für Mergemodule,](merge-module-summary-information-stream-reference.md) in der das Modul beschrieben wird.
-   EineMergeModule.CABinet-Schränkdatei, die als Stream innerhalb des Mergemoduls gespeichert ist. [](mergemodule-cabinet.md) Diese Schränkung enthält alle Dateien, die von den komponenten benötigt werden, die vom Mergemodul bereitgestellt werden.

[Mehrere Sprachzusammenführungsmodule](multiple-language-merge-modules.md) können Komponenten in einem Installationspaket in mehreren Sprachen liefern. In einem Mergemodul mit mehreren Sprachen enthält die Datenbank die Installationseigenschaften und die Logik für mehr als eine Sprache, und die MergeModule.CAB-Inet-Schränkung enthält alle Dateien, die zum Installieren von Komponenten mit allen vom Modul unterstützten Sprachen erforderlich sind.

 

 



