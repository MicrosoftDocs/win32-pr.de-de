---
description: Kopiert den Inhalt eines Quellspeicherblocks in einen Zielspeicherblock und unterstützt überlappende Quell- und Zielspeicherblöcke.
ms.assetid: D374F14D-24C7-4771-AD40-3AC37E7A2D2F
title: RtlMoveMemory-Funktion (Wdm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlMoveMemory
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: bf4366633de321e27f6d3cdc0396fcdce81b0dac30b0d09a4c2c4675706d939e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161662"
---
# <a name="rtlmovememory-function"></a>RtlMoveMemory-Funktion

Kopiert den Inhalt eines Quellspeicherblocks in einen Zielspeicherblock und unterstützt überlappende Quell- und Zielspeicherblöcke.

## <a name="syntax"></a>Syntax


```C++
VOID RtlMoveMemory(
  _Out_       VOID UNALIGNED *Destination,
  _In_  const VOID UNALIGNED *Source,
  _In_        SIZE_T         Length
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ziel* \[ out\]
</dt> <dd>

Ein Zeiger auf den Zielspeicherblock, in den die Bytes kopiert werden.

</dd> <dt>

*Quelle* \[ In\]
</dt> <dd>

Ein Zeiger auf den Quellspeicherblock, aus dem die Bytes kopiert werden.

</dd> <dt>

*Länge* \[ In\]
</dt> <dd>

Die Anzahl der Bytes, die aus der Quelle in das Ziel kopiert werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Keine

## <a name="remarks"></a>Bemerkungen

Der Quellspeicherblock, der durch *Quelle* und *Länge* definiert wird, kann den Zielspeicherblock überlappen, der durch *Destination* und Length *definiert wird.*

Die [**RtlCopyMemory-Routine**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlcopymemory) wird schneller als **RtlMoveMemory** ausgeführt, **aber RtlCopyMemory** erfordert, dass sich die Quell- und Zielspeicherblöcke nicht überschneiden.

Aufrufer von **RtlMoveMemory** können in jedem IRQL ausgeführt werden, wenn sich die Quell- und Zielspeicherblöcke im nicht auspageierten Systemspeicher befinden. Andernfalls muss der Aufrufer unter IRQL <= APC LEVEL \_ ausgeführt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                    |
| Zielplattform<br/>          | <dl> <dt>[Universell](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| Header<br/>                   | <dl> <dt>Wdm.h (einschließlich Wdm.h, Ntddk.h oder Ntifs.h)</dt> </dl>                   |
| Bibliothek<br/>                  | <dl> <dt>Ntdll.lib</dt> </dl>                                                    |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl>                                                    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**RtlCopyMemory**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlcopymemory)
</dt> </dl>

 

 
