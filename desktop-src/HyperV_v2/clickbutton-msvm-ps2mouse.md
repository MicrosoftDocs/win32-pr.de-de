---
description: Simuliert einen Klick auf die angegebene Geräteschaltfläche.
ms.assetid: 77CFA2E9-E422-464C-B124-6F7D3D56BA4C
title: ClickButton-Methode der Msvm_Ps2Mouse-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.ClickButton
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8209e12d6bef02a048b783c98a0299a32ec5ffb96e964ebb7d776e351daecedb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119254500"
---
# <a name="clickbutton-method-of-the-msvm_ps2mouse-class"></a>ClickButton-Methode der Msvm \_ Ps2Mouse-Klasse

Simuliert einen Klick auf die angegebene Geräteschaltfläche. Dies entspricht dem zweimaligen Aufrufen von [**SetButtonState,**](setbuttonstate-msvm-syntheticmouse.md) zuerst zum Drücken der Schaltfläche und zum erneuten Freigeben.

## <a name="syntax"></a>Syntax


```mof
uint32 ClickButton(
  [in] uint32 buttonIndex
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*buttonIndex* \[ In\]
</dt> <dd>

Typ: **uint32**

Der 1-basierte Index der Schaltfläche.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Der Rückgabewert 0 (null) gibt den Erfolg an. Ein Wert ungleich 0 (null) gibt an, dass der Schaltflächenzustand nicht geändert werden kann.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Überprüfte Methodenparameter – Auftragsstart** (4096)
</dt> <dt>

**Fehler** (32768)
</dt> <dt>

**Zugriff verweigert** (32769)
</dt> <dt>

**Nicht unterstützt** (32770)
</dt> <dt>

**Status ist unbekannt** (32771)
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Ungültiger Parameter** (32773)
</dt> <dt>

**System wird verwendet** (32774)
</dt> <dt>

**Ungültiger Zustand für diesen Vorgang** (32775)
</dt> <dt>

**Falscher Datentyp** (32776)
</dt> <dt>

**System ist nicht verfügbar** (32777)
</dt> <dt>

**Nicht genügend Arbeitsspeicher** (32778)
</dt> </dl>

## <a name="remarks"></a>Hinweise

Der Zugriff auf die [**Msvm \_ Ps2Mouse-Klasse**](msvm-ps2mouse.md) kann durch UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Msvm \_ Ps2Mouse**](msvm-ps2mouse.md)
</dt> </dl>

 

