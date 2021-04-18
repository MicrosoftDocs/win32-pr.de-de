---
description: Schwimmt einen Vektor.
ms.assetid: 75608e80-5911-45a8-beca-ceac1f4d2c1c
title: Xmvector Swizzle-Vorlage (directxmath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8e872d76f3251eccc8616c143c645b388e2dca4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352144"
---
# <a name="xmvectorswizzle-template"></a>Xmvector Swizzle-Vorlage

Schwimmt einen Vektor.

## <a name="syntax"></a>Syntax

``` syntax
template<uint32_t SwizzleX, uint32_t SwizzleY, uint32_t SwizzleZ, uint32_t SwizzleW> XMVECTOR XMVectorSwizzle(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="V"></span><span id="v"></span>*Ramelow*
</dt> <dd>

\[in \] Vektor zum Schwenken.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den von einem Streifen geleiteten [**xmvector**](xmvector-data-type.md)zurück.

## <a name="remarks"></a>Bemerkungen

Bei dieser Funktion handelt es sich um eine Vorlagen Version von [**xmvectorswizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) , bei der die *\* swidgumente* Vorlagen Werte sind.

`XM_SWIZZLE_X`, `XM_SWIZZLE_Y` , `XM_SWIZZLE_Z` und `XM_SWIZZLE_W` sind Konstanten, die für die Verwendung mit 0, 1, 2 bzw. 3 ausgewertet werden `XMVectorSwizzle` . Dies ist identisch mit `XM_PERMUTE_0X` , `XM_PERMUTE_0Y` , `XM_PERMUTE_0Z` und `XM_PERMUTE_0W` .

> [!Note]  
> Die `XMVectorSwizzle` Vorlage ist neu für directxmath und für xnamath 2. x nicht verfügbar.

 

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

[**Xmvector perstumm Zeichen**](xmvectorpermute-template.md)
</dt> </dl>

 

 
