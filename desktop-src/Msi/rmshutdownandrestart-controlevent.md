---
description: Benachrichtigt den Windows Installer, den Neustart-Manager zu verwenden, um alle Anwendungen, die Dateien verwenden, herunterzufahren und sie am Ende der Installation neu zu starten.
ms.assetid: bfa19cc8-4cf7-42ed-9e94-acaeca8d707a
title: RmShutdownAndRestart ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f483e485eeefc2d3a761a3d9c9ff95989a3150dcfd8fff6a36bfb6211504e95e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625890"
---
# <a name="rmshutdownandrestart-controlevent"></a>RmShutdownAndRestart ControlEvent

Dieses Ereignis benachrichtigt den Windows Installer, den [Neustart-Manager](../rstmgr/restart-manager-portal.md) zu verwenden, um alle Anwendungen herunterzufahren, die Dateien verwenden, und sie am Ende der Installation neu zu starten.

Dieses ControlEvent hat keine Auswirkungen, wenn eine der folgenden Punkte zutrifft.

-   Das Betriebssystem, unter dem die Installation ausgeführt wird, ist nicht Windows Vista oder Windows Server 2008.
-   Interaktionen mit dem [Neustart-Manager](../rstmgr/restart-manager-portal.md) wurden durch die [**MSIRESTARTMANAGERCONTROL-Eigenschaft**](msirestartmanagercontrol.md) oder die [DisableAutomaticApplicationShutdown-Richtlinie](disableautomaticapplicationshutdown.md) deaktiviert.
-   Es gibt derzeit keine [geöffnete Neustart-Manager-Sitzung.](../rstmgr/restart-manager-portal.md)
-   Alle Aufrufe des Windows Installers an den [Neustart-Manager](../rstmgr/restart-manager-portal.md) gibt einen Fehler zurück.

## <a name="typical-use"></a>Typische Verwendung

Das RMShutdownAndRestart-Steuerelementereignis wird nur von einem [PushButton-Steuerelement](pushbutton-control.md) im Dialogfeld [MsiRMFilesInUse](msirmfilesinuse-dialog.md) veröffentlicht.

 

 
