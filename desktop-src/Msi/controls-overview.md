---
description: Windows Das Installationsprogramm implementiert eine Reihe von Standardsteuerelementen, die Paketautoren in Dialogfeldern platzieren können. Allerdings sind nicht alle standardmäßigen Microsoft Windows-Steuerelemente verfügbar, und benutzerdefinierte Steuerelemente können nicht für die Verwendung mit der Benutzeroberfläche des Installationsprogramms erstellt werden.
ms.assetid: 28416905-ce9a-4bb7-97b7-646c01f370ab
title: Übersicht zu Steuerelementen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ee9d03f0f21f9cc0611a1fae4831b6ccbbda9f40eda873cdf4c26b259ec43f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638522"
---
# <a name="controls-overview"></a>Übersicht zu Steuerelementen

Windows Das Installationsprogramm implementiert eine Reihe von Standardsteuerelementen, die Paketautoren in Dialogfeldern platzieren können. Allerdings sind nicht alle standardmäßigen Microsoft Windows-Steuerelemente verfügbar, und benutzerdefinierte Steuerelemente können nicht für die Verwendung mit der Benutzeroberfläche des Installationsprogramms erstellt werden.

Steuerelemente werden für Dialogfelder im Installationsprogramm ähnlich wie Dialogfelder programmgesteuert mithilfe der Microsoft Windows-Benutzeroberflächen-API erstellt. Ein Steuerelement wird aus einer Vorlage erstellt, die in der Control-Tabelle aufgezeichnet wurde. Diese Vorlage ist etwas anders, da sie den eindeutigen Namen des Dialogfelds enthält, in dem das Steuerelement angezeigt wird.

In der Microsoft Windows-Benutzeroberflächen-API erfolgt die Benutzerinteraktion durch Erstellen einer Rückruffunktion zum Verarbeiten von Nachrichten, die vom -Steuerelement gesendet werden. Außerdem empfangen die meisten Microsoft Windows-Steuerelemente Nachrichten, z. B. die, die von der [SendMessage-Funktion gesendet](/windows/win32/api/winuser/nf-winuser-sendmessage) werden.

Die Kommunikation zwischen dem Benutzer und den Steuerelementen erfolgt im Installationsprogramm mithilfe von [ControlEvents.](controlevent-overview.md) Es gibt jedoch einen begrenzten Satz von ControlEvents, die für jedes Steuerelement in der begrenzten Gruppe von Steuerelementen im Windows sind. Steuerelemente können mehr als ein ControlEvent veröffentlichen und möglicherweise mehr als ein ControlEvent empfangen.

Steuerelemente können bestimmte ControlEvents mithilfe der ControlEvent-Tabelle veröffentlichen. Steuerelemente können ControlEvents über die [EventMapping-Tabelle empfangen.](eventmapping-table.md)

Windows Das Installationsprogramm veröffentlicht ControlEvents auch während der Ausführung einiger Aktionen, und Steuerelemente, die diese ControlEvents in der EventMapping-Tabelle abonniert haben, erhalten sie.

 

 
