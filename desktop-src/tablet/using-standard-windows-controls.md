---
description: Verwenden Sie nach Möglichkeit standardmäßige Windows-Steuerelemente, da Sie vollständig mit den Microsoft-Active Accessibility Richtlinien kompatibel sind. Dies schließt Steuerelemente ein, die von Windows (User32.dll) und der allgemeinen Windows-Steuerelement Bibliothek (Comctl32.dll) bereitgestellt werden.
ms.assetid: 2d0b255f-52be-423b-a495-64bf21041858
title: Verwenden von Windows-Standard Steuerelementen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8732ce48bee762b9a7f3f76669c5dbc45b07c831
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343288"
---
# <a name="using-standard-windows-controls"></a>Verwenden von Windows-Standard Steuerelementen

Verwenden Sie nach Möglichkeit standardmäßige Windows-Steuerelemente, da Sie vollständig mit den Microsoft-Active Accessibility Richtlinien kompatibel sind. Dies schließt Steuerelemente ein, die von Windows (User32.dll) und der allgemeinen Windows-Steuerelement Bibliothek (Comctl32.dll) bereitgestellt werden.

Jedes standardmäßige Windows-Steuerelement ist ein separates Fenster einer bestimmten Klasse, sodass die Barrierefreiheits Hilfe benachrichtigt wird, wenn der Fokus auf ein neues Steuerelement verschoben wird. Die Unterstützung kann die Fenster Klasse des Steuer Elements sowie alle zusätzlichen Meldungen ermitteln, die zum Abfragen oder Ändern des Steuerelement Zustands gesendet werden können. Die Hilfe kann auch alle untergeordneten Steuerelemente identifizieren, die in einem übergeordneten Fenster enthalten sind, und das übergeordnete Steuerelement eines beliebigen Steuer Elements identifizieren.

Einige allgemeine Steuerelemente sind äußerst flexibel und können häufig durch weniger benutzerdefinierte Steuerelemente und vom Besitzer gezeichnete Steuerelemente ersetzt werden. Beispielsweise kann eine Listenansicht ein vom Besitzer gezeichnetes Listenfeld ersetzen, um ein Kontrollkästchen neben jedem Element anzuzeigen. Als weiteres Beispiel kann das Schaltflächen-Steuerelement "Erweitert" sowohl Bilder als auch Text anzeigen. Zuvor erforderte dies die Verwendung eines benutzerdefinierten Steuer Elements.

 

 



