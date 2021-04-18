---
title: Imstscaxevents onfocus Released-Methode
description: Wird aufgerufen, wenn die Tastenkombination für den releasefokus gedrückt wird. Beispielsweise wird dieses Ereignis aufgerufen, wenn der Benutzer die Tastenkombination STRG + ALT + nach-links oder STRG + ALT + nach-rechts-Taste drückt.
ms.assetid: f5d755b0-4b8f-4d62-8dc4-f6b63e3819e5
ms.tgt_platform: multiple
keywords:
- Onfocus Released-Methode Remotedesktopdienste
- Onfocus Released-Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, onfocus Released-Methode
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
ms.openlocfilehash: 6eff03f95d4ebbb068bccbfd9f68a930c00f0b00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337938"
---
# <a name="imstscaxeventsonfocusreleased-method"></a>Imstscaxevents:: onfocus Released-Methode

Wird aufgerufen, wenn die Tastenkombination für den releasefokus gedrückt wird. Beispielsweise wird dieses Ereignis aufgerufen, wenn der Benutzer die Tastenkombination STRG + ALT + nach-links oder STRG + ALT + nach-rechts-Taste drückt.

Dieses Ereignis ermöglicht dem ActiveX-Steuerelement Container, die Steuerung des ActiveX-Steuer Elements zu entfernen. Dies ist beispielsweise in einem Szenario hilfreich, in dem Sie keine Maus haben und spezielle Tastenkombinationen wie Alt + Tab an den Server umgeleitet werden. In diesem Fall haben Sie keine Möglichkeit, den Tastaturfokus zurück zum lokalen Desktop zurückzukehren. Mit der Tastenkombination STRG + ALT + nach-links oder STRG + ALT + nach-rechts-Taste kann der ActiveX-Container jedoch auf dieses Ereignis lauschen und reagieren, indem der Fokus vom ActiveX-Steuerelement entfernt wird.

## <a name="syntax"></a>Syntax


```C++
void OnFocusReleased(
  [in] INT iDirection
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*idirection* \[ in\]
</dt> <dd>

Der Richtungs Parameter 1 (STRG + ALT + nach-rechts-Taste) oder 1 (STRG + ALT + nach-links-Taste).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Dieses Ereignis ist verfügbar, wenn Remotedesktopverbindung 6,0 auf dem Client verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | Imstscaxevents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imstscaxevents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





