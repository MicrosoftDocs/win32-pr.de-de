---
description: Werte für Die Werte definieren die Reihenfolge, in der der Filter Graph Manager versucht, während der Grapherstellung Filter hinzuzufügen.
ms.assetid: 9e026675-e0a9-4c82-9b57-ab0e7d9592ea
title: Vererbt (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a55c112f1a08d63e45d5385f525371ae9642c1b01a1b4af5d7747b042efffe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073014"
---
# <a name="merit"></a>Verdienst

Werte für Die Werte definieren die Reihenfolge, in der der Filter Graph Manager versucht, während der Grapherstellung Filter hinzuzufügen.

<dl> <span id="MERIT_PREFERRED"></span><span id="merit_preferred"></span>**VERERZUNG \_ BEVORZUGTER** (0x800000) <span id="MERIT_NORMAL"></span> <span id="merit_normal"></span> **NORMALWERT \_** (0x600000) <span id="MERIT_UNLIKELY"></span> <span id="merit_unlikely"></span> **\_ UNWAHRSCHEINLICHER** (0x400000) NICHT <span id="MERIT_DO_NOT_USE"></span> <span id="merit_do_not_use"></span> **\_ \_ \_** VERWENDETER (0x200000) <span id="MERIT_SW_COMPRESSOR"></span> <span id="merit_sw_compressor"></span> **VERWENDUNGSWEISUNGSWEISUNG \_ \_** (0X100000) <span id="MERIT_HW_COMPRESSOR"></span> <span id="merit_hw_compressor"></span> **VERWEISUNGS-HW-HW- \_ \_ (0x100050)**
</dl>

## <a name="remarks"></a>Hinweise

Jeder Filter wird mit einem Wert registriert. Wenn der Filtergraph-Manager ein Diagramm erstellt, listet er alle Filter auf, die mit dem richtigen Medientyp registriert sind. Anschließend werden sie in der Reihenfolge der Leistungen von der höchsten bis zur niedrigsten versucht. (Es werden zusätzliche Kriterien verwendet, um zwischen Filtern mit gleicher Leistung zu wählen.) Filter mit einem Wert, der kleiner als oder gleich DEM WERT IST, werden nie von **DER USE-Klasse \_ \_ \_ verwendet.**

Ein Filter, der nie für die normale Wiedergabe in Betracht gezogen werden sollte, sollte den Vorteil **HABEN, dass DER WERT NICHT \_ \_ \_ VERWENDET** oder kleiner ist. Filter können mit Zwischenwerten registriert werden, die nicht durch diese Enumeration definiert sind, z. **B. WENN \_ NORMAL** + 1.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Konstanten und GUIDs](constants-and-guids.md)
</dt> <dt>

[Richtlinien für das Registrieren von Filtern](guidelines-for-registering-filters.md)
</dt> <dt>

[Intelligente Verbinden](intelligent-connect.md)
</dt> </dl>

 

 




