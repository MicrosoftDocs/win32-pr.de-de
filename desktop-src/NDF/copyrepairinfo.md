---
title: Copyrepairren Info-Funktion (ndattributils. h)
description: Erstellt eine Kopie einer repairiinfo-Struktur.
ms.assetid: a1147ce6-9a90-4a46-8fe4-da3353391a13
keywords:
- Copyrepairren Info-Funktion NDF
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
ms.openlocfilehash: 7a24d15ec5a8a69b3c8c40700273ebcb6f32bcfd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949659"
---
# <a name="copyrepairinfo-function"></a>Copyrepairren Info-Funktion

Die **copyrepairren Info** -Funktion erstellt eine Kopie einer [**repairiinfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) -Struktur.

## <a name="syntax"></a>Syntax


```C++
HRESULT CopyRepairInfo(
  _Out_       RepairInfo *Dest,
  _In_  const RepairInfo *Source
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dest* \[ vorgenommen\]
</dt> <dd>

Geben Sie Folgendes ein: **[**repairren Info**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) \** _

Die zu Aktualisier Ende-Struktur.

</dd> <dt>

_Source * \[ in\]
</dt> <dd>

Geben Sie Folgendes ein: * Konstante *[**repairren Info**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) \** _

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

[**Repairren Info**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)
</dt> </dl>

 

 





