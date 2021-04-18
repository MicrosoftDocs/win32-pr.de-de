---
description: Benachrichtigt den Windows Installer, mit dem Neustart-Manager alle Anwendungen mit verwendeten Dateien herunterzufahren und am Ende der Installation neu zu starten.
ms.assetid: bfa19cc8-4cf7-42ed-9e94-acaeca8d707a
title: Rmshutdownandrestart ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc91d1de52f516c0728e8d6469fb8cddc2e50cfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343774"
---
# <a name="rmshutdownandrestart-controlevent"></a>Rmshutdownandrestart ControlEvent

Dieses Ereignis benachrichtigt den Windows Installer, den Neustart- [Manager](../rstmgr/restart-manager-portal.md) zu verwenden, um alle Anwendungen mit verwendeten Dateien herunterzufahren und am Ende der Installation neu zu starten.

Dieses ControlEvent hat keine Auswirkung, wenn eine der folgenden Punkte zutrifft.

-   Das Betriebssystem, auf dem die Installation ausgeführt wird, ist nicht Windows Vista oder Windows Server 2008.
-   Interaktionen mit dem [Neustart-Manager](../rstmgr/restart-manager-portal.md) wurden durch die [**msirestartmanagercontrol**](msirestartmanagercontrol.md) -Eigenschaft oder die [disableautomaticapplicationshutdown](disableautomaticapplicationshutdown.md) -Richtlinie deaktiviert.
-   Zurzeit ist keine geöffnete [Neustart-Manager](../rstmgr/restart-manager-portal.md) -Sitzung vorhanden.
-   Bei allen Aufrufen der Windows Installer an den [Neustart-Manager](../rstmgr/restart-manager-portal.md) wird ein Fehler zurückgegeben.

## <a name="typical-use"></a>Typische Verwendung

Das Ereignis rmshutdownandrestart-Steuerelement wird nur von einem [PUSHBUTTON](pushbutton-control.md) -Steuerelement im [Dialog Feld msirmfilesinuse](msirmfilesinuse-dialog.md) veröffentlicht.

 

 
