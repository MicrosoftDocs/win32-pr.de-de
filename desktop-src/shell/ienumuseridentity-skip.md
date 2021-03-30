---
description: 'Iendumuseridentity:: Skip wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop.'
ms.assetid: bb19ae50-b384-48fb-9272-15e3e3eaa9d0
title: 'Ienumumuseridentity:: Skip-Methode (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Skip
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: cedd4f3c6e9736e26cbf8d58f27f805f0f5d33a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994599"
---
# <a name="ienumuseridentityskip-method"></a>Ienumumuseridentity:: Skip-Methode

\[**Iendumuseridentity:: Skip** wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen [Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop](fastuserswitching.md).\]

Überspringt eine angegebene Anzahl von Benutzer Identitäts Schnittstellen in der-Enumeration. Wird beim Abrufen von Schnittstellen verwendet.

## <a name="syntax"></a>Syntax


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*celt* \[ in\]
</dt> <dd>

Typ: **ulong**

Die Anzahl der zu überspringenden Schnittstellen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

[**Ienumumuseridentity**](ienumuseridentity.md) behält eine interne Anzahl bei, die angibt, welche Schnittstelle als nächstes abgerufen wird. Um diese Anzahl zu erhöhen, ohne Schnittstellen abzurufen, rufen Sie diese Methode auf. Um die Anzahl zurückzusetzen, nennen Sie [**ienumumuseridentity:: Reset**](ienumuseridentity-reset.md).

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                   |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                  |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                         |
| Header<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Iumumuseridentity**](ienumuseridentity.md)
</dt> <dt>

[**Ienumumuseridentity:: Reset**](ienumuseridentity-reset.md)
</dt> <dt>

[**Ienumumuseridentity:: Next**](ienumuseridentity-next.md)
</dt> <dt>

[**Iendumuseridentity:: GetCount**](ienumuseridentity-getcount.md)
</dt> </dl>

 

 




