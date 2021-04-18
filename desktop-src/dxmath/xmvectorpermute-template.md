---
description: Permutes die Komponenten von zwei Vektoren, um einen neuen Vektor zu erstellen.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorpermute(xmvector,xmvector)
title: Xmvector perstumm-Vorlage (directxmath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37271cbb165f1e9c1769ef3a55e47f1e07310a81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352145"
---
# <a name="xmvectorpermute-template"></a>Xmvector perstumm-Vorlage

Permutes die Komponenten von zwei Vektoren, um einen neuen Vektor zu erstellen.

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

\[im \] ersten Vektor.

</dd> <dt>

<span id="V2"></span><span id="v2"></span>*V2*
</dt> <dd>

\[im \] zweiten Vektor.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den permutierten Vektor zurück, der durch Kombinieren der Quell Vektoren entstanden ist.

## <a name="remarks"></a>Bemerkungen

Wenn alle 4 Indizes nur auf einen einzelnen Vektor verweisen (d. h., Sie befinden sich alle im Bereich von 0-3 oder alle im Bereich 4-7), verwenden Sie stattdessen [**xmvector Swizzle**](xmvectorswizzle-template.md) , um die Leistung zu verbessern.

Beachten Sie, dass die Bibliothek auf einigen Plattformen Vorlagen Spezialisierungs Vorlagen verwendet, um die Leistung zu verbessern. Nicht jeder mögliche Spiegelungs Fall wird für diese besonderen Fälle implementiert. bevorzugen Sie daher permutes, bei denen das X-Element des resultierenden Vektors aus dem V1-Parameter und nicht aus dem V2-Parameter stammt. Verwenden Sie beispielsweise, `XMVectorPermute<0,1,4,5>(A,B);` um zu verwenden `XMVectorPermute(4,5,0,1)(B,A);` .

Bei dieser Funktion handelt es sich um eine Vorlagen Version von [**xmvectorperstumm**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) , bei der die *perstumm \** Argumente Vorlagen Werte sind.

Die [XM- \_ perstumm \_](ovw-xnamath-reference-constants.md) Konstanten werden zur Verwendung als Eingabewerte für *permutex*,*permutey*,*permutez* und *permutew* bereitgestellt.

> [!Note]  
> Die `XMVectorPermute` Vorlage ist neu für directxmath und für xnamath 2. x nicht verfügbar.

 

**Namespace**: Verwenden von DirectX

### <a name="platform-requirements"></a>Plattformanforderungen

Microsoft Visual Studio 2010 oder Microsoft Visual Studio 2012 mit dem Windows SDK für Windows 8. Wird für Win32-Desktop-Apps, Windows Store-Apps und Windows Phone 8-Apps unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Directxmath. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Directxmath-Bibliotheks Vorlagen Funktionen](ovw-xnamath-templates.md)
</dt> <dt>

[**Xmvector Swizzle**](xmvectorswizzle-template.md)
</dt> </dl>

 

 
