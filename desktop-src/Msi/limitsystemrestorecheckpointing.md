---
description: Diese pro-Computer-System Richtlinie deaktiviert die Erstellung von Prüfpunkten durch Windows Installer.
ms.assetid: 706d6c85-3876-4205-b7da-b0fd709e65dd
title: Limitsystemrestorecheckpoints
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7606d266b4e9e42f6287669df9b3ab33a3ad9f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348407"
---
# <a name="limitsystemrestorecheckpointing"></a>Limitsystemrestorecheckpoints

Diese pro-Computer- [System Richtlinie](system-policy.md) deaktiviert die Erstellung von Prüfpunkten durch Windows Installer.

Wenn der Wert 0 (null) oder nicht vorhanden ist, führt der Installer für die Installation oder Deinstallation eine normale Auf 1 festgelegt ist, erstellt das Installationsprogramm keine Prüfpunkte.

Diese Richtlinie wirkt sich nur auf Prüfpunkte aus, die von Windows Installer Auf Windows XP-Computern können Administratoren festlegen, dass Prüfpunkte in Windows Installer deaktiviert werden, um die Leistung zu verbessern. Die [**System Wiederherstellung**](../sr/system-restore-portal.md) erstellt auch zusätzliche Prüfpunkte. Weitere Informationen finden Sie unter [System Wiederherstellungspunkte und die Windows Installer](system-restore-points-and-the-windows-installer.md) und [Festlegen eines Wiederherstellungs Punkts aus einer benutzerdefinierten Aktion](setting-a-restore-point-from-a-custom-action.md).

## <a name="registry-key"></a>Registrierungsschlüssel

Legen Sie den Wert limitsystemrestorecheckpoints unter dem folgenden Registrierungsschlüssel fest.

**\_Software Richtlinien für den lokalen HKEY- \_ Computer \\ \\ \\ Microsoft \\ Windows \\ Installer**

## <a name="data-type"></a>Datentyp

**REG \_ DWORD**

 

 
