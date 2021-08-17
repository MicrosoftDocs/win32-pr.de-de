---
title: Informationen zu IP-Adresssteuerelementen
description: Mit einem IP-Adresssteuersystem (InternetProtokoll) kann der Benutzer eine IP-Adresse in einem leicht verständlichen Format eingeben.
ms.assetid: cf6a59fc-661c-420a-a67f-a42619946357
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce537b3b3a92846961e95321889d106a61a81e14bfa4cbc4edd93da5c8c033ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435594"
---
# <a name="about-ip-address-controls"></a>Informationen zu IP-Adresssteuerelementen

Mit einem IP-Adresssteuersystem (InternetProtokoll) kann der Benutzer eine IP-Adresse in einem leicht verständlichen Format eingeben. Dieses Steuerelement ermöglicht es der Anwendung auch, die Adresse in numerischer Form und nicht in Textform zu erhalten.

-   [Informationen zu IP-Adresssteuerelementen](#about-ip-address-controls)
-   [Erstellen eines IP-Adresssteuer steuerelements](#creating-an-ip-address-control)
-   [Ist ein IP-Adresssteuer steuerelement ein Bearbeitungssteuer steuerelement?](#is-an-ip-address-control-an-edit-control)

## <a name="about-ip-address-controls"></a>Informationen zu IP-Adresssteuerelementen

Windows Internet Explorer Version 4.0 führt das IP-Adresssteuersystem ein, ein neues Steuerelement, das einem Bearbeitungssteuerwert ähnelt, mit dem der Benutzer eine numerische Adresse im IP-Format (Internetprotokoll) eingeben kann. Dieses Format besteht aus vier dreistelligen Feldern. Jedes Feld wird einzeln behandelt. Die Feldnummern sind nullbasierte Und fahren von links nach rechts fort, wie in dieser Abbildung dargestellt.

![Diagramm mit Werten in jedem der vier Felder eines IP-Adresssteuerfelds](images/ipa-scrn.png)

Mit dem -Steuerelement kann nur numerischer Text in jedes der Felder eingegeben werden. Nachdem drei Ziffern in ein bestimmtes Feld eingegeben wurden, wird der Tastaturfokus automatisch in das nächste Feld verschoben. Wenn die Anwendung das gesamte Feld nicht ausfüllen muss, kann der Benutzer weniger als drei Ziffern eingeben. Wenn das Feld z. B. nur die Zahl 21 enthalten soll, wird der Benutzer durch Eingeben von "21" und Drücken der Taste zum nächsten Feld.

Der Standardbereich für jedes Feld ist 0 bis 255, aber die Anwendung kann den Bereich mit der [**IPM \_ SETRANGE-Nachricht**](ipm-setrange.md) auf beliebige Werte zwischen diesen Grenzwerten festlegen.

> [!Note]  
> Die IP-Adresssteuerung ist in Version 4.71 und höher von Comctl32.dll.

 

## <a name="creating-an-ip-address-control"></a>Erstellen eines IP-Adresssteuer steuerelements

Rufen Sie vor dem Erstellen eines IP-Adresssteuerzeichens [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) auf, und legen Sie dabei das **FLAG FÜR \_ \_ INTERNETKLASSEN VON INTERNET AUF,** das im **dwICC-Member** der [**INITCOMMONCONTROLSEX-Struktur festgelegt**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) ist.

Verwenden Sie [**die Funktion CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) oder [**CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) um ein IP-Adresssteuer steuerelement zu erstellen. Der Klassenname für das Steuerelement ist [**WC \_ IPADDRESS,**](common-control-window-classes.md)der in Commctrl.h definiert ist. Es sind keine ipadressensteuersteuerspezifischen Stile vorhanden. Da es sich jedoch um ein untergeordnetes Steuerelement handelt, verwenden Sie mindestens [**den WS \_ CHILD-Stil.**](/windows/desktop/winmsg/window-styles)

## <a name="is-an-ip-address-control-an-edit-control"></a>Ist ein IP-Adresssteuer steuerelement ein Bearbeitungssteuer steuerelement?

Ein IP-Adresssteuer steuerelement ist kein Bearbeitungssteuer steuerelement und reagiert nicht auf \_ EM-Nachrichten. Sie sendet jedoch die folgenden Bearbeitungssteuerungsbenachrichtigungen über die [**WM \_ COMMAND-Meldung**](/windows/desktop/menurc/wm-command) an das Besitzerfenster. Beachten Sie, dass das IP-Adresssteuersystem auch private IPN-Benachrichtigungen über \_ die [**WM \_ NOTIFY-Nachricht**](wm-notify.md) sendet.



|     Benachrichtigung                              |     Grund für die Benachrichtigung                                                                                                                                                                                                    |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [EN \_ SETFOCUS](en-setfocus.md)   | Wird gesendet, wenn das IP-Adresssteuer steuerelement den Tastaturfokus erhält.                                                                                                                                              |
| [EN \_ KILLFOCUS](en-killfocus.md) | Wird gesendet, wenn das IP-Adresssteuer steuerelement den Tastaturfokus verliert.                                                                                                                                              |
| [EN \_ CHANGE](en-change.md)       | Wird gesendet, wenn sich ein Feld im IP-Adresssteuerfeld ändert. Wie bei [der EN \_ CHANGE-Benachrichtigung](en-change.md) von einem Standardbearbeitungssteuer steuerelement wird diese Benachrichtigung empfangen, nachdem der Bildschirm aktualisiert wurde. |



 

 

 