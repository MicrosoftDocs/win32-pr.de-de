---
title: TlsServerUseAllPurposeCert
description: Der Registrierungsschlüssel TlsServerUseAllPurposeCert bestimmt, ob Alle-Zweck-Zertifikate für die EAP-TLS-Authentifizierung verwendet werden.
ms.assetid: a672cecb-6bba-4ba6-b362-f6d5a220184b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af2f9d47b4e80409c27c71fe3655a1d3266571e0f8a8dd757e5334b0ef9fec40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118085695"
---
# <a name="tlsserveruseallpurposecert"></a>TlsServerUseAllPurposeCert

Der Registrierungsschlüssel TlsServerUseAllPurposeCert bestimmt, ob Alle-Zweck-Zertifikate für die EAP-TLS-Authentifizierung verwendet werden.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   TlsServerUseAllPurposeCert = value
```

## <a name="remarks"></a>Hinweise

Dies ist ein **REG \_ DWORD-Wert.**



| Wert        | Beschreibung                                                                                                      |
|--------------|------------------------------------------------------------------------------------------------------------------|
| 1            | Alle Zweckzertifikate im Zertifikatspeicher des Clients oder Servers werden für die PEAP-Authentifizierung ausgewählt.     |
| Andere Werte | Allzweckzertifikate im Zertifikatspeicher des Clients oder Servers werden nicht für die PEAP-Authentifizierung ausgewählt. |



 

Wenn dieser Registrierungswert nicht vorhanden ist, werden alle Zweckzertifikate im Zertifikatspeicher des Clients oder Servers für die EAP-TLS-Authentifizierung ausgewählt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[EAPHost Registry Einstellungen](eaphost-registry-settings.md)
</dt> </dl>

 

 




