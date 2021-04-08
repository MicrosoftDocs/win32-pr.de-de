---
description: SChannel gibt die folgenden Fehlermeldungen zurück, wenn die entsprechende Warnung vom Transport Layer Security (TLS)-oder Secure Sockets Layer (SSL)-Protokoll empfangen wird.
ms.assetid: 0a6ac61d-a00c-4fc8-a995-d25d17e405df
title: SChannel-Fehler Codes für TLS-und SSL-Warnungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9fdba202e63d212fc85f0c02eb5ac9dc20db047
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959635"
---
# <a name="schannel-error-codes-for-tls-and-ssl-alerts"></a>SChannel-Fehler Codes für TLS-und SSL-Warnungen

[*SChannel*](../secgloss/s-gly.md) gibt die folgenden Fehlermeldungen zurück, wenn die entsprechende Warnung vom [*Transport Layer Security*](../secgloss/t-gly.md) (TLS)-oder [*Secure Sockets Layer*](../secgloss/s-gly.md) (SSL)-Protokoll empfangen wird. Die Fehlermeldungen werden in WinError. h definiert.



| TLS-oder SSL-Warnung                                           | SChannel-Fehlercode                                                   |
|------------------------------------------------------------|-----------------------------------------------------------------------|
| SSL3 \_ Warnung \_ unerwartete \_ Meldung<br/> 10<br/>  | s \_ E ungültige \_ \_ Nachricht<br/> 0x80090326<br/>             |
| Das TLS1 verwendet \_ Warnung fehlerhafter \_ \_ Datensatz \_ Mac<br/> 20<br/>     | Sek. \_ E- \_ Nachricht \_ geändert<br/> 0x8009030f<br/>             |
| Das TLS1 verwendet Fehler beim \_ Entschlüsseln der Warnung \_ \_<br/> 21<br/>   | SEK \_ . \_ Fehler beim Entschlüsseln \_<br/> 0x80090330<br/>             |
| Das TLS1 verwendet Warnungs \_ \_ Daten Satz \_ Überlauf<br/> 22<br/>     | s \_ E ungültige \_ \_ Nachricht<br/> 0x80090326<br/>             |
| SSL3 Warnungs \_ \_ Komprimierung \_ fehlgeschlagen<br/> 30<br/>  | Sek. \_ E- \_ Nachricht \_ geändert<br/> 0x8009030f<br/>             |
| SSL3 Warnungs \_ \_ Hand Shake \_ Fehler<br/> 40<br/>   | s \_ E ungültige \_ \_ Nachricht<br/> 0x80090326<br/>             |
| Das TLS1 verwendet \_ Warnung fehlerhaftes \_ \_ Zertifikat<br/> 42<br/>     | Sek. \_ E- \_ Zertifikat \_ unbekannt<br/> 0x80090327<br/>                |
| Das TLS1 verwendet \_ Warnung \_ nicht unterstütztes \_ Zertifikat<br/> 43<br/>    | Sek. \_ E- \_ Zertifikat \_ unbekannt<br/> 0x80090327<br/>                |
| Das TLS1 verwendet Warnungs \_ \_ Zertifikat gesperrt \_<br/> 44<br/> | Crypt \_ wurde \_ widerrufen<br/> 0x80092010<br/>                    |
| Das TLS1 verwendet Warnungs \_ \_ Zertifikat \_ abgelaufen<br/> 45<br/> | Sek. \_ E- \_ Zertifikat \_ abgelaufen<br/> 0x0x80090328<br/>                |
| Das TLS1 verwendet Warnungs \_ \_ Zertifikat \_ unbekannt<br/> 46<br/> | Sek. \_ E- \_ Zertifikat \_ unbekannt<br/> 0x80090327<br/>                |
| SSL3-Warnung unzulässiger \_ \_ \_ Parameter<br/>                 | s \_ E ungültige \_ \_ Nachricht<br/> 0x80090326<br/>             |
| Das TLS1 verwendet \_ Warnung \_ unbekannt ( \_ ca)<br/> 48<br/>          | Sekunde \_ E \_ nicht vertrauenswürdiger Stamm \_<br/> 0x80090325<br/>              |
| Das TLS1 verwendet Warnungs \_ \_ Zugriff \_ verweigert<br/> 49<br/>       | Sek. \_ E- \_ Anmeldung \_ verweigert<br/> 0x8009030c bei<br/>                |
| Das TLS1 verwendet Warnungs \_ \_ \_ Decodierungsfehler<br/> 50<br/>        | s \_ E ungültige \_ \_ Nachricht<br/> 0x80090326<br/>             |
| Das TLS1 verwendet \_ - \_ Fehler beim Entschlüsseln der Warnung \_<br/> 51<br/>       | SEK \_ . \_ Fehler beim Entschlüsseln \_<br/> 0x80090330<br/>             |
| Das TLS1 verwendet Warnungs \_ \_ Export \_ Einschränkung<br/> 60<br/>  | s \_ E ungültige \_ \_ Nachricht<br/> 0x80090326<br/>             |
| Das TLS1 verwendet Warnungs \_ \_ Protokoll \_ Version<br/> 70<br/>    | s \_ E \_ nicht unterstützte \_ Funktion<br/> 0x80090302<br/>        |
| Das TLS1 verwendet \_ Warnung ( \_ insuffient- \_ Sicherheit)<br/> 71<br/> | Sek. nicht übereinstimmende \_ \_ Algorithmen \_<br/> 0x80090331<br/>          |
| Das TLS1 verwendet \_ \_ interner \_ Fehler bei Warnung<br/> 80<br/>      | Sek. \_ E ( \_ interner \_ Fehler)<br/> 0x80090304<br/>              |
| Das TLS1 verwendet- \_ Benachrichtigungs \_ Benutzer \_ abgebrochen<br/> 90<br/>       | Sek. \_ E nicht \_ abgeschlossenen \_ Kontext \_ gelöscht<br/> 0x80090333<br/> |
| Das TLS1 verwendet \_ Warnung \_ keine \_ Neuverhandlung<br/> 100<br/>   | s \_ E ungültige \_ \_ Nachricht<br/> 0x80090326<br/>             |
| Das TLS1 verwendet \_ Warnung \_ nicht unterstützte \_ ext<br/> 110<br/>    | s \_ E ungültige \_ \_ Nachricht<br/> 0x80090326<br/>             |
| Standard<br/>                                         | s \_ E ungültige \_ \_ Nachricht<br/> 0x80090326<br/>             |



 

 

 
