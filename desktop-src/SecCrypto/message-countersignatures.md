---
description: Manchmal erfordert eine signierte Nachricht eine Gegensignatur.
ms.assetid: de83a9ad-4e88-4477-8c9e-6dd7d5ec9e8f
title: Nachrichten-Gegensignaturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d95f9d082a2814501bdb948d1bfebdc5c2699012446c5189c5c3fc18612c1ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080640"
---
# <a name="message-countersignatures"></a>Nachrichten-Gegensignaturen

Manchmal erfordert eine signierte Nachricht [*eine Gegensignatur.*](../secgloss/c-gly.md) Beispielsweise kann Benutzer A eine signierte Datennachricht an Benutzer B senden und erwartet, dass B die Zustimmung zu den im Dokument enthaltenen Bedingungen bestätigt. Benutzer B decodiert die Nachricht, liest die Bedingungen und signiert die Nachricht, sofern dies zu einer Vereinbarung kommt, gegen. Die gegensignierte Nachricht wird dann an Benutzer A zurücksandt. Benutzer A weiß jetzt und kann nachweisen, dass Benutzer B den Bedingungen zugestimmt hat.

In der folgenden Tabelle sind Abschnitte aufgeführt, die Prozedurbeschreibungen oder C-Programmbeispiele für die Gegensignierung von Nachrichten enthalten.



| `Section`                                                                                                                                 | Contents                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Nachrichtenfunktionen](cryptography-functions.md)                                                                       | Listet die Zählersignaturfunktionen auf.                             |
| [Gegensignieren einer Nachricht](countersigning-a-message.md)                                                                                | Details zum Prozess der Gegensignierung einer Nachricht.                  |
| [Überprüfen einer Gegensignatur](verifying-a-countersignature.md)                                                                        | Hier erfahren Sie, wie Sie eine Zählersignatur überprüfen.           |
| [Überprüfen einer signierten Nachricht](verifying-a-signed-message.md)                                                                            | Gibt einen Prozess zum Überprüfen der Signatur für eine signierte Nachricht an. |
| [Beispiel C-Programm: Codieren und Decodieren einer CounterSigned-Nachricht](example-c-program-encoding-and-decoding-a-countersigned-message.md) | C-Beispielprogramm, das eine gegensignierte Nachricht codiert und decodiert. |



 

 

 
