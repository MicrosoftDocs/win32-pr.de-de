---
title: Richtlinien für Hintergrundaufgaben in Remotedesktopdienste
description: Um die CPU-Verfügbarkeit für alle Benutzer zu maximieren, deaktivieren Sie entweder Hintergrundaufgaben, wenn sie in einer Remotedesktopdienste-Umgebung ausgeführt werden, oder erstellen Sie effiziente Hintergrundaufgaben, die nicht ressourcenintensiv sind.
ms.assetid: c3688319-dbe7-4be5-8895-622a8f8797d2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c19590d32db21ad08e1d31cbe02e0850bd0964282c8f709207837c3c2a638a12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131289"
---
# <a name="guidelines-for-background-tasks-in-remote-desktop-services"></a>Richtlinien für Hintergrundaufgaben in Remotedesktopdienste

Hintergrundaufgaben – Aufgaben, die ausgeführt werden, wenn sich die Nachrichtenschleife einer Anwendung im Leerlauf befindet – stellen einen Mechanismus zum Behandeln von Aufgaben mit niedriger Priorität in einer Einzelbenutzerumgebung dar. In einer Remotedesktopdienste-Umgebung konkurriert die Hintergrundaufgabe eines Benutzers jedoch um CPU-Zyklen mit den Vordergrundaufgaben eines anderen Benutzers. Wenn mehrere Benutzer sowohl Vordergrund- als auch Hintergrundaufgaben ausführen, sind die CPU-Anforderungen viel höher als wenn alle Benutzer nur Vordergrundaufgaben ausführen. Um die CPU-Verfügbarkeit für alle Benutzer zu maximieren, deaktivieren Sie entweder Hintergrundaufgaben, wenn sie in einer Remotedesktopdienste-Umgebung ausgeführt werden, oder erstellen Sie effiziente Hintergrundaufgaben, die nicht ressourcenintensiv sind.

Weitere Informationen finden Sie unter [Erkennen der Remotedesktopdienste Umgebung.](detecting-the-terminal-services-environment.md) Nachdem Sie die Remotedesktopdienste erkannt haben, können Sie Hintergrundaufgaben für die Anwendung mit dem gleichen Satz von APIs, die Sie zum Verwalten der Aufgaben verwendet haben, deaktivieren oder neu konfigurieren.

 

 




