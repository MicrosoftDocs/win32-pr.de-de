---
description: Legt die horizontale und vertikale Position des Mauszeigers fest.
ms.assetid: 7845E10A-7F61-4134-BF81-AED5483F36AD
title: Die Methode "settabsoluteposition" der Msvm_SyntheticMouse Klasse ("dbdao. h")
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse.SetAbsolutePosition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4b8ffb3a4d415f76dedf30acba5869b4cc585eb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864888"
---
# <a name="setabsoluteposition-method-of-the-msvm_syntheticmouse-class"></a>SetAbsolutePosition-Methode der MSVM- \_ syntheticmouse-Klasse

Legt die horizontale und vertikale Position des Mauszeigers fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetAbsolutePosition(
  [in] sint32 horizontalPosition,
  [in] sint32 verticalPosition
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*HorizontalPosition* \[ in\]
</dt> <dd>

Typ: **sint32**

Die neue horizontale Position des Mauszeigers in Pixel.

</dd> <dt>

*VerticalPosition* \[ in\]
</dt> <dd>

Typ: **sint32**

Die neue vertikale Position des Mauszeigers in Pixel.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Der Rückgabewert 0 (null) gibt den Erfolg an. Ein Wert ungleich 0 (null) gibt an, dass die Scrollposition nicht geändert werden konnte.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)
</dt> <dt>

Fehler **(32768** )
</dt> <dt>

**Zugriff verweigert** (32769)
</dt> <dt>

**Nicht unterstützt** (32770)
</dt> <dt>

Der **Status ist "Unknown** " (32771).
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Ungültiger Parameter** (32773)
</dt> <dt>

Das **System wird verwendet** (32774).
</dt> <dt>

**Ungültiger Status für diesen Vorgang** (32775).
</dt> <dt>

**Falscher Datentyp** (32776).
</dt> <dt>

Das **System ist nicht verfügbar** (32777).
</dt> <dt>

**Nicht** genügend Arbeitsspeicher (32778)
</dt> </dl>

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die [**MSVM \_ syntheticmouse**](msvm-syntheticmouse.md) -Klasse kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| Header<br/>                   | <dl> <dt>Dbdao. h</dt> </dl>                      |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM \_ syntheticmouse**](msvm-syntheticmouse.md)
</dt> </dl>

 

