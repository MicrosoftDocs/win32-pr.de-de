---
description: Manchmal erfordert eine signierte Nachricht eine gegen Signatur.
ms.assetid: de83a9ad-4e88-4477-8c9e-6dd7d5ec9e8f
title: Nachrichten gegen Signaturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8dff2920217dd9a79f917f7b625da3919747d7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752128"
---
# <a name="message-countersignatures"></a>Nachrichten gegen Signaturen

Manchmal erfordert eine signierte Nachricht eine [*gegen Signatur*](../secgloss/c-gly.md). Beispielsweise kann Benutzer a eine signierte Daten Nachricht an Benutzer B senden, wobei B erwartet, dass die Vereinbarung mit den im Dokument enthaltenen Begriffen bestätigt wird. Benutzer B decodiert die Nachricht, liest die Begriffe und signiert die Nachricht, wenn Sie in der Vereinbarung steht. Die gegen signierte Nachricht wird dann an Benutzer a zurückgesendet. Benutzer a weiß nun, dass der Benutzer B den Bedingungen zugestimmt hat.

In der folgenden Tabelle sind Abschnitte aufgelistet, die Prozedur Beschreibungen oder C-Programmbeispiele für die Nachrichten gegen Signierung enthalten.



| `Section`                                                                                                                                 | Contents                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Nachrichtenfunktionen](cryptography-functions.md)                                                                       | Listet die gegen Signatur Funktionen auf.                             |
| [Gegen Signieren einer Nachricht](countersigning-a-message.md)                                                                                | Erläutert den Prozess der gegen Signierung einer Nachricht.                  |
| [Überprüfen einer gegen Signatur](verifying-a-countersignature.md)                                                                        | Erläutert das Verfahren zum Überprüfen einer gegen Signatur.           |
| [Überprüfen einer signierten Nachricht](verifying-a-signed-message.md)                                                                            | Erläutert einen Prozess zum Überprüfen der Signatur in einer signierten Nachricht. |
| [Beispiel-C-Programm: Codieren und Decodieren einer gegen signierten Nachricht](example-c-program-encoding-and-decoding-a-countersigned-message.md) | Beispiel-C-Programm, das eine gegen signierte Nachricht codiert und decodiert. |



 

 

 
