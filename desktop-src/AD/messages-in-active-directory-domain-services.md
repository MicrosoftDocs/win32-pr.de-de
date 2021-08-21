---
title: Nachrichten in Active Directory Domain Services
description: Nachrichten in Active Directory Domain Services sind in Windows 2000 und Windows NT 4.0 mit Service Pack 6a (SP6a) und höher mit DSClient funktionsfähig.
ms.assetid: 32a4724b-3182-4521-975c-cef33afee0b2
ms.tgt_platform: multiple
keywords:
- Active Directory-Nachrichten AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b3f5a9a5e92048f64cc1b49ea67cae05443eda685d588df0c78bb3f48cf0dbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025918"
---
# <a name="messages-in-active-directory-domain-services"></a>Nachrichten in Active Directory Domain Services

Nachrichten in Active Directory Domain Services sind in Windows 2000 und Windows NT 4.0 mit Service Pack 6a (SP6a) und höher mit DSClient funktionsfähig. Sie sind auch auf Windows 98/95-Arbeitsstationen mit IE4.01 und höher und DSClient funktionsfähig. Wenn jedoch Eigenschaftenseiten mit mehrfacher Auswahl über die Shell gestartet werden, sind die [**WM \_ ADSPROP \_ NOTIFY \_ ERROR-Meldung**](wm-adsprop-notify-error.md) und die entsprechenden Hilfsfunktionen [**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) und [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) nicht funktionsfähig und werden nicht angezeigt. Wenn Eigenschaftenseiten mit mehrfacher Auswahl in einem Administratortool gestartet werden, z. B. AD-Benutzer und -Computer, sind alle Nachrichten funktionsfähig und können auf den Eigenschaftenseiten mit mehrfacher Auswahl angezeigt werden.

Active Directory Domain Services verwenden Sie die folgenden Meldungen:

-   [**WM \_ ADSPROP \_ NOTIFY \_ APPLY**](wm-adsprop-notify-apply.md)
-   [**WM \_ ADSPROP \_ NOTIFY \_ CHANGE**](wm-adsprop-notify-change.md)
-   [**WM \_ ADSPROP \_ NOTIFY \_ ERROR**](wm-adsprop-notify-error.md)
-   [**WM \_ ADSPROP \_ NOTIFY \_ EXIT**](wm-adsprop-notify-exit.md)
-   [**WM \_ ADSPROP \_ NOTIFY \_ FOREGROUND**](wm-adsprop-notify-foreground.md)
-   [**WM \_ ADSPROP \_ NOTIFY \_ PAGEHWND**](wm-adsprop-notify-pagehwnd.md)
-   [**WM \_ ADSPROP \_ NOTIFY \_ PAGEINIT**](wm-adsprop-notify-pageinit.md)
-   [**WM \_ ADSPROP \_ NOTIFY \_ SETFOCUS**](wm-adsprop-notify-setfocus.md)
-   [**WM \_ ADSPROP \_ SHEET \_ CREATE**](wm-adsprop-sheet-create.md)
-   [**WM \_ DSA \_ SHEET \_ CLOSE \_ NOTIFY**](wm-dsa-sheet-close-notify.md)
-   [**WM \_ DSA \_ SHEET \_ CREATE \_ NOTIFY**](wm-dsa-sheet-create-notify.md)

 

 




