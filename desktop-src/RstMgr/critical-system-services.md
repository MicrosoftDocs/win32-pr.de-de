---
title: Wichtige System Dienste
description: Kritische Systemdienste können vom Neustart-Manager ohne Systemneustart nicht beendet und neu gestartet werden. Updates an Dateien oder Ressourcen, die von einem dieser Dienste verwendet werden, erfordern einen Systemneustart.
ms.assetid: 8db7c91c-2f96-4d0c-a5b8-59c41a7e4845
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a8fcc921d065dda0670e27e240c93515bc8cb9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037655"
---
# <a name="critical-system-services"></a>Wichtige System Dienste

Kritische Systemdienste können vom Neustart-Manager ohne Systemneustart nicht beendet und neu gestartet werden. Updates an Dateien oder Ressourcen, die von einem dieser Dienste verwendet werden, erfordern einen Systemneustart.

**, Um zu bestimmen, ob ein Prozess ein kritischer Systemdienst ist.**

1.  Registrieren Sie den Prozess mit der [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) -Funktion.
2.  Aufrufen der [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) -Funktion zum Abrufen der [**RM- \_ Prozess \_ Informations**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) Struktur.
3.  Der **applicationtype** -Member der zurückgegebenen [**RM- \_ Prozess \_ Informations**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) Struktur enthält den Enumerationswert des [**RM-APP- \_ \_ Typs**](/windows/desktop/api/RestartManager/ne-restartmanager-rm_app_type) . Dieser Wert wird für einen kritischen System Prozess auf **rmcriticial** festgelegt.

Wichtige Systemdienste sind smss.exe, csrss.exe, wininit.exe, logonui.exe, lsass.exe, services.exe, winlogon.exe, System, svchost.exe mit RPCSS und svchost.exe mit DCOM/PNP.

 

 




