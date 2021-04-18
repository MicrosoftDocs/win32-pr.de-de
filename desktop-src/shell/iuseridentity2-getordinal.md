---
description: Getorion wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop.
ms.assetid: 20b1c1d0-b09f-43a8-9026-9cdbac28c108
title: 'IUserIdentity2:: getordin-Methode (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2.GetOrdinal
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: f5a7e875e92342363722858b3ac714171cb547b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980048"
---
# <a name="iuseridentity2getordinal-method"></a>IUserIdentity2:: getordindiningmethode

\[**Getorion** wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen [Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop](fastuserswitching.md).\]

Ruft die Ordinalzahl für diese Identität ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetOrdinal(
  [out] DWORD *dwOrdinal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwordinon* \[ vorgenommen\]
</dt> <dd>

Typ: **DWORD \** _

Ein Zeiger auf einen _ *DWORD**-Wert, der die Ordinalzahl für diese Identität empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Die Ordinalzahl bestimmt die Reihenfolge der Identitäten in der Identitäts Liste, bleibt jedoch möglicherweise nicht während der Vorgänge für die Identitäten erhalten. Um einen eindeutigen Wert für eine Identität abzurufen, nennen Sie [**GetCookie**](iuseridentity-getcookie.md).

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Ende des Supports (Client)<br/>    | Windows 2000 Professional<br/>                                                   |
| Ende des Supports (Server)<br/>    | Windows 2000 Server<br/>                                                         |
| Header<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IUserIdentity2**](iuseridentity2.md)
</dt> <dt>

[**GetCookie**](iuseridentity-getcookie.md)
</dt> </dl>

 

 




