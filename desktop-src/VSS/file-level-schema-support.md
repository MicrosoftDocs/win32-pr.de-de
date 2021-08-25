---
description: Writer können die Leistung verschiedener Sicherungstypen auf Dateisatzebene optimieren, indem sie über einen Dateispezifikations-Sicherungstyp angeben, der durch eine Bitmaske oder bitweises OR der Member der VSS FILE SPEC BACKUP TYPE-Enumeration angegeben \_ \_ \_ \_ wird.
ms.assetid: a3ac69b4-894a-4536-8fab-f45ad7e5118a
title: Schemaunterstützung auf Dateiebene
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550885a540e62fc145541bae979fad34cb9488f62f9f26ea17e647068c1fad46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006370"
---
# <a name="file-level-schema-support"></a>Schemaunterstützung auf Dateiebene

Writer können die Leistung verschiedener Sicherungstypen [](vssgloss-f.md) auf Dateisatzebene optimieren, indem sie über einen Dateispezifikations-Sicherungstyp angeben, der durch eine Bitmaske oder bitweises OR der Member der [**VSS \_ FILE SPEC \_ \_ BACKUP \_ TYPE-Enumeration**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) angegeben wird.

Für angegebene Sicherungstypen gibt der Writer Folgendes an:

-   Gibt an, ob eine Schattenkopie des Volumes erforderlich ist, um einen Dateisatz ordnungsgemäß zu sichern. Wenn z. B. die Dateien in einem Dateisatz nicht ausschließlich vom Writer geöffnet werden und sichergestellt werden können, dass sie stabil sind, ist keine Schattenkopie erforderlich.
-   Gibt an, ob der Anfordernde die Sicherung so durchführen muss, dass unabhängig vom Zeitpunkt der letzten Änderung oder anderen Problemen die bei der Sicherung aktuelle Version der Dateien des Dateisets wiederhergestellt wird. In der Regel bedeutet dies, dass der Dateisatz als Teil der Sicherung kopiert wird.

Die Werte von [**VSS \_ FILE SPEC \_ BACKUP \_ \_ TYPE,**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) die die Schattenkopieanforderung angeben, sind:

-   VSS \_ FSBT \_ ALLE \_ MOMENTAUFNAHMEN \_ ERFORDERLICH
-   VOLLSTÄNDIGE VSS \_ \_ \_ FSBT-MOMENTAUFNAHME \_ ERFORDERLICH
-   VSS FSBT DIFFERENTIAL SNAPSHOT REQUIRED (VSS \_ \_ FSBT-DIFFERENZIELLE \_ \_ MOMENTAUFNAHME ERFORDERLICH)
-   VSS \_ FSBT: \_ INKREMENTELLE \_ \_ MOMENTAUFNAHME ERFORDERLICH
-   VSS \_ \_ FSBT-PROTOKOLLMOMENTAUFNAHME \_ \_ ERFORDERLICH

Die Werte von [**VSS \_ FILE SPEC \_ BACKUP \_ \_ TYPE,**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) die die Anforderung zum Sichern einer Datei angeben, sind:

-   VSS \_ \_ FSBT: ALLE \_ \_ SICHERUNGEN ERFORDERLICH
-   VOLLSTÄNDIGE VSS \_ \_ \_ FSBT-SICHERUNG \_ ERFORDERLICH
-   VSS FSBT DIFFERENTIAL BACKUP REQUIRED (VSS \_ \_ FSBT-DIFFERENZIELLE \_ \_ SICHERUNG ERFORDERLICH)
-   VSS \_ FSBT: \_ INKREMENTELLE \_ SICHERUNG \_ ERFORDERLICH
-   VSS \_ \_ FSBT-PROTOKOLLSICHERUNG \_ \_ ERFORDERLICH

Standardmäßig werden Dateisätze mit dem Dateispezifikationssicherungstyp VSS \_ FSBT \_ ALL BACKUP REQUIRED \_ \_ \| VSS FSBT ALL SNAPSHOT REQUIRED gekennzeichnet. Dies \_ bedeutet, \_ \_ \_ dass für die Verarbeitung der Dateien des Dateisets immer eine Schattenkopie erforderlich ist und dass die Dateien in alle Sicherungstypen kopiert werden sollen.

 

 



