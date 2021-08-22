---
title: CopyRootCauseInfo-Funktion (Ndattributils.h)
description: Erstellt eine Kopie einer RootCauseInfo-Struktur.
ms.assetid: 6bcd1341-657a-40c1-bebd-1c0f780ae337
keywords:
- CopyRootCauseInfo-Funktion NDF
topic_type:
- apiref
api_name:
- CopyRootCauseInfo
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98bb09fd9a61da536ddd17a4067838b33d4f86ffb8ee29fb404dc861220a5166
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685830"
---
# <a name="copyrootcauseinfo-function"></a>CopyRootCauseInfo-Funktion

Die **CopyRootCauseInfo-Funktion** erstellt eine Kopie einer [**RootCauseInfo-Struktur.**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)

## <a name="syntax"></a>Syntax


```C++
HRESULT CopyRootCauseInfo(
  _Out_       RootCauseInfo *Dest,
  _In_  const RootCauseInfo *Source
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dest* \[ out\]
</dt> <dd>

Typ: **[ **RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)\***

Die zu aktualisierende Struktur.

</dd> <dt>

*Quelle* \[ In\]
</dt> <dd>

Typ: **const [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) \***

Die vorhandene Struktur, die kopiert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Mögliche Rückgabewerte sind u. a. folgende.



| Rückgabecode                                                                                   | Beschreibung                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Der Vorgang wurde erfolgreich ausgeführt.<br/>                                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Mindestens ein Parameter wurde nicht ordnungsgemäß bereitgestellt.<br/>          |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher verfügbar, um diesen Vorgang abzuschließen.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Ndattributils.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)
</dt> </dl>

 

 





