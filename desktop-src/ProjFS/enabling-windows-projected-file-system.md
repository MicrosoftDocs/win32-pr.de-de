---
title: Aktivieren des in Windows projizierten Dateisystems
description: Hier wird beschrieben, wie Sie projfs unter Windows aktivieren.
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/17/2018
ms.topic: article
ms.openlocfilehash: f903192190877631084e366bcaeafd8b5b0e7e72
ms.sourcegitcommit: 42cdae4d2eca84713ab3f7a5c88f583a352991a8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/23/2019
ms.locfileid: "106338354"
---
# <a name="enabling-windows-projected-file-system"></a>Aktivieren des in Windows projizierten Dateisystems

Projfs wird als optionale Komponente mit Windows ausgeliefert.  Bevor Sie von einem Anbieter verwendet werden können, muss er aktiviert werden.  Mit <!--the GUI or--> PowerShell zum Aktivieren von projfs.

<!--
## How to enable ProjFS in the GUI

Open the Start menu and type "Control Panel".  Click "Programs", then "Turn Windows features on or off".  In the Windows Features dialog box select the check box next to "Windows Projected File System":

![Windows features dialog](images/WindowsFeaturesDialog.png)
-->

## <a name="how-to-enable-projfs-using-powershell"></a>Aktivieren von projfs mithilfe von PowerShell

Verwenden Sie das `Enable-WindowsOptionalFeature` Cmdlet in einem PowerShell-Fenster mit erhöhten Rechten, um PowerShell zum Aktivieren von projfs zu verwenden:

```PowerShell
Enable-WindowsOptionalFeature -Online -FeatureName Client-ProjFS -NoRestart
```

Starten Sie den Computer neu, wenn der Enable-WindowsOptionalFeature `RestartNeeded: True` .
