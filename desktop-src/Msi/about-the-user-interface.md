---
description: Windows Das Installationsprogramm enthält Funktionen, mit denen Entwickler von Installationspaketen eine grafische Benutzeroberfläche (GUI) erstellen können, die dem Endbenutzer während der Installation angezeigt wird.
ms.assetid: 58ef0043-fb30-4f64-9291-e703d7a28bb5
title: Informationen zum Benutzeroberfläche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ff4613e82bc25a0a9555904a6bab276b31e16642186401bbb5cc0caff58e973
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996980"
---
# <a name="about-the-user-interface"></a>Informationen zum Benutzeroberfläche

Windows Das Installationsprogramm enthält Funktionen, mit denen Entwickler von Installationspaketen eine grafische Benutzeroberfläche (GUI) erstellen können, die dem Endbenutzer während der Installation angezeigt wird. Diese Benutzeroberfläche kann [das](user-interface-wizard-behavior.md)Verhalten des Benutzeroberflächen-Assistenten zeigen, Dialogfelder und Fenster anzeigen und Benutzern während der Installation interaktive Steuerelemente präsentieren.

Die interne Benutzeroberfläche des Installationsprogramms wird über eine Reihe von Datenbanktabellen innerhalb Windows Installer selbst verwaltet und gesteuert. Das Installationsprogramm stellt nur einen kleinen Satz von Standarddialogfeldern zur Verfügung, die fehler- und informationsmeldungen behandeln sollen. Alle benutzerdefinierten Dialogfelder müssen vom Paketautor erstellt werden.

Es gibt keine spezifische Windows Installer-API, mit der ein Paketautor programmgesteuert eine Benutzeroberfläche erstellen kann. Es ist möglich, die Microsoft Windows-API zu verwenden, um programmgesteuert eine Benutzeroberfläche zu erstellen. Es wird jedoch empfohlen, dass Paketautoren die bereitgestellte interne Benutzeroberfläche verwenden.

Erautoren von Installerpaketen erstellen benutzerdefinierte Dialogfelder, indem sie den Namen ihres benutzerdefinierten Dialogs in die Spalte "Dialog" der Dialogtabelle eingeben und die Größe, Position und andere Attribute mithilfe der verbleibenden Spalten \_ angeben.

Windows Das Installationsprogramm implementiert auch eine Reihe von Standardsteuerelementen, die ein Paketautor in Dialogfeldern platzieren kann. Nicht alle standardmäßigen Microsoft Windows-Steuerelemente sind verfügbar, und benutzerdefinierte Steuerelemente können nicht für die Verwendung mit der Benutzeroberfläche des Installationsprogramms erstellt werden.

Steuerelemente werden in einem bestimmten Dialogfeld erstellt, indem sie den Namen des Dialogfelds, den Primärschlüssel für den Eintrag des Dialogfelds in der Dialogfeldtabelle, in das zweite Feld der Steuertabelle eingeben und die Größe, Position und andere Attribute des Steuerelements mithilfe der verbleibenden Spalten angeben.

Aktive Steuerelemente müssen mit einem ControlEvent in der [ControlEvent-Tabelle](controlevent-table.md) verknüpft sein, damit Benutzerinteraktion mit der Installation möglich ist. Passive Steuerelemente, die Informationen empfangen und anzeigen, müssen ein entsprechendes ControlEvent in der [EventMapping-Tabelle abonniert werden.](eventmapping-table.md)

Weitere Informationen zu ControlEvents finden Sie unter [ControlEvent Overview](controlevent-overview.md). Beachten Sie, dass ein Steuerelement ein ControlEvent veröffentlicht, wenn es in der ControlEvent-Tabelle aufgeführt ist, und ein Ereignis abonniert, wenn es in der EventMapping-Tabelle aufgeführt ist.

Die Anzeige der Installer-Benutzeroberfläche während der Installation wird über die Sequenztabellen der Benutzeroberfläche verwaltet: [InstallUISequence-Tabelle](installuisequence-table.md)und [AdminUISequence-Tabelle.](adminuisequence-table.md) Eine dieser Sequenztabellen wird abhängig von der Aktion der obersten Ebene ausgeführt, die die Installation initiiert hat: [INSTALL](install-action.md), [ADMIN](admin-action.md)oder [ADVERTISE](advertise-action.md).

Weitere Informationen zum Implementieren einer Benutzeroberfläche im Windows-Installer finden Sie unter Verwenden von [Benutzeroberfläche](using-the-user-interface.md), [Benutzeroberfläche-Schema](user-interface-schema.md)und den einzelnen Themen für Dialogfelder und Steuerelemente.

 

 



