---
title: SRPTrustLevel
description: Legt die Richtlinie für die Software Einschränkungs Richtlinie (SRP) für Anwendungen fest.
ms.assetid: 2ec10eb5-f83a-4ce7-8e03-36cdafadf169
keywords:
- SRPTrustLevel Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c1e9290cbe04cfe33e1192b95b86ca03fd5ea5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388146"
---
# <a name="srptrustlevel"></a>SRPTrustLevel

Legt die Richtlinie für die Software Einschränkungs Richtlinie (SRP) für Anwendungen fest.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      SRPTrustLevel = value
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **reg \_ DWORD** -Wert, der ab Windows XP verfügbar ist.



| Wert                                 | BESCHREIBUNG                                                                          |
|---------------------------------------|--------------------------------------------------------------------------------------|
| 0x0 (sicherere \_ levelid nicht \_ zulässig)      | Der Zugriff auf und sicherheitsrelevante Benutzerberechtigungen ist für die Anwendung nicht zulässig. |
| 0x40000 (sichere \_ levelid \_ fullytrusted) | Die Anwendung hat uneingeschränkten Zugriff auf die Berechtigungen des Benutzers.                    |



 

Wenn der **SRPTrustLevel** -Wert nicht vorhanden ist, wird der Standardwert von sicherere \_ levelid nicht \_ zulässig verwendet. Wenn **SRPTrustLevel** den falschen Typ oder außerhalb des zulässigen Bereichs hat, gibt com den Fehler COMAdmin \_ E \_ saferinvalid zurück. Wenn die Aktivierung einer beliebigen Sortierung aufgrund von SRP-Vertrauensstellungs Überprüfungen fehlschlägt, gibt com den Fehler Co \_ E \_ activationfailed zurück.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sicherheit in com](security-in-com.md)
</dt> <dt>

[**Srpactivateasactivatorchecks**](srpactivateasactivatorchecks.md)
</dt> <dt>

[**Srprunningobjectchecks**](srprunningobjectchecks.md)
</dt> </dl>

 

 




