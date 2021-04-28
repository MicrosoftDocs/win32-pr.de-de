---
description: 'SetPowerState-Methode der CIM_AggregatePExtent-Klasse: Die SetPowerState-Methode legt den gewünschten Energiezustand für ein logisches Gerät fest und legt fest, wann das Gerät in diesen Zustand gesetzt werden soll.'
ms.assetid: 1a1a8d5e-d685-4b7e-99fb-61fa2e7bdafa
ms.tgt_platform: multiple
title: SetPowerState-Methode der CIM_AggregatePExtent Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregatePExtent.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5ed988e5f58464479aa29d709eb628feb13f0d1c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089538"
---
# <a name="setpowerstate-method-of-the-cim_aggregatepextent-class"></a>SetPowerState-Methode der CIM \_ AggregatePExtent-Klasse

Die **SetPowerState-Methode** legt den gewünschten Energiezustand für ein logisches Gerät fest und legt fest, wann das Gerät in diesen Zustand gesetzt werden soll. In einer Unterklasse sollte der Satz möglicher Rückgabecodes mithilfe eines ValueMap-Qualifizierers für die -Methode angegeben werden.  Die Zeichenfolgen, in die **der ValueMap-Inhalt** übersetzt wird, sollten auch in der Unterklasse als Values-Arrayqualifizierer angegeben werden.  Diese Methode wird von [**CIM \_ LogicalDevice geerbt.**](cim-logicaldevice.md)

Weitere Informationen zur Verwendung dieser Methode mit C/C++ finden Sie unter [Aufrufen einer Methode.](/windows/desktop/WmiSdk/calling-a-method)

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

Der **ValueMap-Wert,** der den gewünschten Energiezustand für dieses logische Gerät angibt.

<dt>

1
</dt> <dd>

Volle Leistung

</dd> <dt>

2
</dt> <dd>

Energiesparmodus

</dd> <dt>

3
</dt> <dd>

Standbymodus "Stromsparen"

</dd> <dt>

4
</dt> <dd>

Stromsparen anderer

</dd> <dt>

5
</dt> <dd>

Energiezyklus

</dd> <dt>

6
</dt> <dd>

Ausschalten

</dd> </dl> </dd> <dt>

*Zeit* \[ In\]
</dt> <dd>

Wenn der Energiezustand festgelegt werden soll, entweder als regulärer Datums-/Uhrzeitwert oder als Intervallwert (wobei das Intervall beginnt, wenn der Methodenaufruf empfangen wird). Wenn der *PowerState-Parameter* gleich 5 (Energiezyklus) ist, gibt der *Time-Parameter* an, wann das Gerät wieder ein-/aus-netzen soll. Das Ausschalten erfolgt sofort.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 (null) zurück, 1 (eins), wenn die angegebene *PowerState-* und *Time-Anforderung* nicht unterstützt wird, und einen anderen Wert, wenn ein anderer Fehler aufgetreten ist.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird derzeit nicht von WMI implementiert. Um diese Methode verwenden zu können, müssen Sie sie in Ihrem eigenen Anbieter implementieren.

Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von dmtf veröffentlicht wurden. Möglicherweise hat Microsoft Änderungen vorgenommen, um kleinere Fehler zu korrigieren, den Dokumentationsstandards des Microsoft SDK zu entsprechen oder weitere Informationen bereitzustellen.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Stamm \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CIM \_ AggregatePExtent**](setpowerstate-method-in-class-cim-aggregatepextent.md)
</dt> <dt>

[**CIM \_ AggregatePExtent**](cim-aggregatepextent.md)
</dt> </dl>

 

