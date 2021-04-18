---
title: Große ganze Zahlen
description: Die großen ganzzahligen Funktionen und Strukturen haben ursprünglich 64-Bit-Werte auf 32-Bit-Fenstern unterstützt.
ms.assetid: db4ffbd5-d9e4-4c95-83cc-6f0691c080d2
keywords:
- große ganze Zahlen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ab6276ff6879ce5b72f198e3ccbd247f456e70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339086"
---
# <a name="large-integers"></a>Große ganze Zahlen

Die großen ganzzahligen Funktionen und Strukturen haben ursprünglich 64-Bit-Werte auf 32-Bit-Fenstern unterstützt. Nun unterstützt der C-Compiler möglicherweise ganzzahlige 64-Bit-Ganzzahlen. Beispielsweise unterstützt Microsoft Visual C++ den ganzzahligen Typ [**\_ \_ Int64**](/windows/desktop/Midl/--int64) . Weitere Informationen finden Sie in der Dokumentation, die in Ihrem C-Compiler enthalten ist.

Informationen zu ganzzahligen 64-Bit-Zahlen auf 64-Bit-Fenstern finden Sie [unter den neuen Datentypen](/windows/desktop/WinProg64/the-new-data-types).

## <a name="large-integer-operations"></a>Große ganzzahlige Vorgänge

Anwendungen können mit der [**Int32x32To64**](/windows/desktop/api/Winnt/nf-winnt-int32x32to64) -Funktion und der [**UInt32x32To64**](/windows/desktop/api/Winnt/nf-winnt-uint32x32to64) -Funktion eine 64 ganze Zahl mit oder 32 ohne Vorzeichen oder ganze Zahlen mit Vorzeichen oder ohne Vorzeichen multiplizieren. Anwendungen können Bits in 64-Bit-Werten mithilfe der Funktionen [**Int64ShllMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shllmod32), [**Int64ShraMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shramod32)und [**Int64ShrlMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shrlmod32) nach links oder rechts verschieben. Diese Funktionen bieten logische und arithmetische Verschiebungen.

Anwendungen können auch 32-Bit-Werte in einem einzelnen Vorgang multiplizieren und teilen, indem Sie die [**muldiv**](/windows/desktop/api/Winbase/nf-winbase-muldiv) -Funktion verwenden. Obwohl das Ergebnis des Vorgangs ein 32-Bit-Wert ist, speichert die Funktion das Zwischenergebnis als 64-Bit-Wert, sodass die Informationen nicht verloren gehen, wenn große 32-Bit-Werte multipliziert und dividiert werden.

## <a name="large-integer-reference"></a>Verweis auf große Ganzzahl

-   [Große ganzzahlige Funktionen](large-integer-functions.md)
-   [Large Integer-Strukturen](large-integer-structures.md)

 

 