---
description: Gibt einen Speicherblock frei, der von RtlAllocateHeap aus einem Heap zugeordnet wurde.
ms.assetid: 0A08FB6B-23A3-450B-8745-AEB927CEB7BB
title: RtlFreeHeap-Funktion (Ntifs.h)
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
ms.openlocfilehash: 3dd46808c898cd934bbb4ee8804027bcb926e4a5cd07eb1521e2814a2c4b0e1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538073"
---
# <a name="rtlfreeheap-function"></a>RtlFreeHeap-Funktion

Gibt einen Speicherblock frei, der von [**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap)aus einem Heap zugeordnet wurde.

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

*HeapHandle* \[ In\]
</dt> <dd>

Ein Handle für den Heap, dessen Speicherblock freigegeben werden soll. Dieser Parameter ist ein Handle, das von [**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap)zurückgegeben wird.

</dd> <dt>

*Flags* \[ in, optional\]
</dt> <dd>

Eine Gruppe von Flags, die Aspekte des Freigebens eines Speicherblocks steuern. Wenn Sie den folgenden Wert angeben, wird der entsprechende Wert überschrieben, der im *Flags-Parameter* angegeben wurde, als der Heap von [**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap)erstellt wurde.



| Flag                           | Bedeutung                                                                                   |
|--------------------------------|-------------------------------------------------------------------------------------------|
| HEAP \_ OHNE \_ SERIALISIERUNG<br/> | Der gegenseitige Ausschluss wird nicht verwendet, wenn **RtlFreeHeap** auf den Heap zugreift. <br/> |



 

</dd> <dt>

*HeapBase* \[ In\]
</dt> <dd>

Ein Zeiger auf den freizugebende Speicherblock. Dieser Zeiger wird von [**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap)zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn der Block erfolgreich freigegeben wurde. **Andernfalls FALSE.**

> [!Note]  
> Ab Windows 8 wird der Rückgabewert als **LOGICAL** eingegeben, der eine andere Größe als **BOOLEAN** hat.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                    |
| Zielplattform<br/>          | <dl> <dt>[Universell](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| Header<br/>                   | <dl> <dt>Ntifs.h (include Ntifs.h)</dt> </dl>                                    |
| Bibliothek<br/>                  | <dl> <dt>Ntdll.lib</dt> </dl>                                                    |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl>                                                    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap)
</dt> <dt>

[**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap)
</dt> <dt>

[**RtlDestroyHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtldestroyheap)
</dt> </dl>

 

 
