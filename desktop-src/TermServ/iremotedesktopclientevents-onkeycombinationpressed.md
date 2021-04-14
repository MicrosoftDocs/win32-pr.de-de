---
title: Iremotedesktopclientevents-Methode (onkeycombinationpressed)
description: Wird aufgerufen, wenn in der Remote Sitzung Sondertasten Kombinationen gedrückt werden.
ms.assetid: 0A4EAD6C-5DA9-4ED3-BA79-92AE5AE81C9F
ms.tgt_platform: multiple
keywords:
- Onkeycombinationpressed-Methode Remotedesktopdienste
- Onkeycombinationpressed-Methode Remotedesktopdienste, iremotedesktopclientevents-Schnittstelle
- Iremotedesktopclientevents-Schnittstelle Remotedesktopdienste, onkeycombinationpressed-Methode
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnKeyCombinationPressed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 192cad6323578a9bde9fe38af1d2b1d2cf83473c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391728"
---
# <a name="iremotedesktopclienteventsonkeycombinationpressed-method"></a>Iremotedesktopclientevents:: onkeycombinationpressed-Methode

Wird aufgerufen, wenn in der Remote Sitzung Sondertasten Kombinationen gedrückt werden.

## <a name="syntax"></a>Syntax


```C++
void OnKeyCombinationPressed(
  [in] long keyCombination
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Tastenkombination* \[ in\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                 |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | Diid \_ iremotedesktopclientevents ist als 079863b7-6d47-4105-8bfe-0cdcb360e67d definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iremotedesktopclientevents**](iremotedesktopclientevents.md)
</dt> </dl>

 

 





