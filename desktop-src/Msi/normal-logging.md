---
description: Das Installationsprogramm zeichnet Fehler und Ereignisse in seinem eigenen Fehlerprotokoll auf.
ms.assetid: 244e9afa-2052-469e-aa57-424e03ce5673
title: Normale Protokollierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dd1abeb4f110603bcc596cb7981ea65c7d9820d8054adc7533c4f85de2d8bf7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828540"
---
# <a name="normal-logging"></a>Normale Protokollierung

Das Installationsprogramm zeichnet Fehler und Ereignisse in seinem eigenen Fehlerprotokoll auf. Der Typ der Protokollierung, die vom Installationsprogramm ausgeführt wird, wird durch die Einstellung des Protokollierungsmodus bestimmt. Die Protokollierung ist aktiviert, und der Modus kann mithilfe der folgenden Methoden festgelegt werden:

-   Der Protokollierungsmodus einer Installation, die über die Befehlszeile gestartet wird, kann mithilfe der Option /L der [Befehlszeilenoptionen angegeben werden.](command-line-options.md) Wenn der Protokollierungsmodus nicht mithilfe der Befehlszeilenoption /L angegeben wird, wird der Standardprotokollierungsmodus verwendet.
-   Der Protokollierungsmodus eines Installationsprozesses kann programmgesteuert mithilfe der [**MsiEnableLog-Funktion**](/windows/desktop/api/Msi/nf-msi-msienableloga) oder der [**EnableLog-Methode angegeben**](installer-enablelog.md) werden. Wenn der Protokollierungsmodus nicht mithilfe der **MsiEnableLog-Funktion** oder der **EnableLog-Methode** angegeben wird, wird der Standardprotokollierungsmodus verwendet.
-   Der Standardprotokollierungsmodus eines bestimmten Installationspakets kann durch Festlegen der [**MsiLogging-Eigenschaft**](msilogging.md) in der [Property-Tabelle des](property-table.md) Pakets angegeben werden. Diese Eigenschaft ist ab Windows Installer 4.0 verfügbar.
-   Wenn die [**MsiLogging-Eigenschaft**](msilogging.md) in der [Property-Tabelle](property-table.md)vorhanden ist, kann der Standardprotokollierungsmodus des Pakets geändert werden, indem der Wert mithilfe einer [Datenbanktransformation geändert wird.](database-transforms.md) Der Standardprotokollierungsmodus kann nicht mithilfe von [Patchpaketen](patch-packages.md) (MSP-Datei) geändert werden.
-   Wenn die [**MsiLogging-Eigenschaft**](msilogging.md) nicht festgelegt wurde, kann der Standardprotokollierungsmodus für alle Benutzer des Computers mithilfe der [Protokollierungsrichtlinie angegeben](logging.md) werden.
-   Wenn die [**MsiLogging-Eigenschaft**](msilogging.md) festgelegt wurde, kann der Standardprotokollierungsmodus für alle Benutzer des Computers durch Festlegen der [DisableLoggingFromPackage-Richtlinie](disableloggingfrompackage.md) und der [Protokollierungsrichtlinie angegeben](logging.md) werden.
-   Wenn der Protokollierungsmodus nicht durch die Option /L, [**MsiEnableLog,**](/windows/desktop/api/Msi/nf-msi-msienableloga) [**EnableLog,**](installer-enablelog.md) [**msiLogging**](msilogging.md) oder die Protokollierungsrichtlinie angegeben wurde, ist der Standardprotokollierungsmodus für das Paket der gleiche Modus, der beim Festlegen der **MsiLogging-Eigenschaft** auf "iojmo" ermittelt wird. [](logging.md)

 

 



