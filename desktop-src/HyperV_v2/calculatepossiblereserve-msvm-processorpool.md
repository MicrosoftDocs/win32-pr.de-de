---
description: Diese Methode wird verwendet, um die tatsächliche Reserve zu finden, bei der der Eingabeparameter die Anzahl der Prozessoren virtueller Maschinen ist, für die die Reservierung berechnet wird.
ms.assetid: C0497900-00F3-4975-9D12-C82C13C03D8E
title: Calculatepossiblereserve-Methode der Msvm_ProcessorPool-Klasse
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
ms.openlocfilehash: c7f88bcf3295b1792fca6be88ae0c9282b72646e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756624"
---
# <a name="calculatepossiblereserve-method-of-the-msvm_processorpool-class"></a>Calculatepossiblereserve-Methode der MSVM \_ processorpool-Klasse

Diese Methode wird verwendet, um die tatsächliche Reserve zu finden, bei der der Eingabeparameter die Anzahl der Prozessoren virtueller Maschinen ist, für die die Reservierung berechnet wird. Diese Methode ist erforderlich, da die Reservierung von Prozessorressourcen stark von der Anzahl der Prozessoren abhängig ist, die parallel geplant werden müssen.

## <a name="syntax"></a>Syntax


```mof
uint32 CalculatePossibleReserve(
  [in] uint16 ProcessorCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ProcessorCount* \[ in\]
</dt> <dd>

Typ: **UInt16**

Die Anzahl der Prozessoren virtueller Maschinen, für die die Reservierung berechnet wird. Der Maximalwert für diese Eigenschaft ist die Anzahl logischer Prozessoren für den Host Computer.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Die CPU-Ressourcen Menge, die für einen virtuellen Computer reserviert werden kann.

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die [**MSVM \_ processorpool**](msvm-processorpool.md) -Klasse kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**MSVM \_ processorpool**](msvm-processorpool.md)
</dt> </dl>

 

