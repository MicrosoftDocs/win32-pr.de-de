---
description: Writer können die Leistung verschiedener Sicherungs Typen auf Datei Satz Ebene optimieren, indem Sie den Sicherungstyp für die Datei Angabe angeben, der durch eine Bitmaske oder bitweise OR der Member der VSS- \_ dateispezifizierungstyp- \_ \_ \_ Enumeration angegeben wird.
ms.assetid: a3ac69b4-894a-4536-8fab-f45ad7e5118a
title: Schema Unterstützung auf Dateiebene
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460d256a3eaa016933e697687d05e26838c14ae2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960735"
---
# <a name="file-level-schema-support"></a>Schema Unterstützung auf Dateiebene

Writer können die Leistung verschiedener Sicherungs Typen auf [*Datei Satz*](vssgloss-f.md) Ebene optimieren, indem Sie den Sicherungstyp für die Datei Angabe angeben, der durch eine Bitmaske oder bitweise OR der Member der [**VSS- \_ dateispezifizierungstyp \_ \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) -Enumeration angegeben wird.

Für angegebene Sicherungs Typen gibt der Writer Folgendes an:

-   Gibt an, ob es erforderlich ist, das Volume mit einem Schatten zu kopieren, um einen Datei Satz ordnungsgemäß zu sichern. Wenn beispielsweise die Dateien in einem Datei Satz nicht exklusiv vom Writer geöffnet werden und sichergestellt werden können, dass Sie stabil sind, wird keine Schatten Kopie benötigt.
-   Gibt an, ob der Anforderer die Sicherung so ausführen muss, dass unabhängig vom Zeitpunkt der letzten Änderung oder anderen Problemen die bei der Sicherung aktuelle Version der Dateien des Datei Satzes wieder hergestellt wird. In der Regel bedeutet dies, dass der Dateisatz als Teil der Sicherung kopiert wird.

Die Werte für den [**Sicherungstyp der VSS-Datei Spezifikation, die die \_ schattenkopieanforderung \_ \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) angeben,

-   VSS \_ fsbt \_ alle \_ Momentaufnahmen \_ erforderlich
-   Vollständige VSS- \_ fsbt- \_ \_ Momentaufnahme \_ erforderlich
-   VSS- \_ fsbt- \_ differenzielle \_ Momentaufnahme \_ erforderlich
-   VSS \_ fsbt- \_ inkrementelle \_ Momentaufnahme \_ erforderlich
-   VSS- \_ fsbt- \_ Protokoll \_ Momentaufnahme \_ erforderlich

Die Werte für den [**\_ \_ \_ \_ Sicherungstyp der VSS-Datei Spezifikation**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) , die die Anforderung zum Sichern einer Datei angeben, lauten:

-   VSS \_ fsbt \_ alle \_ Sicherungen \_ erforderlich
-   Vollständige VSS- \_ fsbt- \_ \_ Sicherung \_ erforderlich
-   VSS- \_ fsbt- \_ differenzielle \_ Sicherung \_ erforderlich
-   \_ \_ inkrementelle Sicherung von VSS fsbt \_ \_ erforderlich
-   VSS- \_ fsbt- \_ Protokoll \_ Sicherung \_ erforderlich

Standardmäßig werden Dateigruppen mit dem Sicherungstyp "Datei Spezifikation" VSS \_ fsbt \_ alle \_ Sicherungen \_ erforderlich \| VSS \_ fsbt \_ alle \_ Momentaufnahmen \_ erforderlich. Dies bedeutet, dass bei der Verarbeitung der Datei Satz Dateien immer eine Schatten Kopie erforderlich ist und dass die Dateien in alle Sicherungs Typen kopiert werden sollen.

 

 



