---
title: Integrität und Datenschutz
description: Die Kommunikation zwischen Client und Dienst, die eine gegenseitige Authentifizierung erfordert, muss den Datenverkehr schützen, den Sie nach erfolgreicher Authentifizierung
ms.assetid: 5ae3ede3-6eed-4532-9b02-448d2f4ca674
ms.tgt_platform: multiple
keywords:
- Integrität und Datenschutz (AD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88ed167c3796aec2b0717b1207ff56565ec94afa
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103948561"
---
# <a name="integrity-and-privacy"></a>Integrität und Datenschutz

Die Kommunikation zwischen Client und Dienst, die eine gegenseitige Authentifizierung erfordert, muss den Datenverkehr schützen, den Sie nach erfolgreicher Authentifizierung Es ist unklug, sich zum Zeitpunkt der anfänglichen Verbindung mit dem Dienst gegenseitig zu authentifizieren, wenn der Datenverkehr später von einem nicht autorisierten Benutzer geändert werden kann. SSPI, RPC und com stellen alle Hilfsprogramme zum digitalen Signieren und Verschlüsseln von Nachrichten bereit. Durch das Anwenden digitaler Signaturen wird verhindert, dass der geänderte Datenverkehr nicht erkannt wird. Der Datenverkehr kann natürlich abgefangen werden, aber das Entschlüsseln des Datenverkehrs ist ausreichend schwierig, um die meisten nicht autorisierten Benutzer zu verhindern.

Wenn die Leistungsanforderungen nicht schwerwiegend sind, wird die Verwendung von Signierung und Verschlüsselung empfohlen, insbesondere für administrative Funktionen. Auch wenn die Leistung ein Problem ist, haben einige Kunden eine strengere Sicherheit als eine bessere Leistung. In solchen Fällen können Sie mithilfe der Option "Integritäts-und Datenschutzoptionen" mit höherer Sicherheit die Standard-und höhere Leistung konfigurieren.

RPC-Clients können die Integritäts-und Datenschutzebene angeben, wenn Sie die Funktion [**rpcbindingsetauthinfoex**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) aufrufen, um die Authentifizierungsdaten für die RPC-Bindung festzulegen. Verwenden Sie die **\_ \_ \_ \_ Pkt- \_ Integrität der RPC-c-authn-Ebene** für die Signierung und die **\_ \_ \_ \_ Pkt- \_ Datenschutzebene der RPC-c** Weitere Informationen finden Sie unter [gegenseitige Authentifizierung in RPC-Anwendungen](mutual-authentication-in-rpc-applications.md).

Dienste, die ein SSPI-Paket für die gegenseitige Authentifizierung verwenden, können das Paket Abfragen, um zu bestimmen, ob es die Funktionen [**makesignature**](/windows/desktop/api/sspi/nf-sspi-makesignature), [**VerifySignature**](/windows/desktop/api/sspi/nf-sspi-verifysignature), [**verschlüsseltmessage**](../SecAuthN/encryptmessage--general.md)und [**DecryptMessage**](../SecAuthN/decryptmessage--general.md) zum Signieren und Verschlüsseln von Nachrichten unterstützt. Weitere Informationen und ein Codebeispiel finden Sie unter [sicherstellen der Kommunikations Integrität während des Nachrichten Austauschs](/windows/desktop/SecAuthN/ensuring-communication-integrity-during-message-exchange).

 

 