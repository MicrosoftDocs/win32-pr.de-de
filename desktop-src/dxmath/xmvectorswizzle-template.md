---
description: Swizzles ein Vektor.
ms.assetid: 75608e80-5911-45a8-beca-ceac1f4d2c1c
title: XMVectorSwizzle-Vorlage (DirectXMath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 800d976d63480f88defea7f1db07651563df44e8985ae5925810617b44302e87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984480"
---
# <a name="xmvectorswizzle-template"></a>XMVectorSwizzle-Vorlage

Swizzles ein Vektor.

## <a name="syntax"></a>Syntax

``` syntax
template<uint32_t SwizzleX, uint32_t SwizzleY, uint32_t SwizzleZ, uint32_t SwizzleW> XMVECTOR XMVectorSwizzle(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="V"></span><span id="v"></span>*V*
</dt> <dd>

\[in \] Vektor zu Swizzle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den geschwenkten [**XMVECTOR zurück.**](xmvector-data-type.md)

## <a name="remarks"></a>Hinweise

Diese Funktion ist eine Vorlagenversion von [**XMVectorSwizzle,**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) bei der die *Swizzle-Argumente \** Vorlagenwerte sind.

`XM_SWIZZLE_X`, `XM_SWIZZLE_Y` `XM_SWIZZLE_Z` , und sind `XM_SWIZZLE_W` Konstanten, die zu 0, 1, 2 bzw. 3 für die Verwendung mit ausgewertet `XMVectorSwizzle` werden. Dies ist identisch mit `XM_PERMUTE_0X` , `XM_PERMUTE_0Y` , und `XM_PERMUTE_0Z` `XM_PERMUTE_0W` .

> [!Note]  
> Die `XMVectorSwizzle` Vorlage ist neu für DirectXMath und nicht für XNAMath 2.x verfügbar.

 

**Namespace:** DirectX verwenden

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
</dt> </dl>

 

 
