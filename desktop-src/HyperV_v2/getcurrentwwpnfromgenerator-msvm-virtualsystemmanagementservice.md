---
description: Bietet die Möglichkeit, eine Vorschau des aktuellen WWPN (World Wide Port Name) anzuzeigen, ohne dass die WWPN reserviert ist.
ms.assetid: 7fc02099-744e-4a56-ae4b-1f5fd6a1eb45
title: GetCurrentWwpnFromGenerator-Methode der Msvm_VirtualSystemManagementService-Klasse
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
ms.openlocfilehash: 196ad781075128eab42c6daabf7d6ccd6906df1e67e348ebea0d9418cbb08c24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393282"
---
# <a name="getcurrentwwpnfromgenerator-method-of-the-msvm_virtualsystemmanagementservice-class"></a>GetCurrentWwpnFromGenerator-Methode der Msvm \_ VirtualSystemManagementService-Klasse

Bietet die Möglichkeit, eine Vorschau des aktuellen WWPN (World Wide Port Name) anzuzeigen, ohne dass die WWPN reserviert ist. Die WWPN wird innerhalb des vorkonfigurierten Bereichs generiert, der durch die Eigenschaften **MinimumWWPNAddress** und **MaximumWWPNAddress** der [**Msvm \_ VirtualSystemManagementServiceSettingData-Klasse**](msvm-virtualsystemmanagementservicesettingdata.md) definiert wird. Wenn der durch diese Eigenschaften definierte Bereich erschöpft ist, weist die generierte WWPN den ungültigen Eintrag "0000000000000000000" auf, und der Rückgabewert zeigt erfolg (0) an.

## <a name="syntax"></a>Syntax


```mof
uint32 GetCurrentWwpnFromGenerator(
  [out] string CurrentWwpn
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*CurrentWwpn* \[ out\]
</dt> <dd>

Eine Zeichenfolge mit dem Wert der aktuellen WWPN, wie vom WWPN-Generator verwendet. Dies ist der gleiche Wert wie der erste WWPN, der durch den nachfolgenden Aufruf von [**GenerateWwpn**](generatewwpn-msvm-virtualsystemmanagementservice.md)generiert wird. Sie wird in Zeichenfolgenform als "01:23:45:67:89:ab:cd:ef" formatiert.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




