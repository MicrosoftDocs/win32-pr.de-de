---
title: Informationen zu IP-Adress Steuerelementen
description: Ein IP-Adress Steuerelement (Internet Protocol) ermöglicht es dem Benutzer, eine IP-Adresse in einem leicht verständlichen Format einzugeben.
ms.assetid: cf6a59fc-661c-420a-a67f-a42619946357
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb8cf39400c97d211d83b5496067fe6d4772e1e7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949146"
---
# <a name="about-ip-address-controls"></a>Informationen zu IP-Adress Steuerelementen

Ein IP-Adress Steuerelement (Internet Protocol) ermöglicht es dem Benutzer, eine IP-Adresse in einem leicht verständlichen Format einzugeben. Dieses Steuerelement ermöglicht der Anwendung auch das Abrufen der Adresse in numerischer Form und nicht in Textform.

-   [Informationen zu IP-Adress Steuerelementen](#about-ip-address-controls)
-   [Erstellen eines IP-Adress Steuer Elements](#creating-an-ip-address-control)
-   [Ist ein Steuerelement für die IP-Adresse ein Bearbeitungs Steuerelement?](#is-an-ip-address-control-an-edit-control)

## <a name="about-ip-address-controls"></a>Informationen zu IP-Adress Steuerelementen

In Windows Internet Explorer Version 4,0 wird das IP-Adress Steuerelement eingeführt, ein neues Steuerelement, das einem Bearbeitungs Steuerelement ähnelt, mit dem der Benutzer eine numerische Adresse im IP-Format (Internet Protocol) eingeben kann. Dieses Format besteht aus 4 3-stelligen Feldern. Jedes Feld wird einzeln behandelt. die Feldnummern sind NULL basiert und werden von links nach rechts fortgesetzt, wie in dieser Abbildung dargestellt.

![Diagramm, das die Werte in jedem der vier Felder eines IP-Adress Steuer Elements anzeigt](images/ipa-scrn.png)

Mit dem-Steuerelement kann in jedem der Felder nur numerischer Text eingegeben werden. Nachdem drei Ziffern in ein bestimmtes Feld eingegeben wurden, wird der Tastaturfokus automatisch in das nächste Feld verschoben. Wenn das Ausfüllen des gesamten Felds für die Anwendung nicht erforderlich ist, kann der Benutzer weniger als drei Ziffern eingeben. Wenn das Feld z. b. nur die Zahl Twenty-One enthalten soll, geben Sie "21" ein, und drücken Sie die Taste, um den Benutzer zum nächsten Feld zu gelangen.

Der Standardbereich für jedes Feld liegt zwischen 0 und 255, aber die Anwendung kann den Bereich für alle Werte zwischen diesen Grenzwerten mit der [**IPM- \_ SetRange**](ipm-setrange.md) -Nachricht festlegen.

> [!Note]  
> Das IP-Adress Steuerelement wird in Version 4,71 und höher von Comctl32.dll implementiert.

 

## <a name="creating-an-ip-address-control"></a>Erstellen eines IP-Adress Steuer Elements

Bevor Sie ein IP-Adress Steuerelement erstellen, müssen Sie [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) mit dem im **dwicc** -Member der [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) -Struktur festgelegten Flag " **ICC \_ Internet \_ Classes** " anrufen.

Verwenden Sie die Funktion "up [**Window**](/windows/desktop/api/winuser/nf-winuser-createwindowa) " oder " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ", um ein IP-Adress Steuerelement zu erstellen. Der Klassenname für das-Steuerelement ist eine [**WC- \_ IP-Adresse**](common-control-window-classes.md), die in "kommctrl. h" definiert ist. Es sind keine IP-Adress Steuerungs spezifischen Stile vorhanden. Da es sich hierbei jedoch um ein untergeordnetes Steuerelement handelt, verwenden Sie den untergeordneten [**WS \_**](/windows/desktop/winmsg/window-styles) -Stil als Minimalwert.

## <a name="is-an-ip-address-control-an-edit-control"></a>Ist ein Steuerelement für die IP-Adresse ein Bearbeitungs Steuerelement?

Ein IP-Adress Steuerelement ist kein Bearbeitungs Steuerelement und antwortet nicht auf EM- \_ Meldungen. Das Besitzer Fenster wird jedoch über die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung mit den folgenden Bearbeitungs Steuerelement-Benachrichtigungen gesendet. Beachten Sie, dass das IP-Adress Steuerelement auch private IPN- \_ Benachrichtigungen über die [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldung sendet.



|                                   |                                                                                                                                                                                                         |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Benachrichtigung**                  | **Grund für Benachrichtigung**                                                                                                                                                                             |
| [EN \_ SetFocus](en-setfocus.md)   | Wird gesendet, wenn die IP-Adress Steuerung den Tastaturfokus erhält.                                                                                                                                              |
| [EN \_ killfokus](en-killfocus.md) | Wird gesendet, wenn das IP-Adress Steuerelement den Tastaturfokus verliert.                                                                                                                                              |
| [\_Änderung der Änderung](en-change.md)       | Wird gesendet, wenn ein Feld im IP-Adress Steuerelement geändert wird. Wie bei [der \_ Änderung der en-Änderung](en-change.md) von einem Standard-Bearbeitungs Steuerelement wird diese Benachrichtigung empfangen, nachdem der Bildschirm aktualisiert wurde. |



 

 

 