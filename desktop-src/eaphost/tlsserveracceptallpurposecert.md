---
title: TlsServerAcceptAllPurposeCert
description: Der Registrierungsschlüssel TlsServerAcceptAllPurposeCert bestimmt, ob Alle-Zweck-Zertifikate für die EAP-TLS-Authentifizierung akzeptiert werden.
ms.assetid: F0881397-5D8C-4C8F-8EB5-6D59454C55B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 804185773a948299aed3d8b8e2f581d8d8355d112720b66e860bd1f00b7fc3d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118085752"
---
# <a name="tlsserveracceptallpurposecert"></a>TlsServerAcceptAllPurposeCert

Der Registrierungsschlüssel TlsServerAcceptAllPurposeCert bestimmt, ob Alle-Zweck-Zertifikate für die EAP-TLS-Authentifizierung akzeptiert werden.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   TlsServerAcceptAllPurposeCert = value
```

## <a name="remarks"></a>Hinweise

Dies ist ein **REG \_ DWORD-Wert.**



| Wert        | Beschreibung                                                                                                 |
|--------------|-------------------------------------------------------------------------------------------------------------|
| 1            | Server und Client akzeptieren alle von der anderen Partei zur EAP-TLS-Authentifizierung gesendeten Zertifikate.       |
| Andere Werte | Server und Client akzeptieren keine allzweckbasierten Zertifikate, die von der anderen Partei für die EAP-TLS-Authentifizierung gesendet werden. |



 

Wenn dieser Registrierungswert nicht vorhanden ist, akzeptieren Server und Client alle von der anderen Partei für die EAP-TLS-Authentifizierung gesendeten Zertifikate.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[EAPHost Registry Einstellungen](eaphost-registry-settings.md)
</dt> </dl>

 

 




