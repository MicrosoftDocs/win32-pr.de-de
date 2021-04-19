---
description: TAPI 3,1 führt com-basierte Telefon Steuerelemente ein. Es wird davon ausgegangen, dass Sie sich mit com, OLE-Automatisierung und Skripterstellung vertraut machen, ebenso wie das TAPI 3-Objektmodell. Kenntnisse der TAPI 2-Telefon Steuerungsfunktionen sind ebenfalls hilfreich.
ms.assetid: e56aef54-e358-429b-9f0f-c8776507d95f
title: Telefon Steuerung und Telefon Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e9344d54a63efcf1692af361a5f8e88121981e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356660"
---
# <a name="phone-control-and-the-phone-object"></a>Telefon Steuerung und Telefon Objekt

TAPI 3,1 führt com-basierte Telefon Steuerelemente ein. Es wird davon ausgegangen, dass Sie sich mit com, OLE-Automatisierung und Skripterstellung vertraut machen, ebenso wie das TAPI 3-Objektmodell. Kenntnisse der TAPI 2-Telefon Steuerungsfunktionen sind ebenfalls hilfreich.

Die Telefon Steuerung ist auf drei Ebenen von Features implementiert, von denen jede auf der vorherigen basiert:

-   Phone-Objekt. Die erste Ebene definiert, wie die Telefongeräte von TAPI 2. x (APIs, Konstanten und Nachrichten, die mit "Phone" beginnen) im TAPI 3,1-Objektmodell verfügbar gemacht werden. Dies umfasst ein neues Telefon Objekt, das von TAPI 3,1 verfügbar gemacht wird, wobei [**itphone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone) als Standardschnittstelle für das neue Objekt verfügbar ist. Die **itphone** -Schnittstelle, zusammen mit den zugehörigen Konstanten, Enumerationstypen und Ereignissen, macht in der Regel dieselbe Detail-und Funktionsebene verfügbar wie die TAPI 2. x-Funktionen, Konstanten, Strukturen und Nachrichten, die mit dem Wort "Phone" beginnen. Diese Ebene umfasst auch neue Schnittstellen für mehrere vorhandene TAPI 3. x-Objekte, um die Erstellung von Telefon Objekten und die Zuordnung von Telefon Objekten zu anderen Objekten, auf die Sie bezogen sind, zu vereinfachen.
-   Automatisierte Telefon Steuerung und Anruf Behandlung. Die zweite Ebene besteht aus einer zusätzlichen Schnittstelle mit dem Namen [**itautomatedphonecontrol**](/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol) und den zugehörigen Konstanten, enumerierten Typen und Ereignissen. Dies ist eine sekundäre Schnittstelle auf dem Telefon Objekt. Wenn das Telefongerät mit der Berechtigung "Besitzer" geöffnet wurde, verwenden Sie die **QueryInterface** -Methode auf der [**itphone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone) -Schnittstelle, um einen **itautomatedphonecontrol** -Schnittstellen Zeiger zu erhalten.
-   Windows 2000 Phone-Dialer. Die dritte Ebene besteht aus Änderungen an der Windows 2000 Phone Dialer-Anwendung, um bestimmte Benutzerinteraktionen zu implementieren.

Entwickler von Microsoft oder Drittanbietern können das TAPI 3,1-Objektmodell verwenden, um erweiterte Anwendungen oder Dienste mit Telefonen zu implementieren, einschließlich eines Diensts, der USB-Handsets (Universal Serial Bus) zum Beispiel für Telefonanrufe ermöglicht, auch wenn kein Benutzer angemeldet ist und keine andere TAPI-Anwendung explizit gestartet wurde.

In TAPI 3,0 hat ein Telefon-MSP versucht, Telefongeräte zu verbessern, die Zeilen zugeordnet sind, die für TAPI 3,0-Anrufe verwendet werden Diese Entwicklung ist für die Unterstützung von Modems mit Software umsetzbaren Speakers vorgesehen. TAPI 3,1-Anwendungen, die diesen Modem-Typ verwenden, sollten die TAPI 3,1 Phone-Objekte verwenden, um den Status des Modem-huokswitches zu ändern.

Weitere Informationen und eine Liste aller dem Telefon Objekt zugeordneten Schnittstellen finden Sie unter [Telefon Objekt Schnittstellen](phone-object-interfaces.md). Die Telefon Steuerungs Schnittstellen machen Methoden verfügbar, die die Steuerung von Telefon Sätzen mithilfe von com ermöglichen.

 

 



