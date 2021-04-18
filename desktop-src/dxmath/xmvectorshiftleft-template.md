---
description: Verschiebt einen Vektor um eine bestimmte Anzahl von 32-Bit-Elementen nach links und füllt die freigegebenen Elemente mit Elementen aus einem zweiten Vektor.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorshiftleft(xmvector,xmvector)
title: Xmvector shiftleft-Vorlage (directxmath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 115604871d9e8402157a82bf3c420e5762b3a424
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371595"
---
# <a name="xmvectorshiftleft-template"></a>Xmvector shiftleft-Vorlage

Verschiebt einen Vektor um eine bestimmte Anzahl von 32-Bit-Elementen nach links und füllt die freigegebenen Elemente mit Elementen aus einem zweiten Vektor.

## <a name="syntax"></a>Syntax

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorShiftLeft(
  [in]  XMVECTOR V1,
  [in]  XMVECTOR V2
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="V1"></span><span id="v1"></span>*V1*
</dt> <dd>

\[im \] Vektor nach links verschieben.

</dd> <dt>

<span id="V2"></span><span id="v2"></span>*V2*
</dt> <dd>

\[in \] Vector, das verwendet wird, um die frei gewordenen Komponenten von v1 auszufüllen, nachdem es nach links verschoben wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den verschobenen und gefüllten [**xmvector**](xmvector-data-type.md)zurück.

## <a name="remarks"></a>Bemerkungen

Bei dieser Funktion handelt es sich um eine Vorlagen Version von [**xmvectorshiftleft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorshiftleft) , wobei das *Element* -Argument ein Vorlagen Wert ist.

> [!Note]  
> Die `XMVectorShiftLeft` Vorlage ist neu für directxmath und für xnamath 2. x nicht verfügbar.

 

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
</dt> <dt>

[**Xmvector rotateleft**](xmvectorrotateleft-template.md)
</dt> <dt>

[**Xmvector rotateright**](xmvectorrotateright-template.md)
</dt> </dl>

 

 
