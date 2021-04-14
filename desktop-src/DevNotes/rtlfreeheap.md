---
description: Gibt einen Speicherblock frei, der von einem Heap von rtlzucateheap zugewiesen wurde.
ms.assetid: 0A08FB6B-23A3-450B-8745-AEB927CEB7BB
title: RtlFreeHeap-Funktion (ntifs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlFreeHeap
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: e51994c4bcd941bc96575eb3fdbb45d4111c1aeb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523587"
---
# <a name="rtlfreeheap-function"></a>RtlFreeHeap-Funktion

Gibt einen Speicherblock frei, der von einem Heap von [**rtlzucateheap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap)zugewiesen wurde.

## <a name="syntax"></a>Syntax


```C++
BOOLEAN RtlFreeHeap(
  _In_     PVOID HeapHandle,
  _In_opt_ ULONG Flags,
  _In_     PVOID HeapBase
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Heaphandle* \[ in\]
</dt> <dd>

Ein Handle für den Heap, dessen Speicherblock freigegeben werden soll. Dieser Parameter ist ein Handle, das von [**rtlkreateheap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap)zurückgegeben wird.

</dd> <dt>

*Flags* \[ in, optional\]
</dt> <dd>

Ein Satz von Flags, die Aspekte der Freigabe eines Speicherblocks steuern. Wenn Sie den folgenden Wert angeben, wird der entsprechende Wert überschrieben, der im *Flags* -Parameter angegeben wurde, als der Heap von [**rtlkreateheap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap)erstellt wurde.



| Flag                           | Bedeutung                                                                                   |
|--------------------------------|-------------------------------------------------------------------------------------------|
| Heap ist \_ nicht \_ serialisiert.<br/> | Der gegenseitige Ausschluss wird nicht verwendet, wenn **RtlFreeHeap** auf den Heap zugreift. <br/> |



 

</dd> <dt>

*Heapbase* \[ in\]
</dt> <dd>

Ein Zeiger auf den Speicherblock, der freigegeben werden soll. Dieser Zeiger wird von [**rtldepcateheap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap)zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt " **true** " zurück, wenn der Block erfolgreich freigegeben wurde. Andernfalls **false** .

> [!Note]  
> Ab Windows 8 wird der Rückgabewert als **logisch** typisiert, was eine andere Größe aufweist als der **boolesche** Wert.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                    |
| Zielplattform<br/>          | <dl> <dt>[Universell](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| Header<br/>                   | <dl> <dt>Ntifs. h (ntifs. h einschließen)</dt> </dl>                                    |
| Bibliothek<br/>                  | <dl> <dt>Ntdll. lib</dt> </dl>                                                    |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl>                                                    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Rtldepcateheap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap)
</dt> <dt>

[**Rtlkreateheap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap)
</dt> <dt>

[**Rtldestroyheap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtldestroyheap)
</dt> </dl>

 

 
