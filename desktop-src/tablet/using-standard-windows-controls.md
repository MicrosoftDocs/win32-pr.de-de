---
description: Verwenden Sie Windows Standardsteuerelemente, wenn möglich, da sie vollständig mit Microsoft Active Accessibility kompatibel sind. Dies schließt Steuerelemente ein, die von Windows (User32.dll) und der Windows Common Controls Library (Comctl32.dll) bereitgestellt werden.
ms.assetid: 2d0b255f-52be-423b-a495-64bf21041858
title: Verwenden von Standardsteuerelementen Windows Standardsteuerelementen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71beab38b4ee6ea6472a34b4edb190deed97731496eac7101859a9340c65ad0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449273"
---
# <a name="using-standard-windows-controls"></a>Verwenden von Standardsteuerelementen Windows Standardsteuerelementen

Verwenden Sie Windows Standardsteuerelemente, wenn möglich, da sie vollständig mit Microsoft Active Accessibility kompatibel sind. Dies schließt Steuerelemente ein, die von Windows (User32.dll) und der Windows Common Controls Library (Comctl32.dll) bereitgestellt werden.

Jedes standard Windows-Steuerelement ist ein separates Fenster einer bestimmten Klasse, sodass die Barrierefreiheitshilfe benachrichtigt wird, wenn der Fokus auf ein neues Steuerelement wechselt. Die Hilfe kann die Steuerelementfensterklasse und alle zusätzlichen Nachrichten bestimmen, die zum Abfragen oder Ändern des Steuerelementzustands gesendet werden können. Die Hilfe kann auch alle untergeordneten Steuerelemente identifizieren, die in einem übergeordneten Fenster enthalten sind, und das übergeordnete Steuerelement eines Steuerelements identifizieren.

Einige gängige Steuerelemente sind äußerst flexibel und können häufig weniger zugängliche benutzerdefinierte Steuerelemente und vom Besitzer gezeichnete Steuerelemente ersetzen. Beispielsweise kann eine Listenansicht ein vom Besitzer gezeichnetes Listenfeld ersetzen, um ein Kontrollkästchen neben jedem Element anzuzeigen. Als weiteres Beispiel kann das erweiterte Schaltflächen-Steuerelement sowohl Bilder als auch Text anzeigen. Zuvor musste dafür ein benutzerdefiniertes Steuerelement verwendet werden.

 

 



