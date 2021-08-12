---
title: CopyRepairInfo-Funktion (Ndattributils.h)
description: Erstellt eine Kopie einer RepairInfo-Struktur.
ms.assetid: a1147ce6-9a90-4a46-8fe4-da3353391a13
keywords:
- CopyRepairInfo-Funktion NDF
topic_type:
- apiref
api_name:
- CopyRepairInfo
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e40a054df2b16684840f22295f0c26de6029ef150a97ca8839c98d94713ab030
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118620435"
---
# <a name="copyrepairinfo-function"></a>CopyRepairInfo-Funktion

Die **CopyRepairInfo-Funktion** erstellt eine Kopie einer [**RepairInfo-Struktur.**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)

## <a name="syntax"></a>Syntax


```C++
HRESULT CopyRepairInfo(
  _Out_       RepairInfo *Dest,
  _In_  const RepairInfo *Source
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dest* \[ out\]
</dt> <dd>

Typ: **[ **RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)\***

Die zu aktualisierende -Struktur.

</dd> <dt>

*Quelle* \[ In\]
</dt> <dd>

Typ: **const [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) \***

Die vorhandene zu kopierende -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Mögliche Rückgabewerte sind u. a. folgende:



| Rückgabecode                                                                                   | Beschreibung                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Der Vorgang wurde erfolgreich ausgeführt.<br/>                                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Mindestens ein Parameter wurde nicht ordnungsgemäß bereitgestellt.<br/>          |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher verfügbar, um diesen Vorgang abschließen zu können.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Ndattributils.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)
</dt> </dl>

 

 





