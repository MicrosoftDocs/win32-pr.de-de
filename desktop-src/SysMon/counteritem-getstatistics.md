---
title: Countryteritem. getstatistics-Methode
description: Ruft die durchschnittlichen, maximalen und minimalen Werte für den Zählers ab.
ms.assetid: fb55d68b-1dbe-48b1-88c8-51f33048ec24
keywords:
- Getstatistics-Methode (Sysmon)
- Getstatistics-Methode "sysmon", "count"-Klasse
- Namteritem Class sysmon, getstatistics-Methode
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
ms.openlocfilehash: 1c993ed8b9bb39a4d8bb3ff18663f2d884ece156
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956596"
---
# <a name="counteritemgetstatistics-method"></a>Countryteritem. getstatistics-Methode

Ruft die durchschnittlichen, maximalen und minimalen Werte für den Zählers ab.

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

*Max* \[ . vorgenommen\]
</dt> <dd>

Maximaler Wert des Zählers.

</dd> <dt>

*Min* \[ . vorgenommen\]
</dt> <dd>

Der Minimalwert des Zählers.

</dd> <dt>

*Durchschnitt* \[ vorgenommen\]
</dt> <dd>

Der Durchschnittswert des Zählers.

</dd> <dt>

*Status* \[ vorgenommen\]
</dt> <dd>

Gibt an, ob die Werte gültig sind.



| Wert                                                                                              | Bedeutung                              |
|----------------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>0</dt> </dl>                       | Die Werte sind gültig.<br/>     |
| <dl> <dt>0xc0000bba (3221228474)</dt> </dl> | Die Werte sind ungültig.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Es werden nur die im Diagramm fenstersicht baren Werte verwendet, um die statistischen Werte zu berechnen.

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

[**"Count. getdataat"**](counteritem-getdataat.md)
</dt> <dt>

[**"Count. GetValue"**](counteritem-getvalue.md)
</dt> </dl>

 

 





