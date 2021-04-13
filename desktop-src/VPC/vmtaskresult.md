---
title: Vmtaskresult-Enumeration (vpccominterfaces. h)
description: Gibt das Ergebnis einer Aufgabe an.
ms.assetid: 34aa193a-466d-492e-8648-467c286a8c11
keywords:
- Vmtaskresult-Enumeration virtueller PC
topic_type:
- apiref
api_name:
- VMTaskResult
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 903425ca8036e1862df7042f16946fc0f2e9cc7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518908"
---
# <a name="vmtaskresult-enumeration"></a>Vmtaskresult-Enumeration

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Gibt das Ergebnis einer Aufgabe an.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  vmTaskResult_Success                      = 0,
  vmTaskResult_Cancelled                    = 1,
  vmTaskResult_UnexpectedError              = 2,
  vmTaskResult_OutOfMemoryError             = 3,
  vmTaskResult_DiskRelatedError             = 4,
  vmTaskResult_IncompatibleSavedStateError  = 5,
  vmTaskResult_TimeOutError                 = 6,
  vmTaskResult_IllegalValueError            = 7,
  vmTaskResult_ThreadCrashError             = 8,
  vmTaskResult_ShutdownAbort                = 9
} VMTaskResult;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="vmTaskResult_Success"></span><span id="vmtaskresult_success"></span><span id="VMTASKRESULT_SUCCESS"></span>**vmtaskresult \_ erfolgreich**
</dt> <dd>

Der Task wurde erfolgreich ausgeführt.

</dd> <dt>

<span id="vmTaskResult_Cancelled"></span><span id="vmtaskresult_cancelled"></span><span id="VMTASKRESULT_CANCELLED"></span>**vmtaskresult \_ abgebrochen**
</dt> <dd>

Der Task wurde abgebrochen.

</dd> <dt>

<span id="vmTaskResult_UnexpectedError"></span><span id="vmtaskresult_unexpectederror"></span><span id="VMTASKRESULT_UNEXPECTEDERROR"></span>**vmtaskresult \_ unexpectederror**
</dt> <dd>

Unerwarteter Fehler bei der Aufgabe.

</dd> <dt>

<span id="vmTaskResult_OutOfMemoryError"></span><span id="vmtaskresult_outofmemoryerror"></span><span id="VMTASKRESULT_OUTOFMEMORYERROR"></span>**vmtaskresult \_ outo-MemoryError**
</dt> <dd>

Es war nicht genügend Arbeitsspeicher vorhanden, um den Task abzuschließen.

</dd> <dt>

<span id="vmTaskResult_DiskRelatedError"></span><span id="vmtaskresult_diskrelatederror"></span><span id="VMTASKRESULT_DISKRELATEDERROR"></span>**vmtaskresult \_ diskrelatederror**
</dt> <dd>

Fehler bei der Aufgabe beim Schreiben auf den Datenträger (stellen Sie sicher, dass genügend Speicherplatz vorhanden ist).

</dd> <dt>

<span id="vmTaskResult_IncompatibleSavedStateError"></span><span id="vmtaskresult_incompatiblesavedstateerror"></span><span id="VMTASKRESULT_INCOMPATIBLESAVEDSTATEERROR"></span>**vmtaskresult \_ incompatiblesavedstateerror**
</dt> <dd>

Die virtuelle Maschine konnte nicht wieder hergestellt werden, da der gespeicherte Zustand nicht kompatibel war.

</dd> <dt>

<span id="vmTaskResult_TimeOutError"></span><span id="vmtaskresult_timeouterror"></span><span id="VMTASKRESULT_TIMEOUTERROR"></span>**vmtaskresult \_ timeouterror**
</dt> <dd>

Timeout beim Task.

</dd> <dt>

<span id="vmTaskResult_IllegalValueError"></span><span id="vmtaskresult_illegalvalueerror"></span><span id="VMTASKRESULT_ILLEGALVALUEERROR"></span>**vmtaskresult \_ illegalvalueerror**
</dt> <dd>

Beim Verarbeiten der Aufgabe wurde ein unzulässiger Einstellungs Wert gelesen.

</dd> <dt>

<span id="vmTaskResult_ThreadCrashError"></span><span id="vmtaskresult_threadcrasherror"></span><span id="VMTASKRESULT_THREADCRASHERROR"></span>**vmtaskresult \_ threadcrasherror**
</dt> <dd>

Ein dem Task zugeordneter Thread ist abgestürzt.

</dd> <dt>

<span id="vmTaskResult_ShutdownAbort"></span><span id="vmtaskresult_shutdownabort"></span><span id="VMTASKRESULT_SHUTDOWNABORT"></span>**vmtaskresult \_ shutdownabort**
</dt> <dd>

Das angeforderte Herunterfahren wurde abgebrochen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmtask:: result**](ivmtask-result.md)
</dt> </dl>

 

