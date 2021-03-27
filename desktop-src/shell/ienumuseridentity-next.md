---
description: 'Ienumumuseridentity:: Next wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop.'
ms.assetid: 2c8dfe36-c1bb-49f8-8847-f355cfab2984
title: 'Ienumumuseridentity:: Next-Methode (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Next
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 763b2b4a612596c5f02a9826ad2e9c09ab8e4b0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994607"
---
# <a name="ienumuseridentitynext-method"></a>Ienumumuseridentity:: Next-Methode

\[**Ienumumuseridentity:: Next** wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen [Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop](fastuserswitching.md).\]

Veraltet. Ruft ein Array von Benutzer Identitäts Schnittstellen aus der-Enumeration ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT Next(
  [in]  ULONG    celt,
  [out] IUnknown **rgelt,
  [out] ULONG    *pceltFetched
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*celt* \[ in\]
</dt> <dd>

Typ: **ulong**

Ein **ulong** -Wert, der die Anzahl der abzurufenden Schnittstellen darstellt.

</dd> <dt>

*rgelt* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***

Die Adresse eines Zeigers, der die Schnittstellen empfängt.

</dd> <dt>

*pceltfetch* \[ vorgenommen\]
</dt> <dd>

Typ: **ulong \** _

Die Adresse eines Zeigers, der die Anzahl der erfolgreich abgerufenen Schnittstellen empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Type: _ *HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

[**Ienumumuseridentity**](ienumuseridentity.md) behält eine interne Anzahl bei, die angibt, welche Schnittstelle als nächstes abgerufen wird. Bei mehreren Aufrufen dieser Methode wird diese Anzahl nicht zurückgesetzt. Um die Anzahl zurückzusetzen, nennen Sie [**ienumumuseridentity:: Reset**](ienumuseridentity-reset.md). Um die Anzahl zu erhöhen, ohne Schnittstellen abzurufen, rufen Sie [**ienumumuseridentity:: Skip**](ienumuseridentity-skip.md)auf.

Der Wert von " *celt* " sollte nicht den Wert überschreiten, der von " [**ienumumuseridentity:: GetCount**](ienumuseridentity-getcount.md)" zurückgegeben wird.

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

[**Iendumuseridentity:: Skip**](ienumuseridentity-skip.md)
</dt> <dt>

[**Ienumumuseridentity:: Reset**](ienumuseridentity-reset.md)
</dt> <dt>

[**Iendumuseridentity:: GetCount**](ienumuseridentity-getcount.md)
</dt> </dl>

 

 
