---
description: Beschreibung der Verwendung von Customer-Steuerelementen für den Tablet PC.
ms.assetid: 43d78acd-1f02-417d-97be-1682e90a81a2
title: Verwenden benutzerdefinierter Steuerelemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c713d2b3912d2bbe4a689c7d8d05d4d977a6eb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862495"
---
# <a name="using-custom-controls"></a>Verwenden benutzerdefinierter Steuerelemente

Sie können Standard Steuerelemente anpassen, indem Sie die Besitzer Zeichnung verwenden, um die Darstellung des Steuer Elements zu ändern und eine übergeordnete Klasse oder eine Unterklasse zum Ändern des Verhaltens des Steuer Elements einzurichten. In jedem Fall verarbeitet der zugrunde liegende Systemcode für den Standard Steuerungstyp grundlegende Steuerungsfunktionen. Die meisten dieser Steuerelemente können aufgerufen werden, wenn Sie sie ordnungsgemäß verwenden.

Ein vom Besitzer gezeichnetes Steuerelement, das auf einem Standard Steuerelement basiert, wird als Standard Steuerelement für Barrierefreiheits Hilfen angezeigt und unterstützt Microsoft Active Accessibility; Es verfügt jedoch über eine angepasste Darstellung. Einige Anwendungen verwenden benutzerdefinierte Steuerelemente, um die Darstellung eines Steuer Elements zu ändern, aber Besitzer gezeichnete Steuerelemente sind eine besser zugängliche Lösung. Weitere Informationen zum Definieren von von einem Besitzer gezeichneten Menüs und zum verfügbar machen von Steuerelementen, die vom Besitzer gezeichnet werden, finden Sie unter [Barrierefreiheit](../accessibility/accessibility.md)

Das Einrichten einer übergeordneten Klasse oder Unterklasse ist eine Technik zum Anpassen des Verhaltens vorhandener Steuerelemente. Abhängig vom neuen Verhalten des Steuer Elements ist es möglicherweise erforderlich, die von ihm verfügbar gemachten Barrierefreiheits Informationen zu ergänzen. Beispielsweise kann eine Anwendung ein vom Besitzer gezeichnetes Steuerelement verwenden, um ein X in einem ausgewählten Kontrollkästchen anstelle eines Häkchens anzuzeigen, oder um eine Befehls Schaltfläche mit einem Bild anstelle eines Worts zu versehen.

Wenn Sie von einem Besitzer gezeichnete Steuerelemente verwenden, die entweder eine übergeordnete Klasse oder eine Unterklasse sind:

-   Stellen Sie Bezeichnungen für alle Steuerelemente bereit, selbst wenn die Bezeichnungen auf dem Bildschirm nicht sichtbar sind. Wenn Sie ein Steuerelement so anpassen, dass die Standard Beschriftung nicht sichtbar (z. b. eine Schaltfläche mit einem Grafik Gesicht) ist, und die Beschriftung als leere Zeichenfolge belassen, kann die Hilfe zur Barrierefreiheit die Beschriftung nicht erhalten und zum Identifizieren des Steuer Elements verwenden.
-   Stellen Sie sicher, dass [**WM \_ gettext**](../winmsg/wm-gettext.md) unterstützt wird.
-   Stellen Sie sicher, dass alle klassenspezifischen Meldungen unterstützt werden. Es ist besonders wichtig, Text Abruf Nachrichten wie [**CB \_ getlbtext**](../controls/cb-getlbtext.md) und [**lb \_ gettext**](../controls/lb-gettext.md)zu unterstützen. Legen Sie die entsprechenden stilbits wie z. b. **CBS \_ hasstrings** und **lbs \_ hasstrings** fest, um anzugeben, dass das Steuerelement diese Nachrichten unterstützt.

 

 
