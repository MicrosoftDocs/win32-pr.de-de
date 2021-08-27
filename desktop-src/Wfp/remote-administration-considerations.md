---
description: Es gibt einige Aspekte, die nur für remote verwaltete Systeme gelten.
ms.assetid: bfdf121e-9b4e-4323-82ec-9bd32531caad
title: Überlegungen zur WFP-Remoteverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99b3106a02aa4098d2814a955e6582d6e8f1c79f7f161a6875891e13a0db71a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098590"
---
# <a name="wfp-remote-administration-considerations"></a>Überlegungen zur WFP-Remoteverwaltung

Es gibt einige Aspekte, die nur für remote verwaltete Systeme gelten. Erstens: Wenn die Softwareinstallation remote bereitgestellt wird (per SMS oder MSI), werden WFP-Fehlerdialogfelder auf dem Bildschirm eines lokal angemeldeten Administrators (sofern vorhanden) und nicht im Installationsdienst angezeigt. Wenn sich ein Administrator remote bei einem Terminalserver anmeldet und eine Anwendung installiert, die geschützte Systemdateien ersetzt, werden die WFP-Fehlerdialogfelder nur in der Hauptkonsole und nicht im Remotefenster des Administrators angezeigt.

Aus diesen Gründen unterdrückt WFP die Fehlerdialogfelder, bis sich ein Administrator lokal anmeldet. Remoteadministratoren können Dateiersetzungsfehler im Systemereignisprotokoll finden.

**Windows Vista und Windows Server 2008:** Die WFP-Remoteverwaltung wird nicht unterstützt.

 

 



