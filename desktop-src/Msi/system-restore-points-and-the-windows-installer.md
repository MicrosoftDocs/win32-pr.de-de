---
description: Die Systemwiederherstellung überwacht und zeichnet wichtige Systemänderungen automatisch auf dem Computer eines Benutzers auf. Weitere Informationen finden Sie unter Systemwiederherstellung.
ms.assetid: 5fc345ff-8a47-4372-806f-64b8c271fd2d
title: Systemwiederherstellungspunkte und das Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48b8de832208f2bee301a1a159da058ba0f97cf2ecbd74892cb809e1186fbb65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118624093"
---
# <a name="system-restore-points-and-the-windows-installer"></a>Systemwiederherstellungspunkte und das Windows Installer

Die Systemwiederherstellung überwacht und zeichnet wichtige Systemänderungen automatisch auf dem Computer eines Benutzers auf. Weitere Informationen finden Sie unter [Systemwiederherstellung.](../sr/system-restore-portal.md)

Systemwiederherstellungspunkte werden vom System und auch vom Windows Installer erstellt, wenn Software installiert oder entfernt wird.

Auf Windows XP erstellt das Installationsprogramm möglicherweise Prüfpunkte während der ersten Installation einer Anwendung und während des Entfernens. Das Installationsprogramm erstellt in diesen Fällen nur Prüfpunkte, wenn die Änderung mit mindestens einer [*einfachen Benutzeroberfläche*](b-gly.md)ausgeführt wird. Installationen, bei denen die [Benutzeroberflächenebene auf](user-interface-levels.md) Keine festgelegt ist, werden in der Regel vom System oder von einer Anwendung initiiert, die die Erstellung eines Prüfpunkts verarbeiten soll. Weitere Informationen finden Sie unter [Systemwiederherstellung.](../sr/system-restore-portal.md)

In Unternehmen mit vielen kleinen Anwendungen können Administratoren die Prüfpunkte im Installationsprogramm deaktivieren, um die Leistung zu verbessern. Weitere Informationen finden Sie unter [LimitSystemRestoreCheckpointing](limitsystemrestorecheckpointing.md) oder [Festlegen eines Wiederherstellungspunkts aus einer benutzerdefinierten Aktion.](setting-a-restore-point-from-a-custom-action.md)

Ab Windows Installer 5.0 kann die [**MSIFASTINSTALL-Eigenschaft**](msifastinstall.md) festgelegt werden, um zu verhindern, dass eine Installation einen Systemwiederherstellungspunkt generiert.

 

 
