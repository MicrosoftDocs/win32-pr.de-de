---
description: Kopiert den Inhalt eines Quell Speicherblocks in einen Zielspeicher Block und unterstützt überlappende Quell-und Zielspeicher Blöcke.
ms.assetid: D374F14D-24C7-4771-AD40-3AC37E7A2D2F
title: Rtlmuvememory-Funktion (WDM. h)
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
ms.openlocfilehash: 65f8c8490224213e0bef27fab5239a21eca24344
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340112"
---
# <a name="rtlmovememory-function"></a>Rtlmuvememory-Funktion

Kopiert den Inhalt eines Quell Speicherblocks in einen Zielspeicher Block und unterstützt überlappende Quell-und Zielspeicher Blöcke.

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

*Ziel* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf den Zielspeicher Block, in den die Bytes kopiert werden sollen.

</dd> <dt>

*Quelle* \[ in\]
</dt> <dd>

Ein Zeiger auf den Quell Speicherblock, aus dem die Bytes kopiert werden sollen.

</dd> <dt>

*Länge* \[ in\]
</dt> <dd>

Die Anzahl der Bytes, die aus der Quelle in das Ziel kopiert werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Keine

## <a name="remarks"></a>Bemerkungen

Der Quell Speicherblock, der durch *Quelle* und *Länge* definiert wird, kann den Zielspeicher Block überlappen, der durch das *Ziel* und die *Länge* definiert wird.

Die [**rtlcopymemory**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlcopymemory) -Routine läuft schneller als **rtlmuvememory**, aber **rtlcopymemory** erfordert, dass sich die Quell-und Zielspeicher Blöcke nicht überlappen.

Aufrufer von **rtlmuvememory** können in beliebiger unql ausgeführt werden, wenn sich die Quell-und Zielspeicher Blöcke im nicht auslagerenden System Arbeitsspeicher befinden. Andernfalls muss der Aufrufer auf der Ebene "iriql <= APC" ausgeführt werden \_ .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                    |
| Zielplattform<br/>          | <dl> <dt>[Universell](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl> |
| Header<br/>                   | <dl> <dt>WDM. h (Include WDM. h, ntddk. h oder ntifs. h)</dt> </dl>                   |
| Bibliothek<br/>                  | <dl> <dt>Ntdll. lib</dt> </dl>                                                    |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl>                                                    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Rtlcopymemory**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlcopymemory)
</dt> </dl>

 

 
