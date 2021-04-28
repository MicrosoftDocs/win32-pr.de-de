---
description: 'GetButtonState-Methode der Msvm_Ps2Mouse-Klasse: Ruft den aktuellen Zustand der angegebenen Geräteschaltfläche ab.'
ms.assetid: 7772A3AC-1677-44A7-9E5E-D31E90988705
title: GetButtonState-Methode der Msvm_Ps2Mouse-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.GetButtonState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 160134a2ae48bb23dc525eeded70b483484e0b71
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112198"
---
# <a name="getbuttonstate-method-of-the-msvm_ps2mouse-class"></a>GetButtonState-Methode der Msvm \_ Ps2Mouse-Klasse

Ruft den aktuellen Zustand der angegebenen Geräteschaltfläche ab.

## <a name="syntax"></a>Syntax


```mof
uint32 GetButtonState(
  [in]  uint32  buttonIndex,
  [out] boolean buttonState
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*buttonIndex* \[ In\]
</dt> <dd>

Typ: **uint32**

Der 1-basierte Index der abzufragenden Schaltfläche.

</dd> <dt>

*buttonState* \[ out\]
</dt> <dd>

Typ: **boolescher Wert**

Der aktuelle Abwärtszustand der Schaltfläche. Ein **True-Wert** bedeutet, dass die Schaltfläche nicht angezeigt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Der Rückgabewert 0 (null) gibt den Erfolg an. Ein Wert ungleich 0 (null) gibt einen Abfragefehler an.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Methodenparameter überprüft** – Auftrag gestartet (4096)
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

**Ungültiger** Parameter (32773)
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

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die [**Msvm \_ Ps2Mouse-Klasse**](msvm-ps2mouse.md) kann durch UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8 \[ Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2012-Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Msvm \_ Ps2Mouse**](msvm-ps2mouse.md)
</dt> </dl>

 

