---
description: Diese pro-Computer-System Richtlinie wird nur verwendet, wenn die Protokollierung nicht durch die \# Befehlszeilenoption "&0034;/L&\# 0034;" oder durch "msienablelog" aktiviert wurde.
ms.assetid: d8649808-5dc3-4496-8c2f-da9b1512b5aa
title: Protokollierung (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a461051022791e414fe7e211e4dde33c7e83101b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756613"
---
# <a name="logging-windows-installer"></a>Protokollierung (Windows Installer)

Diese Computer spezifische [System Richtlinie](system-policy.md) wird nur verwendet, wenn die Protokollierung nicht durch die Befehlszeilenoption "/L" oder durch " [**msienablelog**](/windows/desktop/api/Msi/nf-msi-msienableloga)" aktiviert wurde. Wenn die Richtlinie in diesem Fall festgelegt wird, erstellt das Installationsprogramm eine Protokolldatei in% Temp% mit dem zufälligen Namen MSI \* . Angezeigt. Legen Sie den Protokollierungs Modus fest, indem Sie den Richtlinien Wert auf eine Zeichenfolge festlegen. Verwenden Sie die gleichen Zeichen, um die Protokollierungs Modus-Richtlinie anzugeben, die von der [Befehlszeilenoption](command-line-options.md)"/L" verwendet wird. Beachten Sie, dass Sie nicht "+" und " \* " für die Richtlinie verwenden können.

Der Protokollierungs Modus kann mithilfe von Richtlinie, einer Befehlszeilenoption oder Programm gesteuert festgelegt werden. Weitere Informationen zu allen Methoden, die zum Festlegen des Protokollierungs Modus verfügbar sind, finden Sie unter [normale Protokollierung](normal-logging.md) im Abschnitt [Windows Installer Protokollierung](windows-installer-logging.md) .

Sie können verhindern, dass vertrauliche Informationen, z. b. Kenn Wörter, in die Protokolldatei eingegeben und sichtbar gemacht werden. Weitere Informationen finden Sie unter [verhindern, dass vertrauliche Informationen in die Protokolldatei geschrieben werden](preventing-confidential-information-from-being-written-into-the-log-file.md) .

## <a name="registry-key"></a>Registrierungsschlüssel

Legen Sie den Wert Logging unter dem folgenden Registrierungsschlüssel fest.

**HKEY \_ Software Richtlinien für lokale \_ Computer** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Datentyp

**REG- \_ SZ**

 

 



