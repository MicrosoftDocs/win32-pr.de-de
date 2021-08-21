---
title: PeapServerUseAllPurposeCert
description: Der Registrierungsschlüssel PeapServerUseAllPurposeCert bestimmt, ob alle Zweckzertifikate für die PEAP-Authentifizierung verwendet werden.
ms.assetid: e239fb88-4bf3-49b6-a95c-67a8c060a50d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a5086a0067bab70a0e222def34d1adf236b37127c0d1ff6c91ac83b8b28c73c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042818"
---
# <a name="peapserveruseallpurposecert"></a>PeapServerUseAllPurposeCert

Der Registrierungsschlüssel PeapServerUseAllPurposeCert bestimmt, ob alle Zweckzertifikate für die PEAP-Authentifizierung verwendet werden.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   PeapServerUseAllPurposeCert = value
```

## <a name="remarks"></a>Hinweise

Dies ist ein **REG \_ DWORD-Wert.**



| Wert        | Beschreibung                                                                                                      |
|--------------|------------------------------------------------------------------------------------------------------------------|
| 1            | Alle Zweckzertifikate im Zertifikatspeicher des Clients oder Servers werden für die PEAP-Authentifizierung ausgewählt.     |
| Andere Werte | Allzweckzertifikate im Zertifikatspeicher des Clients oder Servers werden nicht für die PEAP-Authentifizierung ausgewählt. |



 

Wenn dieser Registrierungswert nicht vorhanden ist, werden alle Zweckzertifikate im Zertifikatspeicher des Clients oder Servers für die PEAP-Authentifizierung ausgewählt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[EAPHost Registry Einstellungen](eaphost-registry-settings.md)
</dt> </dl>

 

 




