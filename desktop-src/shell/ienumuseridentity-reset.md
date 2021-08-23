---
description: Setzt die interne Anzahl der abgerufenen Schnittstellen in der -Enumeration zurück.
ms.assetid: fd79b4be-cc0c-49b3-9874-384858e21ecf
title: IEnumUserIdentity::Reset-Methode (Msident.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Reset
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: df70048760af47b380308eddab4ef5c044c8f6881374c83002944d6d76836ed5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969419"
---
# <a name="ienumuseridentityreset-method"></a>IEnumUserIdentity::Reset-Methode

\[**IEnumUserIdentity::Reset** wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein. Verwenden Sie stattdessen [Benutzerkonten mit schnellem Benutzerwechsel und Remotedesktop](fastuserswitching.md).\]

Setzt die interne Anzahl der abgerufenen Schnittstellen in der -Enumeration zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT Reset();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

[**IEnumUserIdentity behält**](ienumuseridentity.md) eine interne Anzahl bei, die angibt, welche Schnittstelle als Nächstes abgerufen werden soll. Durch Aufrufen dieser Methode wird der Wert dieser Anzahl zurückgesetzt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                   |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                  |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                         |
| Header<br/>                   | <dl> <dt>Msident.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msident.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IEnumUserIdentity**](ienumuseridentity.md)
</dt> <dt>

[**IEnumUserIdentity::Skip**](ienumuseridentity-skip.md)
</dt> <dt>

[**IEnumUserIdentity::GetCount**](ienumuseridentity-getcount.md)
</dt> <dt>

[**IEnumUserIdentity::Next**](ienumuseridentity-next.md)
</dt> </dl>

 

 




