---
description: 'IDelaydC::D isconnect-Methode: Die Disconnect-Methode trennt die NPP vom Netzwerk.'
ms.assetid: 476bbce4-2e3c-448f-b85e-6adac424fb0d
title: IDelaydC::D isconnect-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: ad24ad2557401509c1bc1e076a545f05d1c03dd79fbcf73a05d3efccfdfb8886
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910670"
---
# <a name="idelaydcdisconnect-method"></a>IDelaydC::D isconnect-Methode

Mit der **Disconnect-Methode** wird die NPP vom Netzwerk getrennt.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, lautet der Rückgabewert NMERR \_ SUCCESS.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                          | Beschreibung                                                                                                       |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_NMERR-ERFASSUNG**</dt> </dl>      | Das NPP erfasst Daten. Sie können die NPP während einer Erfassung nicht vom Netzwerk trennen.<br/>            |
| <dl> <dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt> </dl> | Das NPP ist nicht mit dem Netzwerk verbunden.<br/>                                                               |
| <dl> <dt>**NMERR \_ NICHT \_ VERZÖGERT**</dt> </dl>   | Das NPP ist mit dem Netzwerk verbunden, jedoch nicht mit der [IDelaydC::Verbinden-Methode.](idelaydc-connect.md)<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode kann nicht aufgerufen werden, wenn das NPP Daten erfasst. Sie müssen die **IDelaydC::Stop-Methode** aufrufen, bevor Sie **Disconnect** aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[IDelaydC::Verbinden](idelaydc-connect.md)
</dt> <dt>

[IDelaydC::Stop](idelaydc-stop.md)
</dt> </dl>

 

 




