---
title: Treibermeldungen
description: Treibermeldungen
ms.assetid: ed3748ac-08e6-418e-b345-30c796fa38f3
keywords:
- Installierbare Treiber, Meldungen
- Installierbare Treiber, benutzerdefinierte Meldungen
- Treibermeldungen
- Benutzerdefinierte Treibermeldungen
- Installierbare Treiber, DriverProc-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9fb6c741cf782f620d9234f431a248fb47a8362ddcd55cf84205d8faee5800
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526330"
---
# <a name="driver-messages"></a>Treibermeldungen

Jede Treibernachricht besteht aus einem Nachrichtenbezeichner und zwei 32-Bit-Parametern. Der Nachrichtenbezeichner ist ein eindeutiger Wert, den die [DriverProc-Funktion](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) überprüft, um zu bestimmen, welche Aktion durchgeführt werden soll. Die Bedeutung der Nachrichtenparameter hängt von der Nachricht ab. Die Parameter können Werte oder Adressen darstellen. In vielen Fällen werden die Parameter nicht verwendet und auf 0 (null) festgelegt.

Treibermeldungen können standard- oder benutzerdefiniert sein. Windows sendet Standardtreibermeldungen wie [**DRV \_ OPEN,**](drv-open.md) [**DRV \_ CLOSE**](drv-close.md)und [**DRV \_ CONFIGURE**](drv-configure.md)als Antwort auf eine Anforderung zum Öffnen, Schließen oder Konfigurieren des Treibers an einen installierbaren Treiber. Die Standardmeldungen führen den installierbaren Treiber an, seine Ressourcen zu laden oder zu entladen, den Betrieb zu aktivieren oder zu deaktivieren, eine Treiberinstanz zu öffnen oder zu schließen und ein Konfigurationsdialogfeld anzuzeigen. Einige Standardmeldungen wie [**DRV \_ POWER**](drv-power.md) und [**DRV \_ EXITSESSION**](drv-exitsession.md)benachrichtigen den Treiber über systemweite Ereignisse, die sich auf den Betrieb des Treibers oder einer zugehörigen Hardware auswirken.

Anwendungen und DLLs senden benutzerdefinierte Treibermeldungen, um einen installierbaren Treiber an die Durchführung treiberspezifischer Aktionen zu richten. Installierbare Treiber, die benutzerdefinierte Nachrichten unterstützen, müssen eine entsprechende Verarbeitung in der **DriverProc-Funktion** enthalten. Um Konflikte zwischen benutzerdefinierten und Standardtreibermeldungen zu vermeiden, müssen benutzerdefinierte Nachrichtenbezeichner Werte im Bereich von DRV \_ RESERVED bis DRV \_ USER haben. Benutzerdefinierte Nachrichten, die an [die DefDriverProc-Funktion](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) übergeben werden, werden ignoriert.

 

 