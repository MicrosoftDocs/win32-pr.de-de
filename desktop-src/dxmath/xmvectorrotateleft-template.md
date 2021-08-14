---
description: Rotiert den Vektor um eine bestimmte Anzahl von 32-Bit-Elementen nach links.
ms.assetid: ba3698ed-212d-4ef0-846a-4099d0e1abec
title: XMVectorRotateLeft-Vorlage (DirectXMath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbb3d2a06f775e99b275d7333816307f494c5b2a4a7cc0183eaddc4ee4cd8950
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118499403"
---
# <a name="xmvectorrotateleft-template"></a>XMVectorRotateLeft-Vorlage

Rotiert den Vektor um eine bestimmte Anzahl von 32-Bit-Elementen nach links.

## <a name="syntax"></a>Syntax

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorRotateLeft(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="V"></span><span id="v"></span>*V*
</dt> <dd>

\[in \] Vektor, der nach links gedreht werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den gedrehten [**XMVECTOR**](xmvector-data-type.md)zurück.

## <a name="remarks"></a>Hinweise

Diese Funktion ist eine Vorlagenversion von [**XMVectorRotateLeft,**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateleft) wobei das *Elements-Argument* ein Vorlagenwert ist.

> [!Note]  
> Die `XMVectorRotateLeft` Vorlage ist neu für DirectXMath und nicht für XNAMath 2.x verfügbar.

 

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

[**XMVectorPermute**](xmvectorpermute-template.md)
</dt> <dt>

[**XMVectorRotateRight**](xmvectorrotateright-template.md)
</dt> <dt>

[**XMVectorShiftLeft**](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
