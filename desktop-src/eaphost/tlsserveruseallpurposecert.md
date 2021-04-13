---
title: Tlsserveruseallpurposecert
description: Der tlsserveruseallpurposecert-Registrierungsschlüssel legt fest, ob alle Zweck Zertifikate für die EAP-TLS-Authentifizierung verwendet werden.
ms.assetid: a672cecb-6bba-4ba6-b362-f6d5a220184b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b7cb767a8f6c8f40b377cca84d948b384170486
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "104313812"
---
# <a name="tlsserveruseallpurposecert"></a>Tlsserveruseallpurposecert

Der tlsserveruseallpurposecert-Registrierungsschlüssel legt fest, ob alle Zweck Zertifikate für die EAP-TLS-Authentifizierung verwendet werden.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   TlsServerUseAllPurposeCert = value
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **reg \_ DWORD** -Wert.



| Wert        | BESCHREIBUNG                                                                                                      |
|--------------|------------------------------------------------------------------------------------------------------------------|
| 1            | Alle Zweck Zertifikate im Zertifikat Speicher des Clients oder Servers werden für die Peer-Authentifizierung ausgewählt.     |
| Andere Werte | Alle Zweck Zertifikate im Zertifikat Speicher des Clients oder des Servers sind nicht für die Peer-Authentifizierung ausgewählt. |



 

Wenn dieser Registrierungs Wert nicht vorhanden ist, werden alle Zweck Zertifikate im Zertifikat Speicher des Clients oder des Servers für die EAP-TLS-Authentifizierung ausgewählt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[EAPHost-Registrierungs Einstellungen](eaphost-registry-settings.md)
</dt> </dl>

 

 




