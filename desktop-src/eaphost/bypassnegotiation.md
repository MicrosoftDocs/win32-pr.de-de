---
title: Bypassaushandlung
description: Der Registrierungsschlüssel bypassaushandlung bestimmt, ob eine Aushandlung der Funktionen zwischen Server und Client erfolgt oder ob vorkonfigurierte Einstellungen verwendet werden.
ms.assetid: 51e21e9c-d6cb-454b-9584-3f48d76a649a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9fdf883249fc5af7a37be83bb153a670295ba1d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "104389654"
---
# <a name="bypassnegotiation"></a>Bypassaushandlung

Der Registrierungsschlüssel bypassaushandlung bestimmt, ob eine Aushandlung der Funktionen zwischen Server und Client erfolgt oder ob vorkonfigurierte Einstellungen verwendet werden.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   BypassNegotiation = value
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **reg \_ DWORD** -Wert.



| Wert   | BESCHREIBUNG                                                                                                                                                                                          |
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0       | Der Server und der Client aushandeln EAP-Funktionen.                                                                                                                                                        |
| ungleich NULL | Der Server und der Client aushandeln keine EAP-Funktionen. Server und Client verwenden den [AssumePhase2Fragmentation](assumephase2fragmentation.md) -Registrierungsschlüssel Wert, um die Funktionen anderer Parteien zu suchen. |



 

Wenn dieser Registrierungs Wert nicht vorhanden ist, aushandelt der Server und der Client die EAP-Funktionen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[EAPHost-Registrierungs Einstellungen](eaphost-registry-settings.md)
</dt> </dl>

 

 




