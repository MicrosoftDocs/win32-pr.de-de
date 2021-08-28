---
description: Permutiert die Komponenten von zwei Vektoren, um einen neuen Vektor zu erstellen.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorpermute(xmvector,xmvector)
title: XMVectorPermute-Vorlage (DirectXMath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd3f7071edaf659991c1294d29a154d3a319d5faee982537025e107cf9621f55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978670"
---
# <a name="xmvectorpermute-template"></a>XMVectorPermute-Vorlage

Permutiert die Komponenten von zwei Vektoren, um einen neuen Vektor zu erstellen.

## <a name="syntax"></a>Syntax

``` syntax
template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW> XMVECTOR XMVectorPermute(
  [in]  XMVECTOR V1,
  [in]  XMVECTOR V2
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="V1"></span><span id="v1"></span>*V1*
</dt> <dd>

\[in \] Erster Vektor.

</dd> <dt>

<span id="V2"></span><span id="v2"></span>*V2*
</dt> <dd>

\[in \] Zweiter Vektor.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den permutierten Vektor zurück, der sich aus der Kombination der Quellvektoren ergibt.

## <a name="remarks"></a>Hinweise

Wenn alle 4 Indizes nur auf einen einzelnen Vektor verweisen (d. h., sie befinden sich alle im Bereich 0-3 oder alle im Bereich 4-7), verwenden Sie stattdessen [**XMVectorSwizzle,**](xmvectorswizzle-template.md) um eine bessere Leistung zu erzielen.

Beachten Sie, dass die Bibliothek Vorlagenspezialisierungen auf einigen Plattformen verwendet, um die Leistung zu verbessern. Nicht jeder mögliche Spiegelfall wird für diese Sonderfälle implementiert. Bevorzugen Sie daher Permutes, bei denen das X-Element des resultierenden Vektors aus dem V1-Parameter und nicht aus dem V2-Parameter stammt. Verwenden Sie z. B. lieber `XMVectorPermute<0,1,4,5>(A,B);` `XMVectorPermute(4,5,0,1)(B,A);` mit .

Diese Funktion ist eine Vorlagenversion von [**XMVectorPermute,**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) wobei die *Permute-Argumente \** Vorlagenwerte sind.

Die [XM \_ PERMUTE-Konstanten \_](ovw-xnamath-reference-constants.md) werden zur Verwendung als Eingabewerte für *PermuteX,**PermuteY,**PermuteZ* und *PermuteW* bereitgestellt.

> [!Note]  
> Die `XMVectorPermute` Vorlage ist neu für DirectXMath und nicht für XNAMath 2.x verfügbar.

 

**Namespace:** Verwenden von DirectX

### <a name="platform-requirements"></a>Plattformanforderungen

Microsoft Visual Studio 2010 oder Microsoft Visual Studio 2012 mit dem Windows SDK für Windows 8. Wird für Win32-Desktop-Apps, Windows Store-Apps und Windows Phone 8-Apps unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DirectXMath.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Vorlagenfunktionen der DirectXMath-Bibliothek](ovw-xnamath-templates.md)
</dt> <dt>

[**XMVectorSwizzle**](xmvectorswizzle-template.md)
</dt> </dl>

 

 
