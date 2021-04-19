---
description: ATM ist für LAN-und WAN-Umgebungen anwendbar.
ms.assetid: 532a876c-9b31-410e-9331-5e8aa98ccaee
title: Winsock ATM-Anhang
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63ec056cc2b84c9449ed466a60a15683df29744b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356567"
---
# <a name="winsock-atm-annex"></a>Winsock ATM-Anhang

ATM ist für LAN-und WAN-Umgebungen anwendbar. Ein ATM-Netzwerk transportiert gleichzeitig eine Vielzahl von Netzwerk Datenverkehr – sprach-, Daten-, Bild-und Videodaten. Der Benutzer erhält eine garantierte Quality of Service-Qualität auf Basis eines virtuellen Kanals (VC).



| Element          | BESCHREIBUNG                                                                                                                                                 |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Protokoll Name (n) | Atmproto \_ AAL5, atmproto \_ aaluser                                                                                                                           |
| BESCHREIBUNG      | ATM AAL5 stellt einen Transportdienst bereit, der verbindungsorientiert, Nachrichten Begrenzung beibehalten und QoS garantiert ist. Atmproto \_ aaluser ist eine benutzerdefinierte Aal-Datei. |
| Adressfamilie   | AF- \_ ATM                                                                                                                                                     |
| Headerdatei      | Ws2atm. h                                                                                                                                                    |



 

In diesem Abschnitt werden die Anforderungen für den asynchronen Übertragungsmodus (ATM) beschrieben, die zur Unterstützung der systemeigenen ATM-Dienste erforderlich sind, die verfügbar sind und in der Spezifikation für die Benutzer Netzwerkschnittstelle (Uni), Version 3. x (3,0 und 3,1) des ATM-Forums In diesem Dokument werden Aal-Typ 5 (Nachrichten Modus) und benutzerdefinierte Aal unterstützt. In zukünftigen Versionen dieses Dokuments werden andere Arten von Aal und Uni 4,0 unterstützt.

 

 



