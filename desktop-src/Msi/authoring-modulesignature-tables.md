---
description: Die ModuleSignature-Tabelle enthält alle Informationen, die zum Identifizieren des Mergemoduls erforderlich sind.
ms.assetid: 5f0b4590-dac3-4528-b714-ff760ae8d123
title: Erstellen von ModuleSignature-Tabellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 796775b0237c17db4fa21075a792c372bed3e97b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351638"
---
# <a name="authoring-modulesignature-tables"></a>Erstellen von ModuleSignature-Tabellen

Die [ModuleSignature-Tabelle](modulesignature-table.md) enthält alle Informationen, die zum Identifizieren des Mergemoduls erforderlich sind.

Das ModuleID-Feld ist der Primärschlüssel für diese Tabelle und muss der in Benennen von [primär Schlüsseln in mergemoduldatenbanken](naming-primary-keys-in-merge-module-databases.md)beschriebenen Konvention folgen. Wenn beispielsweise der lesbare Name des Mergemoduls MyLibrary und die GUID für das Mergemodul {880de2f0-cdd8-11d1-a849-006097abde17} ist, wird der Eintrag in der ModuleID-Spalte der ModuleSignature-Tabelle zu MyLibrary. 880de2f0 \_ CDD8 \_ 11d1 \_ A849 \_ 006097abde17.

Geben Sie den Dezimal Bezeichner für die Standardsprache des Mergemoduls in das Sprachfeld der ModuleSignature-Tabelle ein.

Geben Sie die Version des Mergemoduls in das Feld Version ein.

 

 



