---
description: Verschiebt einen Vektor um eine bestimmte Anzahl von 32-Bit-Elementen nach links, wobei die frei gewordenen Elemente mit Elementen aus einem zweiten Vektor gefüllt werden.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorshiftleft(xmvector,xmvector)
title: XMVectorShiftLeft-Vorlage (DirectXMath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ab92e2fb64a101251a7531ca1d96b8b06f3e9af6e2b7dabe7958673a61bd8c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118499279"
---
# <a name="xmvectorshiftleft-template"></a>XMVectorShiftLeft-Vorlage

Verschiebt einen Vektor um eine bestimmte Anzahl von 32-Bit-Elementen nach links, wobei die frei gewordenen Elemente mit Elementen aus einem zweiten Vektor gefüllt werden.

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

\[in \] Vektor, um nach links zu verschieben.

</dd> <dt>

<span id="V2"></span><span id="v2"></span>*V2*
</dt> <dd>

\[in \] Vector, der verwendet wird, um die frei gewordenen Komponenten von V1 auszufüllen, nachdem sie nach links verschoben wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die verschobene zurück und wird in [**XMVECTOR**](xmvector-data-type.md)ausgefüllt.

## <a name="remarks"></a>Hinweise

Diese Funktion ist eine Vorlagenversion von [**XMVectorShiftLeft,**](/windows/win32/api/directxmath/nf-directxmath-xmvectorshiftleft) wobei das *Elements-Argument* ein Vorlagenwert ist.

> [!Note]  
> Die `XMVectorShiftLeft` Vorlage ist neu für DirectXMath und nicht für XNAMath 2.x verfügbar.

 

**Namespace:** Verwenden von DirectX

### <a name="platform-requirements"></a>Plattformanforderungen

Microsoft Visual Studio 2010 oder Microsoft Visual Studio 2012 mit dem Windows SDK für Windows 8. Wird für Win32-Desktop-Apps, Windows Store-Apps und Windows Phone 8-Apps unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DirectXMath.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Vorlagenfunktionen der DirectXMath-Bibliothek](ovw-xnamath-templates.md)
</dt> <dt>

[**XMVectorPermute**](xmvectorpermute-template.md)
</dt> <dt>

[**XMVectorRotateLeft**](xmvectorrotateleft-template.md)
</dt> <dt>

[**XMVectorRotateRight**](xmvectorrotateright-template.md)
</dt> </dl>

 

 
