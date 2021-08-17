---
title: PeapServerAcceptAllPurposeCert
description: Der Registrierungsschlüssel PeapServerAcceptAllPurposeCert bestimmt, ob alle Zweckzertifikate für die PEAP-Authentifizierung akzeptiert werden.
ms.assetid: 59C58459-7735-4733-9F95-646864802D70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d568ef2cf3e7fd5eeeaa650e5e6e4fd32a8e1c8d6baa0ed91434a5c0aa60ee0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118784682"
---
# <a name="peapserveracceptallpurposecert"></a>PeapServerAcceptAllPurposeCert

Der Registrierungsschlüssel PeapServerAcceptAllPurposeCert bestimmt, ob alle Zweckzertifikate für die PEAP-Authentifizierung akzeptiert werden.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   PeapServerAcceptAllPurposeCert = value
```

## <a name="remarks"></a>Hinweise

Dies ist ein **REG \_ DWORD-Wert.**



| Wert        | BESCHREIBUNG                                                                                                 |
|--------------|-------------------------------------------------------------------------------------------------------------|
| 1            | Server und Client akzeptieren alle von der anderen Partei zur EAP-TLS-Authentifizierung gesendeten Zertifikate.       |
| Andere Werte | Server und Client akzeptieren keine allzweckbasierten Zertifikate, die von der anderen Partei für die EAP-TLS-Authentifizierung gesendet werden. |



 

Wenn dieser Registrierungswert nicht vorhanden ist, akzeptieren server und client alle von der anderen Partei für die PEAP-Authentifizierung gesendeten Allzweckzertifikate.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[EAPHost Registry Einstellungen](eaphost-registry-settings.md)
</dt> </dl>

 

 




