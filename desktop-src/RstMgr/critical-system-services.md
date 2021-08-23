---
title: Wichtige Systemdienste
description: Kritische Systemdienste können vom Neustart-Manager nicht ohne Systemneustart beendet und neu gestartet werden. Aktualisierungen von Dateien oder Ressourcen, die von einem dieser Dienste verwendet werden, erfordern einen Systemneustart.
ms.assetid: 8db7c91c-2f96-4d0c-a5b8-59c41a7e4845
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb8a50eca43a62d24e0ab6363844bef7457aaf05b34251f5d804dacabaead5e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010228"
---
# <a name="critical-system-services"></a>Wichtige Systemdienste

Kritische Systemdienste können vom Neustart-Manager nicht ohne Systemneustart beendet und neu gestartet werden. Aktualisierungen von Dateien oder Ressourcen, die von einem dieser Dienste verwendet werden, erfordern einen Systemneustart.

**So bestimmen Sie, ob ein Prozess ein kritischer Systemdienst ist.**

1.  Registrieren Sie den Prozess mithilfe der [**RmRegisterResources-Funktion.**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources)
2.  Rufen Sie die [**RmGetList-Funktion**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) auf, um die [**RM PROCESS \_ \_ INFO-Struktur**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) abzurufen.
3.  Der **ApplicationType-Member** der zurückgegebenen [**RM PROCESS \_ \_ INFO-Struktur**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) enthält einen [**RM APP \_ TYPE-Enumerationswert. \_**](/windows/desktop/api/RestartManager/ne-restartmanager-rm_app_type) Dieser Wert wird für einen kritischen Systemprozess auf **RmCriticial** festgelegt.

Wichtige Systemdienste umfassen smss.exe, csrss.exe, wininit.exe, logonui.exe, lsass.exe, services.exe, winlogon.exe, System, svchost.exe mit RPCSS und svchost.exe mit Dcom/PnP.

 

 




