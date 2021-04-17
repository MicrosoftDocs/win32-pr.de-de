---
title: "\"Peer-serveruseallpurposecert\""
description: Der Registrierungsschlüssel "papserveruseallpurposecert" bestimmt, ob für die Peer-Authentifizierung alle Zweck Zertifikate verwendet werden.
ms.assetid: e239fb88-4bf3-49b6-a95c-67a8c060a50d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc90f083f9020ad02960d7620a2ab54706df203e
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "104313835"
---
# <a name="peapserveruseallpurposecert"></a>"Peer-serveruseallpurposecert"

Der Registrierungsschlüssel "papserveruseallpurposecert" bestimmt, ob für die Peer-Authentifizierung alle Zweck Zertifikate verwendet werden.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   PeapServerUseAllPurposeCert = value
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **reg \_ DWORD** -Wert.



| Wert        | BESCHREIBUNG                                                                                                      |
|--------------|------------------------------------------------------------------------------------------------------------------|
| 1            | Alle Zweck Zertifikate im Zertifikat Speicher des Clients oder Servers werden für die Peer-Authentifizierung ausgewählt.     |
| Andere Werte | Alle Zweck Zertifikate im Zertifikat Speicher des Clients oder des Servers sind nicht für die Peer-Authentifizierung ausgewählt. |



 

Wenn dieser Registrierungs Wert nicht vorhanden ist, werden alle Zertifikate im Zertifikat Speicher des Clients oder des Servers für die Peer-Authentifizierung ausgewählt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[EAPHost-Registrierungs Einstellungen](eaphost-registry-settings.md)
</dt> </dl>

 

 




