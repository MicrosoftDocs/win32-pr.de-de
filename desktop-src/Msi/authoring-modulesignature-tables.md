---
description: Die Tabelle ModuleSignature enthält alle Informationen, die zum Identifizieren des Mergemoduls erforderlich sind.
ms.assetid: 5f0b4590-dac3-4528-b714-ff760ae8d123
title: Authoring ModuleSignature Tables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c7aaa84b7e5f2db2327bbb272d195333b7a82e609a2dfe2dc72b82eaad9bd09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045410"
---
# <a name="authoring-modulesignature-tables"></a>Authoring ModuleSignature Tables

Die [Tabelle ModuleSignature enthält](modulesignature-table.md) alle Informationen, die zum Identifizieren des Mergemoduls erforderlich sind.

Das Feld ModuleID ist der Primärschlüssel für diese Tabelle und muss der Konvention folgen, die unter Naming Primary Keys in Merge Module Databases (Benennen von [Primärschlüsseln in Mergemoduldatenbanken) beschrieben ist.](naming-primary-keys-in-merge-module-databases.md) Wenn der lesbare Name des Mergemoduls beispielsweise MyLibrary und die GUID für das Mergemodul {880DE2F0-CDD8-11D1-A849-006097ABDE17} lautet, Der Eintrag in der Spalte ModuleID der Tabelle ModuleSignature wird zu MyLibrary.880DE2F0 \_ CDD8 \_ 11D1 \_ A849 \_ 006097ABDE17.

Geben Sie den Dezimalbezeichner für die Standardsprache des Mergemoduls in das Feld Sprache der Tabelle ModuleSignature ein.

Geben Sie die Version des Mergemoduls in das Feld Version ein.

 

 



