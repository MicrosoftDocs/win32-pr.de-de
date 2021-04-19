---
description: Dreht den Vektor um eine angegebene Anzahl von 32-Bit-Elementen nach links.
ms.assetid: ba3698ed-212d-4ef0-846a-4099d0e1abec
title: Xmvector rotateleft-Vorlage (directxmath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e5b52fccebeb93803fdc33346fa4ee5e873c1d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368577"
---
# <a name="xmvectorrotateleft-template"></a>Xmvector rotateleft-Vorlage

Dreht den Vektor um eine angegebene Anzahl von 32-Bit-Elementen nach links.

## <a name="syntax"></a>Syntax

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorRotateLeft(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="V"></span><span id="v"></span>*Ramelow*
</dt> <dd>

\[im \] Vektor zum Drehen nach links.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den gedrehten [**xmvector**](xmvector-data-type.md)zurück.

## <a name="remarks"></a>Bemerkungen

Bei dieser Funktion handelt es sich um eine Vorlagen Version von [**xmvectorrotateleft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateleft) , bei der das *Elements* -Argument ein Vorlagen Wert ist.

> [!Note]  
> Die `XMVectorRotateLeft` Vorlage ist neu für directxmath und für xnamath 2. x nicht verfügbar.

 

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

[**Xmvector rotateright**](xmvectorrotateright-template.md)
</dt> <dt>

[**Xmvector shiftleft**](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
