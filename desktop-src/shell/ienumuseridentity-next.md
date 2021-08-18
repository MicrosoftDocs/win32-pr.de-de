---
description: IEnumUserIdentity::Next wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schnellem Benutzerwechsel und Remotedesktop.
ms.assetid: 2c8dfe36-c1bb-49f8-8847-f355cfab2984
title: IEnumUserIdentity::Next-Methode (Msident.h)
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
ms.openlocfilehash: eb3074a7b55ce03e7372491fce11160f1df1bc5fc8a4e45ad0f12d4538d4b2f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009400"
---
# <a name="ienumuseridentitynext-method"></a>IEnumUserIdentity::Next-Methode

\[**IEnumUserIdentity::Next** wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein. Verwenden Sie stattdessen [Benutzerkonten mit schnellem Benutzerwechsel und Remotedesktop](fastuserswitching.md).\]

Veraltet. Ruft ein Array von Benutzeridentitätsschnittstellen aus der -Enumeration ab.

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

*Celt* \[ In\]
</dt> <dd>

Typ: **ULONG**

Ein **ULONG-Wert,** der die Anzahl der abzurufende Schnittstellen darstellt.

</dd> <dt>

*rgelt* \[ out\]
</dt> <dd>

Typ: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***

Die Adresse eines Zeigers, der die Schnittstellen empfängt.

</dd> <dt>

*pceltFetched* \[ out\]
</dt> <dd>

Typ: **ULONG \***

Die Adresse eines Zeigers, der die Anzahl der erfolgreich abgerufenen Schnittstellen empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

[**IEnumUserIdentity**](ienumuseridentity.md) behält eine interne Anzahl bei, die angibt, welche Schnittstelle als Nächstes abgerufen werden soll. Durch mehrere Aufrufe dieser Methode wird diese Anzahl nicht zurückgesetzt. Um die Anzahl zurückzusetzen, rufen [**Sie IEnumUserIdentity::Reset auf.**](ienumuseridentity-reset.md) Um die Anzahl zu erhöhen, ohne Schnittstellen abzurufen, rufen [**Sie IEnumUserIdentity::Skip**](ienumuseridentity-skip.md)auf.

Der Wert von *celt* darf den von [**IEnumUserIdentity::GetCount zurückgegebenen**](ienumuseridentity-getcount.md)Wert nicht überschreiten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                            |
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

[**IEnumUserIdentity::Reset**](ienumuseridentity-reset.md)
</dt> <dt>

[**IEnumUserIdentity::GetCount**](ienumuseridentity-getcount.md)
</dt> </dl>

 

 
