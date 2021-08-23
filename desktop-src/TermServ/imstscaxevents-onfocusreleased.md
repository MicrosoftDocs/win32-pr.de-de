---
title: IMsTscAxEvents OnFocusReleased-Methode
description: Wird aufgerufen, wenn die Tastenkombination für den Releasefokus gedrückt wird. Dieses Ereignis wird beispielsweise aufgerufen, wenn der Benutzer die Tastenkombination STRG+ALT+NACH-LINKS oder STRG+ALT+NACH-RECHTS-TASTE drückt.
ms.assetid: f5d755b0-4b8f-4d62-8dc4-f6b63e3819e5
ms.tgt_platform: multiple
keywords:
- OnFocusReleased-Remotedesktopdienste
- OnFocusReleased-Methode Remotedesktopdienste , IMsTscAxEvents-Schnittstelle
- IMsTscAxEvents-Schnittstelle Remotedesktopdienste , OnFocusReleased-Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnFocusReleased
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 673916c3a538f21ceea5b0b7578bb9e8f225ec2a349e38015eab0b50d73935aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512340"
---
# <a name="imstscaxeventsonfocusreleased-method"></a>IMsTscAxEvents::OnFocusReleased-Methode

Wird aufgerufen, wenn die Tastenkombination für den Releasefokus gedrückt wird. Dieses Ereignis wird beispielsweise aufgerufen, wenn der Benutzer die Tastenkombination STRG+ALT+NACH-LINKS oder STRG+ALT+NACH-RECHTS-TASTE drückt.

Dieses Ereignis ermöglicht dem ActiveX, die Kontrolle vom Steuerelement ActiveX zu nehmen. Dies ist beispielsweise nützlich in einem Szenario, in dem Sie keine Maus haben und spezielle Tastenkombinationen wie ALT+TAB an den Server umgeleitet werden. In diesem Fall haben Sie keine Möglichkeit, den Tastaturfokus auf den lokalen Desktop zurück zu setzen. Mit der Tastenkombination STRG+ALT+NACH-LINKS oder STRG+ALT+NACH-RECHTS-TASTE kann der ActiveX-Container jedoch auf dieses Ereignis lauschen und reagieren, indem er den Fokus vom Steuerelement ActiveX entfernt.

## <a name="syntax"></a>Syntax


```C++
void OnFocusReleased(
  [in] INT iDirection
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*iDirection* \[ In\]
</dt> <dd>

Der Richtungsparameter von 1 (STRG+ALT+NACH-RECHTS-TASTE) oder 1 (STRG+ALT+NACH-LINKS-TASTE).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Dieses Ereignis ist verfügbar, wenn Remotedesktopverbindung 6.0 auf dem Client verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





