---
title: "\"Peer-serveraccept tallpurposecert\""
description: Der Registrierungsschlüssel "papserverakzeptallpurposecert" legt fest, ob Zertifikate für alle Zwecke für die Peer-Authentifizierung akzeptiert werden.
ms.assetid: 59C58459-7735-4733-9F95-646864802D70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b291696c6bee90b4f980d8f96ad96faf40fe3376
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "106339034"
---
# <a name="peapserveracceptallpurposecert"></a>"Peer-serveraccept tallpurposecert"

Der Registrierungsschlüssel "papserverakzeptallpurposecert" legt fest, ob Zertifikate für alle Zwecke für die Peer-Authentifizierung akzeptiert werden.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   PeapServerAcceptAllPurposeCert = value
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **reg \_ DWORD** -Wert.



| Wert        | BESCHREIBUNG                                                                                                 |
|--------------|-------------------------------------------------------------------------------------------------------------|
| 1            | Server und Client akzeptieren sämtliche Zertifikate, die von der anderen Partei für die EAP-TLS-Authentifizierung gesendet werden.       |
| Andere Werte | Server und Client akzeptieren keine von der anderen Partei gesendeten Zertifikate für die EAP-TLS-Authentifizierung. |



 

Wenn dieser Registrierungs Wert nicht vorhanden ist, akzeptieren der Server und der Client sämtliche Zertifikate, die von der anderen Partei für die Peer-Authentifizierung gesendet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[EAPHost-Registrierungs Einstellungen](eaphost-registry-settings.md)
</dt> </dl>

 

 




