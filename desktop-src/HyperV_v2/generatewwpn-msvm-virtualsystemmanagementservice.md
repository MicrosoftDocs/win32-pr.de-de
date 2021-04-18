---
description: Generiert einen Satz von World Wide Port Names (WWPNs).
ms.assetid: 36f393eb-6f34-4ae3-a976-c5da60211f3e
title: Generatewwpn-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GenerateWwpn
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b0efba6a24a7e4f7e6826f91930cb69b4b54f3cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368115"
---
# <a name="generatewwpn-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Generatewwpn-Methode der MSVM \_ virtualsystemmanagementservice-Klasse

Generiert einen Satz von World Wide Port Names (WWPNs). Die WWPNs werden aus dem vorkonfigurierten Bereich generiert, der in den Eigenschaften **minimumwwpnaddress** und **maximumwwpnaddress** der [**MSVM \_ virtualsystemmanagementservicesettingdata**](msvm-virtualsystemmanagementservicesettingdata.md) -Klasse definiert ist. Wenn die gültige Anzahl von WWPNs, die generiert werden können, kleiner ist als die angeforderte Anzahl, haben die restlichen Einträge im *generatedwwpn* -Array den ungültigen Eintrag "0000000000000000", und der Rückgabewert gibt Erfolg (0) an.

## <a name="syntax"></a>Syntax


```mof
uint32 GenerateWwpn(
  [in]  uint32 NumberOfWwpns,
  [out] string GeneratedWwpn[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Anzahl der WWPNs* \[ in\]
</dt> <dd>

Die Anzahl der zu generierenden WWPNs.

</dd> <dt>

*Generatedwwpn* \[ vorgenommen\]
</dt> <dd>

Ein Array von Zeichen folgen, von denen jede einen generierten WWPN enthält. Er wird im Zeichen folgen Format als "01:23:45:67:89: ab: CD: EF" formatiert.

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

 

 




