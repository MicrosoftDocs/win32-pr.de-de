---
description: Bietet die Möglichkeit, den aktuellen World Wide Port Name (WWPN) anzuzeigen, ohne dass der WWPN reserviert ist.
ms.assetid: 7fc02099-744e-4a56-ae4b-1f5fd6a1eb45
title: Getcurrentwwpnfromgenerator-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetCurrentWwpnFromGenerator
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 88e1fd8f19b4a0542744cbfff7058ed7e69a421d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959026"
---
# <a name="getcurrentwwpnfromgenerator-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Getcurrentwwpnfromgenerator-Methode der MSVM \_ virtualsystemmanagementservice-Klasse

Bietet die Möglichkeit, den aktuellen World Wide Port Name (WWPN) anzuzeigen, ohne dass der WWPN reserviert ist. Der WWPN wird aus dem vorkonfigurierten Bereich generiert, der durch die Eigenschaften **minimumwwpnaddress** und **maximumwwpnaddress** der [**MSVM \_ virtualsystemmanagementservicesettingdata**](msvm-virtualsystemmanagementservicesettingdata.md) -Klasse definiert wird. Wenn der von diesen Eigenschaften definierte Bereich erschöpft ist, weist das generierte WWPN den ungültigen Eintrag "0000000000000000" auf, und der Rückgabewert gibt Erfolg (0) an.

## <a name="syntax"></a>Syntax


```mof
uint32 GetCurrentWwpnFromGenerator(
  [out] string CurrentWwpn
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Currentwwpn* \[ vorgenommen\]
</dt> <dd>

Eine Zeichenfolge, die den Wert des aktuellen WWPN hat, wie er vom WWPN-Generator verwendet wird. Dabei handelt es sich um den gleichen Wert, der das erste WWPN ist, das durch den nachfolgenden " [**generatewwpn**](generatewwpn-msvm-virtualsystemmanagementservice.md)"-Befehl generiert wird. Er wird im Zeichen folgen Format als "01:23:45:67:89: ab: CD: EF" formatiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
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
</dt> </dl>

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

[**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




