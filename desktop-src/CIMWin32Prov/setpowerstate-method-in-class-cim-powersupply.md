---
description: Die SetPowerState-Methode der CIM PowerSupply-Klasse legt den gewünschten Energiezustand für ein logisches Gerät fest und legt fest, wann ein Gerät \_ in diesen Zustand gesetzt werden soll.
ms.assetid: 2f783410-1e71-4be2-9495-b2256b49d1a7
ms.tgt_platform: multiple
title: SetPowerState-Methode der CIM_PowerSupply Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PowerSupply.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f15aecffb88608ae88f89cc464180043e748450cdbd924a8699068d804033afa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119079884"
---
# <a name="setpowerstate-method-of-the-cim_powersupply-class"></a>SetPowerState-Methode der CIM \_ PowerSupply-Klasse

Die **SetPowerState-Methode** der CIM PowerSupply-Klasse legt den gewünschten Energiezustand für ein logisches Gerät fest und legt fest, wann ein Gerät \_ in diesen Zustand gesetzt werden soll. In einer Unterklasse sollte der Satz möglicher Rückgabecodes  mithilfe eines ValueMap-Qualifizierers für die -Methode angegeben werden. Die Zeichenfolgen, in die **der ValueMap-Inhalt** übersetzt wird, sollten auch in der Unterklasse als Values-Arrayqualifizierer angegeben werden.  Diese Methode wird von [**CIM \_ LogicalDevice geerbt.**](cim-logicaldevice.md)

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

## <a name="syntax"></a>Syntax


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PowerState* \[ In\]
</dt> <dd>

Ein **ValueMap-Wert,** der den gewünschten Energiezustand für dieses logische Gerät angibt.

<dt>

1
</dt> <dd>

Volle Leistung.

</dd> <dt>

2
</dt> <dd>

Energiesparmodus mit geringer Leistung.

</dd> <dt>

3
</dt> <dd>

Standbymodus "Energie sparen".

</dd> <dt>

4
</dt> <dd>

Energie sparen Sie andere.

</dd> <dt>

5
</dt> <dd>

Energiezyklus.

</dd> <dt>

6
</dt> <dd>

Ausschalten.

</dd> </dl> </dd> <dt>

*Zeit* \[ In\]
</dt> <dd>

Gibt an, wann der Energiezustand festgelegt werden soll, entweder als regulärer Datums-/Uhrzeitwert oder als Intervallwert (wobei das Intervall beginnt, wenn der Methodenaufruf empfangen wird). Wenn der *PowerState-Parameter* gleich 5 ("Power Cycle") ist, gibt der *Time-Parameter* an, wann das Gerät wieder ein-/aus netzen soll. Das Ausschalten ist sofort.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 (null) zurück, 1 (eins), wenn die angegebene *PowerState-* und *Time-Anforderung* nicht unterstützt wird, und einen anderen Wert, wenn ein anderer Fehler aufgetreten ist.

## <a name="remarks"></a>Hinweise

Diese Methode wird derzeit nicht von WMI implementiert. Um diese Methode zu verwenden, müssen Sie sie in Ihrem eigenen Anbieter implementieren.

Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von DMTF veröffentlicht wurden. Microsoft hat möglicherweise Änderungen vorgenommen, um kleinere Fehler zu beheben, die Dokumentationsstandards des Microsoft SDK zu erfüllen oder weitere Informationen zur Verfügung zu stellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[CIM \_ PowerSupply](setpowerstate-method-in-class-cim-powersupply.md)
</dt> <dt>

[**CIM \_ PowerSupply**](cim-powersupply.md)
</dt> </dl>

 

 




