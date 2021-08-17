---
description: IEnumUserIdentity::Skip wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schnellem Benutzerwechsel und Remotedesktop.
ms.assetid: bb19ae50-b384-48fb-9272-15e3e3eaa9d0
title: IEnumUserIdentity::Skip-Methode (Msident.h)
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
ms.openlocfilehash: ced6a1a9ce463f82b6b33275339216edabc02737928e985a294154e579523575
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117678927"
---
# <a name="ienumuseridentityskip-method"></a>IEnumUserIdentity::Skip-Methode

\[**IEnumUserIdentity::Skip** wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein. Verwenden Sie stattdessen [Benutzerkonten mit schnellem Benutzerwechsel und Remotedesktop](fastuserswitching.md).\]

Überspringt eine bestimmte Anzahl von Benutzeridentitätsschnittstellen in der -Enumeration. Wird beim Abrufen von Schnittstellen verwendet.

## <a name="syntax"></a>Syntax


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Celt* \[ In\]
</dt> <dd>

Typ: **ULONG**

Die Anzahl der zu überspringenden Schnittstellen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

[**IEnumUserIdentity**](ienumuseridentity.md) behält eine interne Anzahl bei, die angibt, welche Schnittstelle als Nächstes abgerufen werden soll. Um diese Anzahl zu erhöhen, ohne Schnittstellen abzurufen, rufen Sie diese Methode auf. Um die Anzahl zurückzusetzen, rufen [**Sie IEnumUserIdentity::Reset auf.**](ienumuseridentity-reset.md)

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IEnumUserIdentity**](ienumuseridentity.md)
</dt> <dt>

[**IEnumUserIdentity::Reset**](ienumuseridentity-reset.md)
</dt> <dt>

[**IEnumUserIdentity::Next**](ienumuseridentity-next.md)
</dt> <dt>

[**IEnumUserIdentity::GetCount**](ienumuseridentity-getcount.md)
</dt> </dl>

 

 




