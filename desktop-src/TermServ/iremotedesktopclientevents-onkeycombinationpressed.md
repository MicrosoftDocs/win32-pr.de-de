---
title: IRemoteDesktopClientEvents OnKeyCombinationPressed-Methode
description: Wird aufgerufen, wenn in der Remotesitzung spezielle Tastenkombinationen gedrückt werden.
ms.assetid: 0A4EAD6C-5DA9-4ED3-BA79-92AE5AE81C9F
ms.tgt_platform: multiple
keywords:
- OnKeyCombinationPressed-Remotedesktopdienste
- OnKeyCombinationPressed-Methode Remotedesktopdienste , IRemoteDesktopClientEvents-Schnittstelle
- IRemoteDesktopClientEvents-Schnittstelle Remotedesktopdienste , OnKeyCombinationPressed-Methode
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
ms.openlocfilehash: e175bc0d65126c11cbcb97d0b73accd48ff92b02e38cca6e3ac35ebcce1ae961
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119515100"
---
# <a name="iremotedesktopclienteventsonkeycombinationpressed-method"></a>IRemoteDesktopClientEvents::OnKeyCombinationPressed-Methode

Wird aufgerufen, wenn in der Remotesitzung spezielle Tastenkombinationen gedrückt werden.

## <a name="syntax"></a>Syntax


```C++
void OnKeyCombinationPressed(
  [in] long keyCombination
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*keyCombination* \[ In\]
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
| IID<br/>                      | DIID \_ IRemoteDesktopClientEvents ist als 079863B7-6D47-4105-8BFE-0CDCB360E67D definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IRemoteDesktopClientEvents**](iremotedesktopclientevents.md)
</dt> </dl>

 

 





