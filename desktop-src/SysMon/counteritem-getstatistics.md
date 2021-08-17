---
title: CounterItem.GetStatistics-Methode
description: Ruft die Durchschnitts-, Höchst- und Mindestwerte für den Leistungsindikator ab.
ms.assetid: fb55d68b-1dbe-48b1-88c8-51f33048ec24
keywords:
- GetStatistics-Methode SysMon
- GetStatistics-Methode SysMon , CounterItem-Klasse
- CounterItem-Klasse SysMon , GetStatistics-Methode
topic_type:
- apiref
api_name:
- CounterItem.GetStatistics
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bea1be162d68bb02db4842a7140effe653231dcc5105c4bea3b557abb02beab0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118883776"
---
# <a name="counteritemgetstatistics-method"></a>CounterItem.GetStatistics-Methode

Ruft die Durchschnitts-, Höchst- und Mindestwerte für den Leistungsindikator ab.

## <a name="syntax"></a>Syntax


```VB
CounterItem.GetStatistics( _
  ByRef max As Double, _
  ByRef min As Double, _
  ByRef average As Double, _
  ByRef status As Long _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*max* \[ out\]
</dt> <dd>

Maximalwert des Leistungsindikators.

</dd> <dt>

*min* \[ out\]
</dt> <dd>

Mindestwert des Leistungsindikators.

</dd> <dt>

*Average (Durchschnitt)* \[ out\]
</dt> <dd>

Durchschnittswert des Leistungsindikators.

</dd> <dt>

*status* \[ out\]
</dt> <dd>

Gibt an, ob die Werte gültig sind.



| Wert                                                                                              | Bedeutung                              |
|----------------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>0</dt> </dl>                       | Die Werte sind gültig.<br/>     |
| <dl> <dt>0xC0000BBA (3221228474)</dt> </dl> | Die Werte sind ungültig.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Nur die Indikatorwerte, die im Diagrammfenster sichtbar sind, werden verwendet, um die statistischen Werte zu berechnen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> <dt>

[**CounterItem.GetDataAt**](counteritem-getdataat.md)
</dt> <dt>

[**CounterItem.GetValue**](counteritem-getvalue.md)
</dt> </dl>

 

 





