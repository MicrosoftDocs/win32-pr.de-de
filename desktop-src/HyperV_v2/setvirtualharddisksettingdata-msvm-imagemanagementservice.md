---
description: Aktualisiert die Einstellungen für eine virtuelle Festplatte.
ms.assetid: 10f80313-bc78-447e-bdf2-5635d7354e3c
title: Setvirtualharddisksettingdata-Methode der Msvm_ImageManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.SetVirtualHardDiskSettingData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 969e9019d05b49f2f171f2177e1e74f135e212da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349029"
---
# <a name="setvirtualharddisksettingdata-method-of-the-msvm_imagemanagementservice-class"></a>Setvirtualharddisksettingdata-Methode der MSVM \_ imagemanagementservice-Klasse

Aktualisiert die Einstellungen für eine virtuelle Festplatte.

## <a name="syntax"></a>Syntax


```mof
uint32 SetVirtualHardDiskSettingData(
  [in]  string              VirtualDiskSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Virtualdisksettingdata* \[ in\]
</dt> <dd>

Eine Zeichen folgen Darstellung der [**MSVM \_ virtualharddisksettingdata**](msvm-virtualharddisksettingdata.md) -Klasse, die die zu aktualisierenden virtuellen Festplatte angibt, die die neuen Einstellungsdaten enthält. Nur die Eigenschaften **path**, **physicalsectorsize** oder **virtualdiskid** können mit dieser Methode aktualisiert werden. Sie können diese Eigenschaften nicht mit einem Methoden aufzurufen aktualisieren. Sie können eine dieser Eigenschaften nur mit einem einzigen Methoden aufzurufen aktualisieren.

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

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

**System wird verwendet** (32774)
</dt> <dt>

**Ungültiger Status für diesen Vorgang** (32775).
</dt> <dt>

**Falscher Datentyp** (32776).
</dt> <dt>

Das **System ist nicht verfügbar** (32777).
</dt> <dt>

**Nicht** genügend Arbeitsspeicher (32778)
</dt> <dt>

Die **Datei wurde nicht gefunden** (32779).
</dt> </dl>

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die [**MSVM \_ imagemanagementservice**](msvm-imagemanagementservice.md) -Klasse kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM \_ imagemanagementservice**](msvm-imagemanagementservice.md)
</dt> </dl>

 

