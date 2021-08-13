---
description: Dieses Steuerelementereignis führt eine angegebene Datei aus. Wenn die Datei nicht vorhanden ist oder das Ereignis fehlschlägt, protokolliert Windows Installer den Fehler im ausführlichen Protokoll, ohne ein Dialogfeld mit einer Fehlermeldung anzuzeigen.
ms.assetid: a185c5a1-6584-4916-967a-313e6b7cf97c
title: MsiLaunchApp ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 982152d58748ba8b1b8f9d302766e1e9c55eb2ee3c9fa0ce7582507c017dc9b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118627788"
---
# <a name="msilaunchapp-controlevent"></a>MsiLaunchApp ControlEvent

Dieses Steuerelementereignis führt eine angegebene Datei aus. Wenn die Datei nicht vorhanden ist oder das Ereignis fehlschlägt, protokolliert Windows Installer den Fehler im ausführlichen Protokoll, ohne ein Dialogfeld mit einer Fehlermeldung anzuzeigen.

**[Windows Installer 4.5 oder früher:](not-supported-in-windows-installer-4-5.md)** Wird nicht unterstützt. Dieses ControlEvent ist ab Windows Installer 5.0 verfügbar.

## <a name="published-by"></a>Veröffentlicht von

Dieses ControlEvent wird vom Installationsprogramm veröffentlicht.

## <a name="argument"></a>Argument

Die Felder des Argumentwerts werden durch Leerzeichen getrennt. Das erste Feld enthält einen Zeichenfolgenwert, der die auszuführende Datei angibt. Verwenden Sie den Zeichenfolgenwert \[ \# *filekey,* \] um die Datei zu identifizieren, und ersetzen Sie *filekey* durch den Dateibezeichner, der in der Spalte Datei der [Dateitabelle](file-table.md) angezeigt wird. Alle verbleibenden Felder des Arguments können Parameter enthalten, die von der ausgeführten Datei verwendet werden.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Dieses ControlEvent führt keine Aktionen auf Abonnenten aus.

## <a name="typical-use"></a>Typische Verwendung

So ermöglichen Sie es einem Benutzer, eine Datei am Ende einer Installation auszuführen. Dieses Ereignis kann auf eine Eigenschaft festgelegt werden, die von einem [CheckBox-Steuerelement](checkbox-control.md) festgelegt wird, das im letzten Dialogfeld der Installation angezeigt wird. Das CheckBox-Steuerelement sollte während des Entfernens des Pakets nicht angezeigt werden.

 

 



