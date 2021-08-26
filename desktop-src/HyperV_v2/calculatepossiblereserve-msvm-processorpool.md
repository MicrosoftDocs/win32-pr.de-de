---
description: Diese Methode wird verwendet, um die tatsächliche Reserve zu ermitteln, wobei der Eingabeparameter die Anzahl der VM-Prozessoren ist, für die die Reserve berechnet wird.
ms.assetid: C0497900-00F3-4975-9D12-C82C13C03D8E
title: CalculatePossibleReserve-Methode der Msvm_ProcessorPool-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ProcessorPool.CalculatePossibleReserve
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 06cfa01dd89392c05f460462d8bda5898b47d90b6e027fa885bf039f62488cc3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042070"
---
# <a name="calculatepossiblereserve-method-of-the-msvm_processorpool-class"></a>CalculatePossibleReserve-Methode der Msvm \_ ProcessorPool-Klasse

Diese Methode wird verwendet, um die tatsächliche Reserve zu ermitteln, wobei der Eingabeparameter die Anzahl der VM-Prozessoren ist, für die die Reserve berechnet wird. Diese Methode ist erforderlich, da die Reservierung von Prozessorressourcen stark von der Anzahl der Prozessoren abhängt, die parallel geplant werden müssen.

## <a name="syntax"></a>Syntax


```mof
uint32 CalculatePossibleReserve(
  [in] uint16 ProcessorCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ProcessorCount* \[ In\]
</dt> <dd>

Typ: **uint16**

Die Anzahl der VM-Prozessoren, für die die Reserve berechnet wird. Der Maximale Wert für diese Eigenschaft ist die Logische Prozessoranzahl für den Hostcomputer.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **uint32**

Die Menge der CPU-Ressourcen, die für einen virtuellen Computer reserviert werden können.

## <a name="remarks"></a>Hinweise

Der Zugriff auf die [**Msvm \_ ProcessorPool-Klasse**](msvm-processorpool.md) kann durch UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[**Msvm \_ ProcessorPool**](msvm-processorpool.md)
</dt> </dl>

 

