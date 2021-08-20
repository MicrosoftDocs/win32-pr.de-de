---
description: ATM gilt sowohl für LAN- als auch für WAN-Umgebungen.
ms.assetid: 532a876c-9b31-410e-9331-5e8aa98ccaee
title: Winsock ATM-Anhang
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90f55c71b830fa8a5f27f083af0263c62766e7b037e433c04b73bfea5ba12960
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118822446"
---
# <a name="winsock-atm-annex"></a>Winsock ATM-Anhang

ATM gilt sowohl für LAN- als auch für WAN-Umgebungen. Ein ATM-Netzwerk transportiert gleichzeitig eine Vielzahl von Netzwerkdatenverkehr – Sprach-, Daten-, Bild- und Videodatenverkehr. Es bietet Benutzern eine garantierte Dienstqualität pro virtuellem Kanal (VC).



| Element          | Beschreibung                                                                                                                                                 |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Protokollnamen | ATMPROTO \_ AAL5, ATMPROTO \_ ADOMSER                                                                                                                           |
| Beschreibung      | ATM AAL5 bietet einen Transportdienst, der verbindungsorientiert ist, die Nachrichtengrenze beibehalten und QOS garantiert. ATMPROTO \_ ADOMSER ist eine benutzerdefinierte AAL. |
| Adressfamilie   | AF \_ ATM                                                                                                                                                     |
| Headerdatei      | Ws2atm.h                                                                                                                                                    |



 

In diesem Abschnitt werden die spezifischen Erweiterungen für den asynchronen Übertragungsmodus (Asynchronous Transfer Mode, ATM) beschrieben, die zur Unterstützung der nativen ATM-Dienste erforderlich sind, wie in der UNI-Spezifikation (ATM Forum User Network Interface) version 3.x (3.0 und 3.1) verfügbar gemacht und angegeben. Dieses Dokument unterstützt AAL-Typ 5 (Nachrichtenmodus) und benutzerdefinierte AAL. Zukünftige Versionen dieses Dokuments unterstützen andere AAL-Typen sowie UNI 4.0.

 

 



