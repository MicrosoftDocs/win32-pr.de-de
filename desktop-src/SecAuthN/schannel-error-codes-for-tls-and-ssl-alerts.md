---
description: Schannel gibt die folgenden Fehlermeldungen zurück, wenn die entsprechende Warnung von den Protokollen Transport Layer Security (TLS) oder Secure Sockets Layer (SSL) empfangen wird.
ms.assetid: 0a6ac61d-a00c-4fc8-a995-d25d17e405df
title: Schannel-Fehlercodes für TLS- und SSL-Warnungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4819c39948a2baf5889734fe7e2c08c8d85cbd22868cc9fad8a33281d13a306c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918589"
---
# <a name="schannel-error-codes-for-tls-and-ssl-alerts"></a>Schannel-Fehlercodes für TLS- und SSL-Warnungen

[*Schannel*](../secgloss/s-gly.md) gibt die folgenden Fehlermeldungen zurück, wenn die entsprechende Warnung von den [*Protokollen Transport Layer Security*](../secgloss/t-gly.md) (TLS) oder [*Secure Sockets Layer*](../secgloss/s-gly.md) (SSL) empfangen wird. Die Fehlermeldungen werden in Winerror.h definiert.



| TLS- oder SSL-Warnung                                           | Schannel-Fehlercode                                                   |
|------------------------------------------------------------|-----------------------------------------------------------------------|
| UNERWARTETE \_ \_ \_ SSL3-WARNUNGSMELDUNG<br/> 10<br/>  | SEC \_ E \_ ILLEGAL \_ MESSAGE<br/> 0x80090326<br/>             |
| TLS1 \_ ALERT \_ BAD \_ RECORD \_ MAC<br/> 20<br/>     | SEC \_ E \_ MESSAGE \_ ALTERED<br/> 0x8009030F<br/>             |
| FEHLER BEI DER \_ TLS1-WARNUNGSENTSCHLÜSSELUNG \_ \_<br/> 21<br/>   | SEC \_ E \_ DECRYPT \_ FAILURE<br/> 0x80090330<br/>             |
| TLS1 \_ ALERT \_ RECORD \_ OVERFLOW<br/> 22<br/>     | SEC \_ E \_ ILLEGAL \_ MESSAGE<br/> 0x80090326<br/>             |
| FEHLER BEI DER \_ \_ DEKOMPRIMIERUNG VON SSL3-WARNUNGEN \_<br/> 30<br/>  | SEC \_ E \_ MESSAGE \_ ALTERED<br/> 0x8009030F<br/>             |
| SSL3 \_ ALERT \_ HANDSHAKE \_ FAILURE<br/> 40<br/>   | SEC \_ E \_ ILLEGAL \_ MESSAGE<br/> 0x80090326<br/>             |
| UNGÜLTIGES \_ \_ \_ TLS1-WARNUNGSZERTIFIKAT<br/> 42<br/>     | SEC \_ E \_ CERT \_ UNKNOWN<br/> 0x80090327<br/>                |
| TLS1 \_ ALERT \_ UNSUPPORTED \_ CERT<br/> 43<br/>    | SEC \_ E \_ CERT \_ UNKNOWN<br/> 0x80090327<br/>                |
| \_TLS1-WARNUNGSZERTIFIKAT \_ \_ WIDERRUFEN<br/> 44<br/> | CRYPT \_ E \_ REVOKED<br/> 0x80092010<br/>                    |
| \_TLS1-WARNUNGSZERTIFIKAT \_ \_ ABGELAUFEN<br/> 45<br/> | SEC \_ E \_ CERT \_ EXPIRED<br/> 0x80090328<br/>                |
| \_TLS1-WARNUNGSZERTIFIKAT \_ \_ UNBEKANNT<br/> 46<br/> | SEC \_ E \_ CERT \_ UNKNOWN<br/> 0x80090327<br/>                |
| SSL3 \_ ALERT \_ ILLEGAL \_ PARAMETER<br/>                 | SEC \_ E \_ ILLEGAL \_ MESSAGE<br/> 0x80090326<br/>             |
| TLS1 \_ ALERT \_ UNKNOWN \_ CA<br/> 48<br/>          | \_NICHT \_ VERTRAUENSWÜRDIGER \_ SEC E-STAMM<br/> 0x80090325<br/>              |
| ZUGRIFF \_ AUF TLS1-WARNUNG \_ \_ VERWEIGERT<br/> 49<br/>       | SEC \_ E \_ LOGON \_ DENIED<br/> 0x8009030C<br/>                |
| FEHLER BEIM DECODIEREN VON \_ TLS1-WARNUNGEN \_ \_<br/> 50<br/>        | SEC \_ E \_ ILLEGAL \_ MESSAGE<br/> 0x80090326<br/>             |
| TLS1 \_ ALERT \_ DECRYPT \_ ERROR<br/> 51<br/>       | SEC \_ E \_ DECRYPT \_ FAILURE<br/> 0x80090330<br/>             |
| EXPORTEINSCHRÄNKUNG \_ FÜR TLS1-WARNUNGEN \_ \_<br/> 60<br/>  | SEC \_ E \_ ILLEGAL \_ MESSAGE<br/> 0x80090326<br/>             |
| VERSION \_ DES TLS1-WARNUNGSPROTOKOLLS \_ \_<br/> 70<br/>    | \_NICHT \_ UNTERSTÜTZTE SEC \_ E-FUNKTION<br/> 0x80090302<br/>        |
| \_TLS1-WARNUNG \_ INSUFFIENT \_ SECURITY<br/> 71<br/> | SEC \_ E \_ ALGORITHM \_ MISMATCH<br/> 0x80090331<br/>          |
| INTERNER \_ \_ \_ TLS1-WARNUNGSFEHLER<br/> 80<br/>      | \_INTERNER \_ SEC \_ E-FEHLER<br/> 0x80090304<br/>              |
| \_TLS1-WARNUNGSBENUTZER \_ \_ ABGEBROCHEN<br/> 90<br/>       | SEC \_ E \_ UNFINISHED \_ CONTEXT \_ DELETED<br/> 0x80090333<br/> |
| \_TLS1-WARNUNG \_ KEINE \_ NEUVERHANDLUNG<br/> 100<br/>   | SEC \_ E \_ ILLEGAL \_ MESSAGE<br/> 0x80090326<br/>             |
| TLS1 \_ ALERT \_ UNSUPPORTED \_ EXT<br/> 110<br/>    | SEC \_ E \_ ILLEGAL \_ MESSAGE<br/> 0x80090326<br/>             |
| Standard<br/>                                         | SEC \_ E \_ ILLEGAL \_ MESSAGE<br/> 0x80090326<br/>             |



 

 

 
