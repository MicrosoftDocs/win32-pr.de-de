---
title: Copyhelperattribute-Funktion (ndattributils. h)
description: Erstellt eine Kopie einer \_ hilfsattribut Struktur.
ms.assetid: ff49be29-4cd8-4730-929f-c66a7325704f
keywords:
- Copyhelperattribute-Funktion NDF
topic_type:
- apiref
api_name:
- CopyHelperAttribute
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59fac3449ee48659980681c836d24406c4db7e2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338328"
---
# <a name="copyhelperattribute-function"></a>Copyhelperattribute-Funktion

Die **copyhelperattribute** -Funktion erstellt eine Kopie einer [**\_ hilfsattribut**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) Struktur.

## <a name="syntax"></a>Syntax


```C++
HRESULT CopyHelperAttribute(
  _Out_       HELPER_ATTRIBUTE *Dest,
  _In_  const HELPER_ATTRIBUTE *Source
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dest* \[ vorgenommen\]
</dt> <dd>

Type: **[**helper- \_ Attribut**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) \** _

Die zu Aktualisier Ende-Struktur.

</dd> <dt>

_Source * \[ in\]
</dt> <dd>

Geben Sie Folgendes ein: * Konstante *[**\_ hilfsattribut**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) \** _

Die vorhandene zu kopierende-Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Type: _ *HRESULT**

Mögliche Rückgabewerte sind u. a. die folgenden.



| Rückgabecode                                                                                   | Beschreibung                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Der Vorgang wurde erfolgreich ausgeführt.<br/>                                         |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Mindestens ein Parameter wurde nicht ordnungsgemäß bereitgestellt.<br/>          |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher verfügbar, um diesen Vorgang abzuschließen.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Ndattributils. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**HELPER- \_ Attribut**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)
</dt> </dl>

 

 





