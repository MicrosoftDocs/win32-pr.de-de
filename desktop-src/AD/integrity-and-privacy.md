---
title: Integrität und Datenschutz
description: Client-/Dienstkommunikation, die gegenseitige Authentifizierung erfordert, muss den Datenverkehr schützen, den sie nach erfolgreicher Authentifizierung austauschen.
ms.assetid: 5ae3ede3-6eed-4532-9b02-448d2f4ca674
ms.tgt_platform: multiple
keywords:
- Integrität und Datenschutz AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc7c287956fcebc250d5324a15f88fb6a47e087fca40f68f793dd695b47e6719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187104"
---
# <a name="integrity-and-privacy"></a>Integrität und Datenschutz

Client-/Dienstkommunikation, die gegenseitige Authentifizierung erfordert, muss den Datenverkehr schützen, den sie nach erfolgreicher Authentifizierung austauschen. Es ist unklug, sich zum Zeitpunkt der ersten Verbindung mit dem Dienst gegenseitig zu authentifizieren, wenn der Datenverkehr später von einem nicht autorisierten Benutzer geändert wird. SSPI, RPC und COM bieten Hilfsprogramme zum digitalen Signieren und Verschlüsseln von Nachrichten. Das Anwenden digitaler Signaturen verhindert, dass geänderter Datenverkehr unerkannt bleibt, und rät von Lauschangriffen ab. Der Datenverkehr kann natürlich abgefangen werden, aber die Entschlüsselung des Datenverkehrs ist ausreichend schwierig, um die meisten nicht autorisierten Benutzer abzuschärfen.

Sofern die Leistungsanforderungen nicht schwerwiegend sind, wird die Verwendung von Signierung und Verschlüsselung empfohlen, insbesondere für administrative Funktionen. Auch wenn die Leistung ein Problem ist, entscheiden sich einige Kunden für eine strengere Sicherheit als für eine bessere Leistung. Machen Sie in solchen Fällen konfigurierbare Optionen für Integrität und Datenschutz mit höherer Sicherheit zur Standard- und Leistungssteigerung.

RPC-Clients können die Integritäts- und Datenschutzebene angeben, wenn sie die [**RpcBindingSetAuthInfoEx-Funktion**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) aufrufen, um die Authentifizierungsdaten für die RPC-Bindung festzulegen. Verwenden **Sie RPC C \_ \_ AUTHN \_ LEVEL \_ PKT \_ INTEGRITY** für die Signierung und **RPC C \_ \_ AUTHN \_ LEVEL \_ PKT PRIVACY \_ für** die Verschlüsselung. Weitere Informationen finden Sie unter [Gegenseitige Authentifizierung in RPC-Anwendungen.](mutual-authentication-in-rpc-applications.md)

Dienste, die ein SSPI-Paket für die gegenseitige Authentifizierung verwenden, können das Paket abfragen, um zu bestimmen, ob es die [**Funktionen MakeSignature,**](/windows/desktop/api/sspi/nf-sspi-makesignature) [**VerifySignature,**](/windows/desktop/api/sspi/nf-sspi-verifysignature) [**EncryptMessage**](../SecAuthN/encryptmessage--general.md)und [**DecryptMessage**](../SecAuthN/decryptmessage--general.md) zum Signieren und Verschlüsseln von Nachrichten unterstützt. Weitere Informationen und ein Codebeispiel finden Sie unter [Ensuring Communication Integrity During Message Exchange](/windows/desktop/SecAuthN/ensuring-communication-integrity-during-message-exchange).

 

 