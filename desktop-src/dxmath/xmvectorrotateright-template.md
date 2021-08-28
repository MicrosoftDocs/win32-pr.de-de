---
description: Rotiert den Vektor um eine bestimmte Anzahl von 32-Bit-Elementen nach rechts.
ms.assetid: 7493c1fe-2c3d-4eb6-bec1-02c066a70b9f
title: XMVectorRotateRight-Vorlage (DirectXMath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47017982af6bb61212129665010d403bd9db898c65056110c4d2f40a5f8a9362
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984490"
---
# <a name="xmvectorrotateright-template"></a>XMVectorRotateRight-Vorlage

Rotiert den Vektor um eine bestimmte Anzahl von 32-Bit-Elementen nach rechts.

## <a name="syntax"></a>Syntax

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorRotateRight(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="V"></span><span id="v"></span>*V*
</dt> <dd>

\[in \] Vektor, um nach rechts zu drehen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den gedrehten [**XMVECTOR**](xmvector-data-type.md)zurück.

## <a name="remarks"></a>Hinweise

Diese Funktion ist eine Vorlagenversion von [**XMVectorRotateRight,**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateright) wobei das *Elements-Argument* ein Vorlagenwert ist.

> [!Note]  
> Die `XMVectorRotateRight` Vorlage ist neu für DirectXMath und nicht für XNAMath 2.x verfügbar.

 

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

[**XMVectorRotateLeft**](xmvectorrotateleft-template.md)
</dt> <dt>

[**XMVectorShiftLeft**](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
