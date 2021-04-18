---
title: Richtlinien für Hintergrundaufgaben in Remotedesktopdienste
description: Um die CPU-Verfügbarkeit für alle Benutzer zu maximieren, deaktivieren Sie entweder Hintergrundaufgaben bei der Ausführung in einer Remotedesktopdienste Umgebung, oder erstellen Sie effiziente Hintergrundaufgaben, die nicht ressourcenintensiv sind.
ms.assetid: c3688319-dbe7-4be5-8895-622a8f8797d2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b93169b248fb086b7ccad88aa57c0feae171f91
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338981"
---
# <a name="guidelines-for-background-tasks-in-remote-desktop-services"></a>Richtlinien für Hintergrundaufgaben in Remotedesktopdienste

Hintergrundaufgaben – Aufgaben, die ausgeführt werden, wenn sich die Nachrichten Schleife einer Anwendung im Leerlauf befindet – bieten einen Mechanismus zum Verarbeiten von Aufgaben mit niedriger Priorität in einer Einzelbenutzer Umgebung. In einer Remotedesktopdienste Umgebung wird jedoch der Hintergrund Task eines Benutzers für CPU-Zyklen mit den Vordergrund Aufgaben eines anderen Benutzers in den Vordergrund gesetzt. Wenn mehrere Benutzer sowohl Vordergrund-als auch Hintergrundaufgaben ausführen, sind die CPU-Anforderungen deutlich höher, als wenn alle Benutzer nur Vordergrund Aufgaben ausführen. Um die CPU-Verfügbarkeit für alle Benutzer zu maximieren, deaktivieren Sie entweder Hintergrundaufgaben bei der Ausführung in einer Remotedesktopdienste Umgebung, oder erstellen Sie effiziente Hintergrundaufgaben, die nicht ressourcenintensiv sind.

Weitere Informationen finden Sie unter [erkennen der Remotedesktopdienste Umgebung](detecting-the-terminal-services-environment.md). Nachdem Sie die Remotedesktopdienste Umgebung erkannt haben, können Sie Hintergrundaufgaben für die Anwendung mit demselben Satz von APIs, die Sie zum Verwalten der Tasks verwendet haben, deaktivieren oder neu konfigurieren.

 

 




