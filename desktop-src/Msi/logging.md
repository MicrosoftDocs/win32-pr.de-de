---
description: Diese computerspezifische Systemrichtlinie wird nur verwendet, wenn die Protokollierung nicht durch die Befehlszeilenoption &\# 0034;/L&\# 0034; oder msiEnableLog aktiviert wurde.
ms.assetid: d8649808-5dc3-4496-8c2f-da9b1512b5aa
title: Protokollierung (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49993419b03e3c092fdf4d2b6d9d118ca4dc2d3d641c82c4fc829cbfd6b68c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945635"
---
# <a name="logging-windows-installer"></a>Protokollierung (Windows Installer)

Diese computerspezifische [Systemrichtlinie](system-policy.md) wird nur verwendet, wenn die Protokollierung nicht durch die Befehlszeilenoption "/L" oder [**msiEnableLog aktiviert wurde.**](/windows/desktop/api/Msi/nf-msi-msienableloga) Wenn die Richtlinie in diesem Fall festgelegt ist, erstellt das Installationsprogramm eine Protokolldatei in %temp% mit dem zufälligen Namen MSI \* . Protokoll. Geben Sie den Protokollierungsmodus an, indem Sie den Richtlinienwert auf eine Zeichenfolge festlegen. Verwenden Sie dieselben Zeichen, um die Protokollierungsmodusrichtlinie anzugeben, die von der Befehlszeilenoption "/L" [verwendet wird.](command-line-options.md) Beachten Sie, dass Sie "+" und " \* " nicht für die Richtlinie verwenden können.

Der Protokollierungsmodus kann mithilfe einer Richtlinie, einer Befehlszeilenoption oder programmgesteuert festgelegt werden. Weitere Informationen zu allen Methoden, die zum Festlegen des Protokollierungsmodus verfügbar sind, finden Sie unter [Normale](normal-logging.md) Protokollierung im Abschnitt Windows [Installer-Protokollierung.](windows-installer-logging.md)

Sie können verhindern, dass vertrauliche Informationen, z. B. Kennwörter, in die Protokolldatei eingegeben und sichtbar gemacht werden. Weitere Informationen finden Sie unter [Verhindern, dass vertrauliche Informationen in die Protokolldatei geschrieben werden.](preventing-confidential-information-from-being-written-into-the-log-file.md)

## <a name="registry-key"></a>Registrierungsschlüssel

Legen Sie den Wert logging unter dem folgenden Registrierungsschlüssel fest.

**HKEY \_ LOCAL \_** \\ **MACHINE-Softwarerichtlinien** \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Datentyp

**REG \_ SZ**

 

 



