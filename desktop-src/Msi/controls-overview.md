---
description: Windows Installer implementiert eine Reihe von Standard Steuerelementen, die Paket Autoren in Dialogfeldern platzieren können. Allerdings sind nicht alle standardmäßigen Microsoft Windows-Steuerelemente verfügbar, und benutzerdefinierte Steuerelemente können nicht für die Verwendung mit der Installer-Benutzeroberfläche erstellt werden.
ms.assetid: 28416905-ce9a-4bb7-97b7-646c01f370ab
title: Übersicht zu Steuerelementen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85fbd8477416eb5a126eca56cb1050112309b0fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352326"
---
# <a name="controls-overview"></a>Übersicht zu Steuerelementen

Windows Installer implementiert eine Reihe von Standard Steuerelementen, die Paket Autoren in Dialogfeldern platzieren können. Allerdings sind nicht alle standardmäßigen Microsoft Windows-Steuerelemente verfügbar, und benutzerdefinierte Steuerelemente können nicht für die Verwendung mit der Installer-Benutzeroberfläche erstellt werden.

Steuerelemente werden in Dialogfeldern im Installer so erstellt, wie Dialogfelder Programm gesteuert mithilfe der Microsoft Windows-Benutzeroberflächen-API erstellt werden. Ein-Steuerelement wird aus einer Vorlage erstellt, die in der Steuerelement Tabelle aufgezeichnet ist. Diese Vorlage unterscheidet sich geringfügig insofern, als Sie den eindeutigen Namen des Dialog Felds enthält, in dem das Steuerelement angezeigt wird.

In der Microsoft Windows-Benutzeroberflächen-API wird die Benutzerinteraktion erreicht, indem eine Rückruffunktion zum Verarbeiten von Nachrichten erstellt wird, die vom Steuerelement gepostet werden. Außerdem empfangen die meisten Microsoft Windows-Steuerelemente Nachrichten, z. b. die von der [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) -Funktion gesendeten.

Die Kommunikation zwischen dem Benutzer und den Steuerelementen wird im Installationsprogramm durch die Verwendung von [ControlEvents](controlevent-overview.md)erreicht. Es gibt jedoch einen begrenzten Satz von ControlEvents, die für jedes Steuerelement in der begrenzten Gruppe von Steuerelementen in Windows Installer spezifisch sind. Steuerelemente können mehr als einen ControlEvent bereitstellen und können mehr als einen ControlEvent erhalten.

Steuerelemente können mithilfe der ControlEvent-Tabelle bestimmte ControlEvents veröffentlichen. Steuerelemente können mithilfe der [EventMapping-Tabelle](eventmapping-table.md)ControlEvents empfangen.

Windows Installer veröffentlicht ControlEvents auch während der Ausführung einiger Aktionen, und Steuerelemente, die diese ControlEvents in der EventMapping-Tabelle abonniert haben, erhalten Sie.

 

 
