---
description: Bei der Systemwiederherstellung werden wichtige Systemänderungen auf dem Computer eines Benutzers automatisch überwacht und aufgezeichnet. Weitere Informationen finden Sie unter System Wiederherstellung.
ms.assetid: 5fc345ff-8a47-4372-806f-64b8c271fd2d
title: System Wiederherstellungspunkte und die Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7fe9bd4b8e22f5aee7e49d3e4c452378f402e7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359914"
---
# <a name="system-restore-points-and-the-windows-installer"></a>System Wiederherstellungspunkte und die Windows Installer

Bei der Systemwiederherstellung werden wichtige Systemänderungen auf dem Computer eines Benutzers automatisch überwacht und aufgezeichnet. Weitere Informationen finden Sie unter [System Wiederherstellung](../sr/system-restore-portal.md).

System Wiederherstellungspunkte werden vom System erstellt und auch Windows Installer erstellt, wenn Software installiert oder entfernt wird.

Unter Windows XP kann das Installationsprogramm während der ersten Installation einer Anwendung und während des Entfernens Prüfpunkte erstellen. Der Installer erstellt in diesen Fällen nur Prüfpunkte, wenn die Änderung mit mindestens einer [*grundlegenden Benutzeroberfläche*](b-gly.md)ausgeführt wird. Installationen, bei denen die [Benutzeroberflächen Ebene](user-interface-levels.md) auf None festgelegt ist, werden normalerweise vom System oder einer Anwendung initiiert, die das Erstellen eines Prüf Punkts behandeln soll. Weitere Informationen finden Sie unter [System Wiederherstellung](../sr/system-restore-portal.md).

In Unternehmen mit vielen kleinen Anwendungen können Administratoren festlegen, dass die Prüfpunkte im Installer deaktiviert werden, um die Leistung zu verbessern. Weitere Informationen finden Sie unter [limitsystemrestorecheckpointpunkt](limitsystemrestorecheckpointing.md) oder [Festlegen eines Wiederherstellungs Punkts aus einer benutzerdefinierten Aktion](setting-a-restore-point-from-a-custom-action.md).

Ab Windows Installer 5,0 kann die [**msifastinstall**](msifastinstall.md) -Eigenschaft festgelegt werden, um zu verhindern, dass eine Installation einen Systemwiederherstellungspunkt erzeugt.

 

 
