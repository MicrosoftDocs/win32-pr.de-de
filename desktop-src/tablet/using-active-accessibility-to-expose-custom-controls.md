---
description: Beschreibung der Verwendung der aktiven Barrierefreiheit, um benutzerdefinierte Steuerelemente für den Tablet-PC verfügbar zu machen.
ms.assetid: 1557bde2-c382-4259-ae0c-a70902fa91bd
title: Verwenden Active Accessibility zum Verfügbar machen von benutzerdefinierten Steuerelementen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d275b6c5639dddfe60f358427751ad4ff4cd7989923dc4a368b3316b3bfc01e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934320"
---
# <a name="using-active-accessibility-to-expose-custom-controls"></a>Verwenden Active Accessibility zum Verfügbar machen von benutzerdefinierten Steuerelementen

Sie können Microsoft Active Accessibility effektive Methode verwenden, um benutzerdefinierte Steuerelemente mit Barrierefreiheitshilfen kompatibel zu machen. Active Accessibility erfordert, dass die Anwendung:

-   Erstellen Component Object Model (COM)-Objekte, die einzelne benutzerdefinierte Steuerelemente oder Gruppen von Steuerelementen darstellen, die die **IAccessible-Schnittstelle ordnungsgemäß** unterstützen. (Das Objekt kann bei Bedarf erstellt werden, wenn es von einem Active Accessibility wird.)
-   Rufen [**Sie NotifyWinEvent**](/windows/win32/api/winuser/nf-winuser-notifywinevent) auf, wenn die Steuerelemente erstellt oder zerstört werden, den Fokus erhalten oder verlieren oder den Zustand anderweitig ändern.
-   Behandeln Sie die WM \_ GETOBJECT-Nachricht, wenn sie zum Abfragen von Eigenschaften des Objekts oder der Objekte verwendet wird.

Im Rahmen dieser Diskussion muss auch ein Fenster mit anderen benutzerdefinierten Objekten für Active Accessibility verfügbar gemacht werden, sodass der Client die untergeordneten Objekte finden und zu diesen navigieren kann. Weitere Informationen dazu, wie benutzerdefinierte Steuerelemente mit Barrierefreiheitshilfen kompatibel sind, finden Sie unter [Barrierefreiheit.](../accessibility/accessibility.md)

 

 
