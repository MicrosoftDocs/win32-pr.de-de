---
description: Werte Werte definieren die Reihenfolge, in der der Filter Graph-Manager versucht, während der Diagramm Bildung Filter hinzuzufügen.
ms.assetid: 9e026675-e0a9-4c82-9b57-ab0e7d9592ea
title: Verdienst (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 947a13d78f58c12c236ec31f0eeee1dc6d44f1d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361268"
---
# <a name="merit"></a>Verdienst

Werte Werte definieren die Reihenfolge, in der der Filter Graph-Manager versucht, während der Diagramm Bildung Filter hinzuzufügen.

<dl> <span id="MERIT_PREFERRED"></span><span id="merit_preferred"></span>**Verdienst \_ Bevorzugter** (0x800000) Wert <span id="MERIT_NORMAL"></span> <span id="merit_normal"></span> **\_ Normal** (0x600000) verdient <span id="MERIT_UNLIKELY"></span> <span id="merit_unlikely"></span> nicht **\_ wahrscheinliche** (0x400000) Wert <span id="MERIT_DO_NOT_USE"></span> <span id="merit_do_not_use"></span> **\_ \_ nicht \_ verwenden** (0x200.000) Verdienst- <span id="MERIT_SW_COMPRESSOR"></span> <span id="merit_sw_compressor"></span> **\_ SW- \_ Kompressor** (0x100000) <span id="MERIT_HW_COMPRESSOR"></span> <span id="merit_hw_compressor"></span> **Merit \_ HW- \_ Kompressor** (0x100050)
</dl>

## <a name="remarks"></a>Bemerkungen

Jeder Filter ist mit einem Verdienst Wert registriert. Wenn der Filter Graph-Manager ein Diagramm erstellt, listet er alle Filter auf, die mit dem richtigen Medientyp registriert sind. Anschließend werden die Werte in der Reihenfolge ihrer Vorzüge, von der höchsten zum niedrigsten, ausprobiert. (Es werden zusätzliche Kriterien verwendet, um zwischen Filtern mit gleichem Verdienst auszuwählen.) Es werden niemals Filter mit einem Wert vom Wert "Value" **verwendet, \_ der \_ nicht \_ verwendet** wird.

Ein Filter, der nie für die normale Wiedergabe berücksichtigt werden sollte, sollte den Vorteil haben, dass **\_ Sie \_ nicht \_** oder weniger verwenden. Filter können mit zwischen Werten registriert werden, die nicht von dieser Enumeration definiert werden, wie z. b. "Wert **\_ Normal** + 1".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Konstanten und GUIDs](constants-and-guids.md)
</dt> <dt>

[Richtlinien zum Registrieren von Filtern](guidelines-for-registering-filters.md)
</dt> <dt>

[Intelligent Connect](intelligent-connect.md)
</dt> </dl>

 

 




