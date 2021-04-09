---
description: Windows Installer enthält Funktionen, die es Installationspaket Entwicklern ermöglichen, eine grafische Benutzeroberfläche (GUI) zu erstellen, die dem Endbenutzer während der Installation angezeigt wird.
ms.assetid: 58ef0043-fb30-4f64-9291-e703d7a28bb5
title: Informationen zur Benutzeroberfläche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8639a19c5ec045d77cb90648323388d5cb6e452
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864531"
---
# <a name="about-the-user-interface"></a>Informationen zur Benutzeroberfläche

Windows Installer enthält Funktionen, die es Installationspaket Entwicklern ermöglichen, eine grafische Benutzeroberfläche (GUI) zu erstellen, die dem Endbenutzer während der Installation angezeigt wird. Diese Benutzeroberfläche kann das [Verhalten des Benutzeroberflächen-Assistenten](user-interface-wizard-behavior.md)anzeigen, Dialogfelder und Plakatwände anzeigen und Benutzern während der Installation interaktive Steuerelemente präsentieren.

Die interne Benutzeroberfläche des Installers wird durch einen Satz von Datenbanktabellen innerhalb Windows Installer selbst verwaltet und gesteuert. Das Installationsprogramm bietet nur einen kleinen Satz von Standard Dialogfeldern, die für die Behandlung von Fehler-und Informationsmeldungen vorgesehen sind. Alle benutzerdefinierten Dialogfelder müssen vom Paket Ersteller erstellt werden.

Es gibt keine spezifische Windows Installer-API, mit der ein Paket Autor eine Benutzeroberfläche Programm gesteuert erstellen kann. Es ist möglich, die Microsoft Windows-API zum programmgesteuerten Erstellen einer Benutzeroberfläche zu verwenden. Es wird jedoch empfohlen, dass Paket Autoren die bereitgestellte interne Benutzeroberfläche verwenden.

Installer-Paket Autoren erstellen benutzerdefinierte Dialogfelder, indem Sie den Namen des benutzerdefinierten Dialog Felds in die \_ Spalte "Dialog" der Dialogfeld Tabelle eingeben und die Größe, Position und andere Attribute mit den verbleibenden Spalten angeben.

Windows Installer implementiert auch eine Reihe von Standard Steuerelementen, die ein Paket Autor in Dialogfeldern platzieren kann. Nicht alle standardmäßigen Microsoft Windows-Steuerelemente sind verfügbar, und benutzerdefinierte Steuerelemente können nicht zur Verwendung mit der Installer-Benutzeroberfläche erstellt werden.

Steuerelemente werden in einem bestimmten Dialogfeld erstellt, indem der Name des Dialog Felds, der Primärschlüssel zum Eintrag des Dialog Felds in der Dialogfeld Tabelle, in das zweite Feld der Steuerelement Tabelle eingegeben und die Größe, Position und andere Attribute des Steuer Elements mithilfe der restlichen Spalten angegeben werden.

Aktive Steuerelemente müssen mit einem ControlEvent in der [ControlEvent-Tabelle](controlevent-table.md) verknüpft werden, um die Benutzerinteraktion mit der Installation zu ermöglichen. Passive Steuerelemente, die Informationen empfangen und anzeigen, müssen ein entsprechendes ControlEvent in der [Tabelle EventMapping](eventmapping-table.md)abonniert werden.

Weitere Informationen zu ControlEvents finden Sie unter [ControlEvent Overview](controlevent-overview.md). Beachten Sie, dass ein Steuerelement ein ControlEvent veröffentlicht, wenn es in der Tabelle ControlEvent aufgeführt ist, und ein Ereignis abonniert, wenn es in der Tabelle EventMapping aufgeführt ist.

Die Benutzeroberfläche der Installer-Benutzeroberfläche wird während der Installation über die Benutzeroberflächen-Sequenz Tabellen verwaltet: [Tabelle "InstallUISequence](installuisequence-table.md)" und " [AdminUISequence](adminuisequence-table.md)". Eine dieser Sequenz Tabellen wird ausgeführt, abhängig von der Aktion der obersten Ebene, die die Installation initiiert hat: " [install](install-action.md)", " [Admin](admin-action.md) [" oder "](advertise-action.md)Ankündigungs".

Weitere Informationen zum Implementieren einer Benutzeroberfläche in Windows Installer finden Sie unter [Verwenden der Benutzeroberfläche](using-the-user-interface.md), [Benutzeroberflächen Schema](user-interface-schema.md)sowie der einzelnen Themen für Dialogfelder und Steuerelemente.

 

 



