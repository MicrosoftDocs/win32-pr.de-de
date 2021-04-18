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
# <a name="enabling-windows-projected-file-system"></a><span data-ttu-id="a4e2e-103">Aktivieren des in Windows projizierten Dateisystems</span><span class="sxs-lookup"><span data-stu-id="a4e2e-103">Enabling Windows Projected File System</span></span>

<span data-ttu-id="a4e2e-104">Projfs wird als optionale Komponente mit Windows ausgeliefert.</span><span class="sxs-lookup"><span data-stu-id="a4e2e-104">ProjFS ships with Windows as an Optional Component.</span></span>  <span data-ttu-id="a4e2e-105">Bevor Sie von einem Anbieter verwendet werden können, muss er aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="a4e2e-105">Before a provider can use it, it must be enabled.</span></span>  <span data-ttu-id="a4e2e-106">Mit</span><span class="sxs-lookup"><span data-stu-id="a4e2e-106">You can use</span></span> <!--the GUI or--> <span data-ttu-id="a4e2e-107">PowerShell zum Aktivieren von projfs.</span><span class="sxs-lookup"><span data-stu-id="a4e2e-107">PowerShell to enable ProjFS.</span></span>

<!--
## How to enable ProjFS in the GUI

Open the Start menu and type "Control Panel".  Click "Programs", then "Turn Windows features on or off".  In the Windows Features dialog box select the check box next to "Windows Projected File System":

![Windows features dialog](images/WindowsFeaturesDialog.png)
-->

## <a name="how-to-enable-projfs-using-powershell"></a><span data-ttu-id="a4e2e-108">Aktivieren von projfs mithilfe von PowerShell</span><span class="sxs-lookup"><span data-stu-id="a4e2e-108">How to enable ProjFS using PowerShell</span></span>

<span data-ttu-id="a4e2e-109">Verwenden Sie das `Enable-WindowsOptionalFeature` Cmdlet in einem PowerShell-Fenster mit erhöhten Rechten, um PowerShell zum Aktivieren von projfs zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="a4e2e-109">To use PowerShell to enable ProjFS use the `Enable-WindowsOptionalFeature` cmdlet in an elevated PowerShell window:</span></span>

```PowerShell
Enable-WindowsOptionalFeature -Online -FeatureName Client-ProjFS -NoRestart
```

<span data-ttu-id="a4e2e-110">Starten Sie den Computer neu, wenn der Enable-WindowsOptionalFeature `RestartNeeded: True` .</span><span class="sxs-lookup"><span data-stu-id="a4e2e-110">Reboot the computer if the Enable-WindowsOptionalFeature reports `RestartNeeded: True`.</span></span>
