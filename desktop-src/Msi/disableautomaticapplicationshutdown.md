---
description: Wenn diese pro-Computer-System Richtlinie auf 1 (eins) festgelegt ist, wird Windows Installer nicht mit dem Neustart-Manager interagieren, aber das Dialogfeld FilesInUse verwendet. wenn diese pro-Computer-System Richtlinie auf 2 (2) festgelegt ist, verwendet Windows Installer das FilesInUse-Dialogfeld.
ms.assetid: a59de5bb-e0a1-459d-83e6-afaf81298123
title: Disableautomaticapplicationshutdown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 060c4027a1fb4026f4e1d578bd1d0c2ed8cd979c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356898"
---
# <a name="disableautomaticapplicationshutdown"></a>Disableautomaticapplicationshutdown

Wenn diese Computer spezifische System Richtlinie auf 1 (eins) festgelegt ist, interagiert Windows Installer nicht mit dem [Neustart-Manager](/windows/desktop/RstMgr/restart-manager-portal), sondern verwendet das [Dialog Feld FilesInUse](filesinuse-dialog.md).

Wenn diese pro-Computer-System Richtlinie auf 2 (2) festgelegt ist, wird Windows Installer das [FilesInUse-Dialog](filesinuse-dialog.md)Feld verwendet. Mit dieser Einstellung werden Versuche durch den [Neustart-Manager](/windows/desktop/RstMgr/restart-manager-portal) deaktiviert, um beim Installieren eines Windows Installer Pakets, das noch nicht für die Verwendung des Neustart-Managers erstellt wurde, Neustarts zu vermeiden. Der Installer verwendet weiterhin den Neustart-Manager, um die von Anwendungen verwendeten Dateien zu erkennen.

Die disableautomaticapplicationshutdown-Richtlinie ist ab Windows Installer Version 4,0 unter Windows Vista verfügbar.

## <a name="registry-key"></a>Registrierungsschlüssel

**HKEY \_ Software Richtlinien für lokale \_ Computer** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Datentyp

**REG \_ DWORD**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md)
</dt> <dt>

[Wird in Windows Installer 3,1 und früheren Versionen nicht unterstützt.](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
