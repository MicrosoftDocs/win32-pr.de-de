---
description: Diese computerspezifische Systemrichtlinie deaktiviert die Erstellung von Prüfpunkten durch Windows Installer.
ms.assetid: 706d6c85-3876-4205-b7da-b0fd709e65dd
title: LimitSystemRestoreCheckpointing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cbea03dcab5db690f6fc06725dbb38a376310e967b9e92a9fcb0c59daab0180
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763510"
---
# <a name="limitsystemrestorecheckpointing"></a>LimitSystemRestoreCheckpointing

Diese computerspezifische [Systemrichtlinie](system-policy.md) deaktiviert die Erstellung von Prüfpunkten durch Windows Installer.

Legen Sie auf 0 (oder nicht vorhanden) fest. Das Installationsprogramm führt normale Prüfpunkte für die Installation oder Deinstallation durch. Auf 1 festgelegt, erstellt das Installationsprogramm keine Prüfpunkte.

Diese Richtlinie wirkt sich nur auf Prüfpunkte aus, die vom Windows festgelegt werden. Auf Windows XP-Computern können Administratoren das Prüfpunkting innerhalb Windows Installer deaktivieren, um die Leistung zu verbessern. [**Bei der Systemwiederherstellung**](../sr/system-restore-portal.md) werden auch zusätzliche Prüfpunkte erstellt. Weitere Informationen finden Sie unter [Systemwiederherstellungspunkte und Windows](system-restore-points-and-the-windows-installer.md) Installer und Festlegen eines Wiederherstellungspunkts [aus einer benutzerdefinierten Aktion.](setting-a-restore-point-from-a-custom-action.md)

## <a name="registry-key"></a>Registrierungsschlüssel

Legen Sie den Wert namens LimitSystemRestoreCheckpointing unter dem folgenden Registrierungsschlüssel fest.

**HKEY \_ LOCAL MACHINE Software Policies Microsoft Windows \_ \\ \\ \\ \\ \\ Installer**

## <a name="data-type"></a>Datentyp

**REG \_ DWORD**

 

 
