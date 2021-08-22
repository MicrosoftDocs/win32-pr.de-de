---
description: Deklariert ein Objekt als pick-any-Konstante, um redundantes erneutes Laden dieses Objekts zu vermeiden, wenn es an mehreren Stellen in der DirectXMath-Bibliothek verwendet (und deklariert) wird.
ms.assetid: FDE5C004-9E8E-4890-8FDC-987C1569D8E5
title: XMGLOBALCONST-Makro
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be72254865aed46de86955c2a27a4d73351311c5aa63a44a6e218be7a3915d1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119118000"
---
# <a name="xmglobalconst-macro"></a>XMGLOBALCONST-Makro

Deklariert ein Objekt als *pick-any-Konstante,* um redundantes erneutes Laden dieses Objekts zu vermeiden, wenn es an mehreren Stellen in der DirectXMath-Bibliothek verwendet (und deklariert) wird.

## <a name="syntax"></a>Syntax

``` syntax
#define XMGLOBALCONST  extern const __declspec(selectany)
```

## <a name="remarks"></a>Hinweise

Die Verwendung von XMGLOBALCONST ermöglicht die Angabe globaler Konstanten. Dies trägt dazu bei, die Größe des Datensegments einer Anwendung zu reduzieren, die Erstellung und Zerstörung redundanter Objekte zu vermeiden und die Last und Speichervorgänge zu reduzieren.

## <a name="requirements"></a>Anforderungen

**Header:** Deklariert in DirectXMath.h.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectXMath-Bibliotheksmakros](ovw-xnamath-reference-macros.md)
</dt> <dt>

[Globale Konstanten in der DirectXMath-Bibliothek](pg-xnamath-internals.md)
</dt> <dt>

[selectany](/previous-versions/visualstudio/visual-studio-6.0/aa273550(v=vs.60))
</dt> <dt>

[Declspec](/previous-versions/visualstudio/visual-studio-6.0/aa273692(v=vs.60))
</dt> </dl>

 

 
