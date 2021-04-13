---
description: Die SetPowerState-Methode der CIM \_ -Klasse "magnedeopticaldrive" legt den gewünschten Energiezustand für ein logisches Gerät fest, und wenn ein Gerät in diesen Zustand versetzt werden soll.
ms.assetid: 78f89dd5-79ce-43cc-b878-9d943386eb74
ms.tgt_platform: multiple
title: SetPowerState-Methode der CIM_MagnetoOpticalDrive-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MagnetoOpticalDrive.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3d634a0c4185d8854543697368bac1e2374ab8ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483902"
---
# <a name="setpowerstate-method-of-the-cim_magnetoopticaldrive-class"></a>SetPowerState-Methode der CIM- \_ Klasse "magnedeopticaldrive"

Die **SetPowerState** -Methode der CIM \_ -Klasse "magnedeopticaldrive" legt den gewünschten Energiezustand für ein logisches Gerät fest, und wenn ein Gerät in diesen Zustand versetzt werden soll. In einer Unterklasse sollte der Satz möglicher Rückgabecodes mit einem **ValueMap** -Qualifizierer für die-Methode angegeben werden. Die Zeichen folgen, in die der **ValueMap** -Inhalt übersetzt wird, sollten in der-Unterklasse auch als **Werte** Array Qualifizierer angegeben werden. Diese Methode wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

## <a name="syntax"></a>Syntax


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PowerState* \[ in\]
</dt> <dd>

Ein **ValueMap** -Wert, der den gewünschten Energiezustand für dieses logische Gerät angibt.

<dt>

1
</dt> <dd>

Vollständige Leistung.

</dd> <dt>

2
</dt> <dd>

Energiesparmodus im Energiesparmodus.

</dd> <dt>

3
</dt> <dd>

Energiesparmodus.

</dd> <dt>

4
</dt> <dd>

Andere Energie speichern.

</dd> <dt>

5
</dt> <dd>

Leistungs Zyklen.

</dd> <dt>

6
</dt> <dd>

Ausschalten.

</dd> </dl> </dd> <dt>

*Uhrzeit* \[ in\]
</dt> <dd>

Gibt an, wann der Energiezustand festgelegt werden soll, entweder als regulärer Datums-/Uhrzeitwert oder als Intervall Wert (wobei das Intervall beginnt, wenn der Methodenaufruf empfangen wird). Wenn der *PowerState* -Parameter gleich 5 ("Power Cycle") ist, gibt der *Zeit* Parameter an, wann das Gerät erneut einschalten soll. Der Ausschalten erfolgt sofort.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 (null) zurück, 1 (eins), wenn die angegebene *PowerState* -und *time* -Anforderung nicht unterstützt wird, und einen anderen Wert, wenn ein anderer Fehler aufgetreten ist.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird zurzeit nicht von WMI implementiert. Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.

Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet. Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[CIM- \_ Magnet Laufwerk](setpowerstate-method-in-class-cim-magnetoopticaldrive.md)
</dt> <dt>

[**CIM- \_ Magnet Laufwerk**](cim-magnetoopticaldrive.md)
</dt> </dl>

 

 




