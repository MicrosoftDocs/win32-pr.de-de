---
description: Deklariert ein Objekt als eine pick-any-Konstante, um redundante Neuladungen dieses Objekts zu vermeiden, wenn es an mehreren Stellen in der directxmath-Bibliothek verwendet (und deklariert) wird.
ms.assetid: FDE5C004-9E8E-4890-8FDC-987C1569D8E5
title: Xmglobalconst-Makro
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6675b17138fca66e293321a9d848262a8bffc94e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355575"
---
# <a name="xmglobalconst-macro"></a>Xmglobalconst-Makro

Deklariert ein Objekt als eine *pick-any-* Konstante, um redundante Neuladungen dieses Objekts zu vermeiden, wenn es an mehreren Stellen in der directxmath-Bibliothek verwendet (und deklariert) wird.

## <a name="syntax"></a>Syntax

``` syntax
#define XMGLOBALCONST  extern const __declspec(selectany)
```

## <a name="remarks"></a>Bemerkungen

Die Verwendung von xmglobalconst ermöglicht die Angabe von globalen Konstanten. Dies trägt dazu bei, die Größe des Datensegments einer Anwendung zu reduzieren, eine redundante Objekt Erstellung und-Zerstörung zu vermeiden und Lade-und Speichervorgänge zu verringern.

## <a name="requirements"></a>Anforderungen

**Header:** Deklariert in "directxmath. h".

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Directxmath-Bibliotheks Makros](ovw-xnamath-reference-macros.md)
</dt> <dt>

[Globale Konstanten in der directxmath-Bibliothek](pg-xnamath-internals.md)
</dt> <dt>

[selectany](/previous-versions/visualstudio/visual-studio-6.0/aa273550(v=vs.60))
</dt> <dt>

[declspec](/previous-versions/visualstudio/visual-studio-6.0/aa273692(v=vs.60))
</dt> </dl>

 

 
