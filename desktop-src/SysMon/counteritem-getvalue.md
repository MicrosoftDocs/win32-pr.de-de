---
title: Count. GetValue-Methode
description: Ruft den letzten Wert des Zählers ab.
ms.assetid: cf50d878-a119-42b0-bc59-b0e37ed15321
keywords:
- GetValue-Methode (Sysmon)
- GetValue-Methode "sysmon", "count"-Klasse
- "\"Sysmon\"-Klasse der \"count Value\"-Klasse"
topic_type:
- apiref
api_name:
- CounterItem.GetValue
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94e40950ce4a8bf24a6a4301db133779b34ce4ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342466"
---
# <a name="counteritemgetvalue-method"></a>Count. GetValue-Methode

Ruft den letzten Wert des Zählers ab.

## <a name="syntax"></a>Syntax


```VB
CounterItem.GetValue( _
  ByRef value As Double, _
  ByRef status As Long _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wert* \[ vorgenommen\]
</dt> <dd>

Der zuletzt erfasste Wert des Zählers.

</dd> <dt>

*Status* \[ vorgenommen\]
</dt> <dd>

Gibt an, ob der Wert gültig ist.



| Wert                                                                                              | Bedeutung                            |
|----------------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <dt>0</dt> </dl>                       | Der Wert ist gültig.<br/>     |
| <dl> <dt>0xc0000bba (3221228474)</dt> </dl> | Der Wert ist ungültig.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn die Quelle der Leistungsdaten aus einer Protokolldatei ist, ist der Wert der letzte Leistungswert in der Protokolldatei.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ratteritem**](counteritem.md)
</dt> <dt>

[**"Count. getstatistics"**](counteritem-getstatistics.md)
</dt> <dt>

[**"Count. Value"**](counteritem-value.md)
</dt> </dl>

 

 





