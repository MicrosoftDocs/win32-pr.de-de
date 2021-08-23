---
description: Beschreibung der Verwendung von Kundensteuerelementen für den Tablet PC.
ms.assetid: 43d78acd-1f02-417d-97be-1682e90a81a2
title: Verwenden von benutzerdefinierten Steuerelementen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70699a141f0319f917953e25363db0e0cd38eb21ecc06345c581b55526ad6bbb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119551880"
---
# <a name="using-custom-controls"></a>Verwenden von benutzerdefinierten Steuerelementen

Sie können Standardsteuerelemente anpassen, indem Sie das Besitzerzeichnungs-Steuerelement verwenden, um die Darstellung des Steuerelements zu ändern, und eine Ober- oder Unterklasse einrichten, um das Verhalten des Steuerelements zu ändern. In jedem Fall verarbeitet der zugrunde liegende Systemcode für den Standardsteuerelementtyp grundlegende Steuerungsfunktionen. Auf die meisten dieser Steuerelemente kann zugegriffen werden, wenn Sie sie ordnungsgemäß verwenden.

Ein vom Besitzer gezeichnetes Steuerelement, das auf einem Standardsteuerelement basiert, wird als Standardsteuerelement für Barrierefreiheitshilfen angezeigt und unterstützt Microsoft Active Accessibility. verfügt jedoch über eine angepasste Darstellung. Einige Anwendungen verwenden benutzerdefinierte Steuerelemente, um die Darstellung eines Steuerelements zu ändern, aber vom Besitzer gezeichnete Steuerelemente sind eine besser zugängliche Lösung. Weitere Informationen zum Definieren von vom Besitzer gezeichneten Menüs und zum Verfügbar machen von Besitzern gezeichneter Steuerelemente finden Sie unter [Barrierefreiheit.](../accessibility/accessibility.md)

Das Einrichten einer Übergeordneten Klasse oder Unterklasse ist eine Technik zum Anpassen des Verhaltens vorhandener Steuerelemente. Abhängig vom neuen Verhalten des Steuerelements kann es erforderlich sein, die verfügbar gemachten Barrierefreiheitsinformationen zu ergänzen. Beispielsweise kann eine Anwendung ein vom Besitzer gezeichnetes Steuerelement verwenden, um ein X in einem ausgewählten Kontrollkästchen anstelle eines Häkchens anzuzeigen, oder eine Befehlsschaltfläche mit einem Bild statt mit einem Wort zu bezeichnen.

Bei Verwendung von besitzergezeichneten Steuerelementen, die entweder eine Oberklasse oder eine Unterklasse sind:

-   Stellen Sie Bezeichnungen für alle Steuerelemente bereit, auch wenn die Bezeichnungen auf dem Bildschirm nicht sichtbar sind. Wenn Sie ein Steuerelement so anpassen, dass die Standardbeschriftung nicht sichtbar ist (z. B. eine Schaltfläche mit grafischer Darstellung), und die Beschriftung als leere Zeichenfolge belassen, kann die Barrierefreiheitshilfe die Beschriftung nicht abrufen und zum Identifizieren des Steuerelements verwenden.
-   Stellen Sie sicher, dass [**WM \_ GETTEXT**](../winmsg/wm-gettext.md) unterstützt wird.
-   Stellen Sie sicher, dass alle klassenspezifischen Nachrichten unterstützt werden. Es ist besonders wichtig, Textabrufnachrichten wie [**CB \_ GETLBTEXT**](../controls/cb-getlbtext.md) und [**LB \_ GETTEXT**](../controls/lb-gettext.md)zu unterstützen. Legen Sie die entsprechenden Stilbits wie **CBS \_ HASSTRINGS** und **LBS \_ HASSTRINGS** fest, um anzugeben, dass das Steuerelement diese Nachrichten unterstützt.

 

 
