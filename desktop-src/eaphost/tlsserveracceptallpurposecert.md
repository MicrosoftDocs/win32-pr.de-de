---
title: Tlsserverakzeptallpurposecert
description: Der Registrierungsschlüssel "tlsserverakzeptallpurposecert" legt fest, ob Zertifikate für alle Zwecke für die EAP-TLS-Authentifizierung akzeptiert werden.
ms.assetid: F0881397-5D8C-4C8F-8EB5-6D59454C55B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6561418d8d9cb06fb9618e6b93189cbd28e408
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "106338237"
---
# <a name="tlsserveracceptallpurposecert"></a>Tlsserverakzeptallpurposecert

Der Registrierungsschlüssel "tlsserverakzeptallpurposecert" legt fest, ob Zertifikate für alle Zwecke für die EAP-TLS-Authentifizierung akzeptiert werden.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   TlsServerAcceptAllPurposeCert = value
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **reg \_ DWORD** -Wert.



| Wert        | BESCHREIBUNG                                                                                                 |
|--------------|-------------------------------------------------------------------------------------------------------------|
| 1            | Server und Client akzeptieren sämtliche Zertifikate, die von der anderen Partei für die EAP-TLS-Authentifizierung gesendet werden.       |
| Andere Werte | Server und Client akzeptieren keine von der anderen Partei gesendeten Zertifikate für die EAP-TLS-Authentifizierung. |



 

Wenn dieser Registrierungs Wert nicht vorhanden ist, akzeptieren der Server und der Client alle Zweck Zertifikate, die von der anderen Partei für die EAP-TLS-Authentifizierung gesendet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[EAPHost-Registrierungs Einstellungen](eaphost-registry-settings.md)
</dt> </dl>

 

 




