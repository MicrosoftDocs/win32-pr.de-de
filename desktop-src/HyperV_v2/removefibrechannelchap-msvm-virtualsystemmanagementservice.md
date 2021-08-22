---
description: Entfernt DH-CHAP-Parameter (Diffie Hellman – Challenge Handshake Authentication Protocol) aus einem synthetischen Fibre Channel port in einem virtuellen Computer.
ms.assetid: f15673e2-287d-4e87-bee4-6c0f5f9178c8
title: RemoveFibreChannelChap-Methode der Msvm_VirtualSystemManagementService Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveFibreChannelChap
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9b934839f6d908594ee58f0838c884fdedc48f372de061482ddf2147123a351c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147793"
---
# <a name="removefibrechannelchap-method-of-the-msvm_virtualsystemmanagementservice-class"></a>RemoveFibreChannelChap-Methode der Msvm \_ VirtualSystemManagementService-Klasse

Entfernt DH-CHAP-Parameter (Diffie Hellman – Challenge Handshake Authentication Protocol) aus einem synthetischen Fibre Channel port in einem virtuellen Computer. Diese Methode kann nicht ausgeführt werden, wenn der virtuelle Computer ausgeführt wird.

## <a name="syntax"></a>Syntax


```mof
uint32 RemoveFibreChannelChap(
  [in] string FcPortSettings[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FcPortSettings* \[ In\]
</dt> <dd>

Ein Array von Zeichenfolgen, die eine eingebettete Instanz der [**Msvm \_ SyntheticFcPortSettingData-Klasse**](msvm-syntheticfcportsettingdata.md) enthalten, die die synthetischen Fibre Channel-Ports definieren, aus denen die DH-CHAP-Parameter entfernt werden sollen. Die **InstanceID-Eigenschaft** jeder dieser Instanzen identifiziert die zu ändernden Elemente.

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

 

 




