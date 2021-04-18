---
description: Dieses Steuerungs Ereignis führt eine angegebene Datei aus. Wenn die Datei nicht vorhanden ist oder das Ereignis fehlschlägt, protokolliert Windows Installer den Fehler im ausführlichen Protokoll, ohne dass ein Dialogfeld mit einer Fehlermeldung angezeigt wird.
ms.assetid: a185c5a1-6584-4916-967a-313e6b7cf97c
title: Msilaunchapp ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 298867868a80eb2cb831a2304325d14355adc669
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347296"
---
# <a name="msilaunchapp-controlevent"></a>Msilaunchapp ControlEvent

Dieses Steuerungs Ereignis führt eine angegebene Datei aus. Wenn die Datei nicht vorhanden ist oder das Ereignis fehlschlägt, protokolliert Windows Installer den Fehler im ausführlichen Protokoll, ohne dass ein Dialogfeld mit einer Fehlermeldung angezeigt wird.

**[Windows Installer 4,5 oder früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt. Dieses ControlEvent ist ab Windows Installer 5,0 verfügbar.

## <a name="published-by"></a>Veröffentlicht von

Diese ControlEvent wird vom Installationsprogramm veröffentlicht.

## <a name="argument"></a>Argument

Die Felder des Argument Werts sind durch Leerzeichen begrenzt. Das erste Feld enthält einen Zeichen folgen Wert, der die Datei angibt, die ausgeführt werden soll. Verwenden Sie den Zeichen folgen Wert \[ \# *filekey* \] , um die Datei zu identifizieren und *filekey* durch den Bezeichner der Datei zu ersetzen, der in der Datei Spalte der [Datei](file-table.md) Tabelle angezeigt wird. Alle verbleibenden Felder des Arguments können Parameter enthalten, die von der Datei verwendet werden, die ausgeführt wird.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Diese ControlEvent führt keine Aktionen für Abonnenten aus.

## <a name="typical-use"></a>Typische Verwendung

, Um es einem Benutzer zu ermöglichen, eine Datei am Ende einer-Installation auszuführen. Dieses Ereignis kann auf eine Eigenschaft festgelegt werden, die durch ein [CheckBox](checkbox-control.md) -Steuerelement festgelegt wird, das im abschließenden Dialogfeld der Installation angezeigt wird. Beim Entfernen des Pakets sollte das CheckBox-Steuerelement nicht angezeigt werden.

 

 



