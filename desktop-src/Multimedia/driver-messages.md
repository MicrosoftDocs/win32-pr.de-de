---
title: Treiber Meldungen
description: Treiber Meldungen
ms.assetid: ed3748ac-08e6-418e-b345-30c796fa38f3
keywords:
- installierbare Treiber, Meldungen
- installierbare Treiber, benutzerdefinierte Meldungen
- Treiber Meldungen
- benutzerdefinierte Treiber Meldungen
- installierbare Treiber, driverproc-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25e03f9d68254752655be8abe9040a17d44dc0ff
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038854"
---
# <a name="driver-messages"></a>Treiber Meldungen

Jede Treiber Meldung besteht aus einem Nachrichten Bezeichner und 2 32-Bit-Parametern. Der Nachrichten Bezeichner ist ein eindeutiger Wert, den die [driverproc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) -Funktion prüft, um zu bestimmen, welche Aktion ausgeführt werden soll. Die Bedeutung der Nachrichten Parameter hängt von der Nachricht ab. Die Parameter können Werte oder Adressen darstellen. In vielen Fällen werden die Parameter nicht verwendet und auf 0 (null) festgelegt.

Treiber Nachrichten können Standard oder Benutzer definiert sein. Windows sendet Standardtreiber Nachrichten wie z. b. [**drv \_ Open**](drv-open.md), [**drv \_ Close**](drv-close.md)und [**drv \_ configure**](drv-configure.md)an einen installierbaren Treiber als Reaktion auf eine Anforderung zum Öffnen, schließen oder Konfigurieren des Treibers. Die Standard Meldungen leiten den installierbaren Treiber an, seine Ressourcen zu laden oder zu entladen, den Vorgang zu aktivieren oder zu deaktivieren, eine Treiber Instanz zu öffnen oder zu schließen und ein Konfigurations Dialogfeld anzuzeigen. Einige Standard Meldungen, wie z. b. [**drv \_ Power**](drv-power.md) und [**drv \_ exitsession**](drv-exitsession.md), benachrichtigen den Treiber über systemweite Ereignisse, die sich auf den Betrieb des Treibers oder auf zugehörige Hardware auswirken.

Anwendungen und DLLs senden benutzerdefinierte Treiber Nachrichten, um einen installierbaren Treiber zum Ausführen von treiberspezifischen Aktionen zu leiten. Installierbare Treiber, die benutzerdefinierte Nachrichten unterstützen, müssen die entsprechende Verarbeitung in der **driverproc** -Funktion einschließen Zur Vermeidung von Konflikten zwischen benutzerdefinierten und Standardtreiber Nachrichten müssen benutzerdefinierte Meldungs-IDs Werte aufweisen, die von \_ dem für den drv-Benutzer reservierten drv reichen \_ . An die [defdriverproc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) -Funktion übergebene benutzerdefinierte Nachrichten werden ignoriert.

 

 