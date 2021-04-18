---
title: Nachrichten in Active Directory Domain Services
description: Nachrichten in Active Directory Domain Services sind in Windows 2000 und Windows NT 4,0 mit Service Pack 6a (SP6a) und höher mit DSClient funktionsfähig.
ms.assetid: 32a4724b-3182-4521-975c-cef33afee0b2
ms.tgt_platform: multiple
keywords:
- Active Directory Meldungen anzeigen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6895aee711af04778318cf42920d0b0416725205
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340408"
---
# <a name="messages-in-active-directory-domain-services"></a>Nachrichten in Active Directory Domain Services

Nachrichten in Active Directory Domain Services sind in Windows 2000 und Windows NT 4,0 mit Service Pack 6a (SP6a) und höher mit DSClient funktionsfähig. Sie sind auch in Windows 98/95-Arbeitsstationen mit IE 4.01 und höher und DSClient funktionsfähig. Wenn jedoch Mehrfachauswahl-Eigenschaften Seiten von der Shell aus gestartet werden, sind die Fehlermeldung " [**WM \_ adsprop \_ Notify \_ Error**](wm-adsprop-notify-error.md) " und die zugehörigen Hilfsfunktionen " [**adspropsenderrormessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) " und " [**adspropshowerrordialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) " nicht funktionsfähig und werden nicht angezeigt. Wenn Mehrfachauswahl-Eigenschaften Seiten innerhalb eines Verwaltungs Tools (z. b. AD-Benutzer und-Computer) gestartet werden, sind alle Meldungen funktionsfähig und verfügbar, die auf den Mehrfachauswahl-Eigenschaften Seiten angezeigt werden können.

Active Directory Domain Services die folgenden Meldungen verwenden:

-   [**WM- \_ adsprop- \_ Benachrichtigung \_ anwenden**](wm-adsprop-notify-apply.md)
-   [**WM- \_ adsprop- \_ Benachrichtigungs \_ Änderung**](wm-adsprop-notify-change.md)
-   [**WM- \_ adsprop- \_ Benachrichtigungs \_ Fehler**](wm-adsprop-notify-error.md)
-   [**WM- \_ adsprop \_ Benachrichtigen \_ Beenden**](wm-adsprop-notify-exit.md)
-   [**WM- \_ adsprop- \_ Benachrichtigungs \_ Vordergrund**](wm-adsprop-notify-foreground.md)
-   [**WM \_ adsprop- \_ Benachrichtigungs \_ paar Benachrichtigen**](wm-adsprop-notify-pagehwnd.md)
-   [**WM \_ adsprop \_ benachrichtigt \_ pageingeit**](wm-adsprop-notify-pageinit.md)
-   [**WM \_ adsprop \_ Benachrichtigen von \_ SetFocus**](wm-adsprop-notify-setfocus.md)
-   [**WM- \_ adsprop- \_ Blatt \_ Erstellen**](wm-adsprop-sheet-create.md)
-   [**WM- \_ DSA- \_ Blatt " \_ Schließen \_ "**](wm-dsa-sheet-close-notify.md)
-   [**WM \_ - \_ Blatt "DSA \_ Erstellen \_ "**](wm-dsa-sheet-create-notify.md)

 

 




