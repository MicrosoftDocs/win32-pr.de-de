---
description: Beschreibung der Verwendung von aktivem Zugriff, um benutzerdefinierte Steuerelemente für den Tablet PC verfügbar zu machen.
ms.assetid: 1557bde2-c382-4259-ae0c-a70902fa91bd
title: Verwenden von Active Accessibility zur Bereitstellung benutzerdefinierter Steuerelemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d33d4c2b57a881cfbdc15f14e71e339ed7f9e84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345695"
---
# <a name="using-active-accessibility-to-expose-custom-controls"></a>Verwenden von Active Accessibility zur Bereitstellung benutzerdefinierter Steuerelemente

Sie können Microsoft Active Accessibility als effektive Methode verwenden, um benutzerdefinierte Steuerelemente mit Barrierefreiheits Hilfen kompatibel zu machen. Active Accessibility erfordert, dass die Anwendung:

-   Erstellen Sie Component Object Model (com)-Objekte, die einzelne benutzerdefinierte Steuerelemente oder Gruppen von Steuerelementen darstellen, die die Schnittstelle **IAccessible** ordnungsgemäß unterstützen (Das Objekt kann Bedarfs gesteuert erstellt werden, wenn es von einem Active Accessibility-Client angefordert wird.)
-   Ruft [**NotifyWinEvent**](/windows/win32/api/winuser/nf-winuser-notifywinevent) auf, wenn die Steuerelemente erstellt oder zerstört werden, der Fokus erhalten oder verloren geht oder andernfalls der Status geändert wird.
-   Behandeln Sie die WM- \_ GetObject-Nachricht, wenn Sie zum Abfragen der Eigenschaften des Objekts oder der Objekte verwendet wird.

Im Rahmen dieser Diskussion muss ein Fenster, das andere benutzerdefinierte Objekte enthält, auch für Active Accessibility verfügbar gemacht werden, sodass der Client die untergeordneten Objekte ermitteln und zu diesen navigieren kann. Weitere Informationen dazu, wie Sie benutzerdefinierte Steuerelemente mit Barrierefreiheits Hilfen kompatibel machen, finden Sie unter [Barrierefreiheit](../accessibility/accessibility.md).

 

 
