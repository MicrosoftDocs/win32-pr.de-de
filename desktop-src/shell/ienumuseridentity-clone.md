---
description: 'Ienumumuseridentity:: Clone wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop.'
ms.assetid: dde9afca-db8d-41ba-afa0-94eadecb695b
title: 'Ienumumuseridentity:: Clone-Methode (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Clone
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: ebdec426fe7ab591c801c00b637211e903cf5356
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994614"
---
# <a name="ienumuseridentityclone-method"></a>Ienumumuseridentity:: Clone-Methode

\[**Ienumumuseridentity:: Clone** wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen [Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop](fastuserswitching.md).\]

Ruft eine Kopie der aktuellen Enumeration ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT Clone(
  [out] IEnumUserIdentity **ppenum
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppum* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **iumumuseridentity**](ienumuseridentity.md)\*\***

Die Adresse eines Zeigers, der eine Kopie dieser Enumeration empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

[**Ienumumuseridentity**](ienumuseridentity.md) behält eine interne Anzahl bei, die angibt, welche Schnittstelle als nächstes abgerufen wird. Der Wert dieser Anzahl wird auf die von *ppum* empfangene Schnittstelle angewendet. Um die Anzahl zurückzusetzen, nennen Sie [**ienumumuseridentity:: Reset**](ienumuseridentity-reset.md).

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
</dt> </dl>

 

 




