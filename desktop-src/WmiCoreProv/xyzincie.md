---
description: Enthält die Koordinaten der Anzeige im Bereich der International Commission on Illumination (CIE) XYZ-Farbraum.
ms.assetid: e44e8a5f-005d-4d58-84e3-135d4e396086
title: Xyzincie-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- XYZinCIE
- XYZinCIE.X
- XYZinCIE.Y
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: ba7f781a83f3e6ba5aa4683003386a0478d65088
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356988"
---
# <a name="xyzincie-class"></a>Xyzincie-Klasse

Die **xyzincie** WMI-Klasse enthält die Koordinaten der Anzeige im Bereich der International Commission on Illumination (CIE) XYZ-Farbraum.

## <a name="syntax"></a>Syntax

``` syntax
class XYZinCIE : WmiMonitorColorCharacteristics
{
  uint16 X;
  uint16 Y;
};
```

## <a name="members"></a>Member

Die **xyzincie** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **xyzincie** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**X**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

X-Koordinate.

</dd> <dt>

**J**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Y-Koordinate.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die [**wmimonitorcolorcharacteristics**](wmimonitorcolorcharacteristics.md) -Klasse enthält eingebettete Instanzen der **xyzincie** -Klasse, um die Farbmerkmale eines Monitors zu beschreiben.

Um die z-Koordinate basierend auf den x-und y-Werten zu berechnen, verwenden Sie die-Beziehung \| \| (x, y, z) \| \| = 1.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Namespace<br/>                | WMI-Stammdatei \\<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WMI Core. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




