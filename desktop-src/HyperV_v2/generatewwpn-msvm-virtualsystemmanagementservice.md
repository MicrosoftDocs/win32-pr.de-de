---
description: Generiert einen Satz von WWPNs (World Wide Port Names).
ms.assetid: 36f393eb-6f34-4ae3-a976-c5da60211f3e
title: GenerateWwpn-Methode der Msvm_VirtualSystemManagementService-Klasse
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
ms.openlocfilehash: 1952954d107185fdcc31634b9d0e19bd4cd3450db5a63d78aa3ef823cdf38afe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119532520"
---
# <a name="generatewwpn-method-of-the-msvm_virtualsystemmanagementservice-class"></a>GenerateWwpn-Methode der Msvm \_ VirtualSystemManagementService-Klasse

Generiert einen Satz von WWPNs (World Wide Port Names). Die WWPNs werden innerhalb des vorkonfigurierten Bereichs generiert, der durch die Eigenschaften **MinimumWWPNAddress** und **MaximumWWPNAddress** der [**Msvm \_ VirtualSystemManagementServiceSettingData-Klasse**](msvm-virtualsystemmanagementservicesettingdata.md) definiert wird. Wenn die gültige Anzahl von WWPNs, die generiert werden können, kleiner als die angeforderte Zahl ist, weisen die verbleibenden Einträge im *GeneratedWwpn-Array* den ungültigen Eintrag "00000000000000000" auf, und der Rückgabewert zeigt erfolg (0) an.

## <a name="syntax"></a>Syntax


```mof
uint32 GenerateWwpn(
  [in]  uint32 NumberOfWwpns,
  [out] string GeneratedWwpn[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NumberOfWwpns* \[ In\]
</dt> <dd>

Die Anzahl der zu generierenden WWPNs.

</dd> <dt>

*GeneratedWwpn* \[ out\]
</dt> <dd>

Ein Array von Zeichenfolgen, von denen jede eine generierte WWPN enthält. Sie wird in Zeichenfolgenform als "01:23:45:67:89:ab:cd:ef" formatiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
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

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




