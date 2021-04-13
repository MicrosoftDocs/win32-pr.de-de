---
description: Der Installer zeichnet Fehler und Ereignisse in einem eigenen Fehlerprotokoll auf.
ms.assetid: 244e9afa-2052-469e-aa57-424e03ce5673
title: Normale Protokollierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0846305ef53c596fbd6f117eaf76b0715a94c313
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528169"
---
# <a name="normal-logging"></a>Normale Protokollierung

Der Installer zeichnet Fehler und Ereignisse in einem eigenen Fehlerprotokoll auf. Der Protokollierungstyp, der vom Installationsprogramm ausgeführt wird, wird durch die Einstellung des Protokollierungs Modus bestimmt. Die Protokollierung ist aktiviert, und der Modus kann mithilfe der folgenden Methoden festgelegt werden:

-   Der Protokollierungs Modus einer Installation, die über die Befehlszeile gestartet wird, kann mithilfe der Option/L der [Befehlszeilenoptionen](command-line-options.md)angegeben werden. Wenn der Protokollierungs Modus nicht mithilfe der Befehlszeilenoption/L angegeben wird, wird der Standard Protokollierungs Modus verwendet.
-   Der Protokollierungs Modus eines Installationsprozesses kann Programm gesteuert mithilfe der [**msienablelog**](/windows/desktop/api/Msi/nf-msi-msienableloga) -Funktion oder der [**EnableLog**](installer-enablelog.md) -Methode angegeben werden. Wenn der Protokollierungs Modus nicht mithilfe der **msienablelog** -Funktion oder der **EnableLog** -Methode angegeben wird, wird der Standard Protokollierungs Modus verwendet.
-   Der Standard Protokollierungs Modus eines bestimmten Installationspakets kann durch Festlegen der [**MsiLogging**](msilogging.md) -Eigenschaft in der [Eigenschaften Tabelle](property-table.md) des Pakets angegeben werden. Diese Eigenschaft ist ab Windows Installer 4,0 verfügbar.
-   Wenn die [**MsiLogging**](msilogging.md) -Eigenschaft in der [Eigenschaften Tabelle](property-table.md)vorhanden ist, kann der Standard Protokollierungs Modus des Pakets geändert werden, indem der Wert mithilfe einer [Daten Bank Transformation](database-transforms.md)geändert wird. Der Standard Protokollierungs Modus kann nicht mithilfe von [patchpaketen](patch-packages.md) (MSP-Datei) geändert werden.
-   Wenn die [**MsiLogging**](msilogging.md) -Eigenschaft nicht festgelegt wurde, kann der Standard Protokollierungs Modus für alle Benutzer des Computers mithilfe der [Protokollierungs](logging.md) Richtlinie angegeben werden.
-   Wenn die [**MsiLogging**](msilogging.md) -Eigenschaft festgelegt wurde, kann der Standard Protokollierungs Modus für alle Benutzer des Computers durch Festlegen der Richtlinie " [disableloggingfrompackage](disableloggingfrompackage.md) " und der [Protokollierungs](logging.md) Richtlinie angegeben werden.
-   Wenn der Protokollierungs Modus nicht durch die/L-Option, die [**msienablelog**](/windows/desktop/api/Msi/nf-msi-msienableloga), die [**EnableLog**](installer-enablelog.md), die [**MsiLogging**](msilogging.md) -Eigenschaft oder die [Protokollierungs](logging.md) Richtlinie angegeben wurde, entspricht der Standard Protokollierungs Modus für das Paket dem Modus, der als Festlegen der **MsiLogging** -Eigenschaft auf ' iwearmo ' abgerufen wird.

 

 



