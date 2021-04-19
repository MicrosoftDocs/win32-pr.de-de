---
description: Dreht den Vektor nach rechts um eine angegebene Anzahl von 32-Bit-Elementen.
ms.assetid: 7493c1fe-2c3d-4eb6-bec1-02c066a70b9f
title: Xmvector rotateright-Vorlage (directxmath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa2c4e623a75015e8051a5a9ccf32f4715016b73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359819"
---
# <a name="xmvectorrotateright-template"></a>Xmvector rotateright-Vorlage

Dreht den Vektor nach rechts um eine angegebene Anzahl von 32-Bit-Elementen.

## <a name="syntax"></a>Syntax

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorRotateRight(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="V"></span><span id="v"></span>*Ramelow*
</dt> <dd>

\[in \] Vektor zum Drehen nach rechts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den gedrehten [**xmvector**](xmvector-data-type.md)zurück.

## <a name="remarks"></a>Bemerkungen

Bei dieser Funktion handelt es sich um eine Vorlagen Version von [**xmvectorrotateright**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateright) , bei der das *Elements* -Argument ein Vorlagen Wert ist.

> [!Note]  
> Die `XMVectorRotateRight` Vorlage ist neu für directxmath und für xnamath 2. x nicht verfügbar.

 

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

[**Xmvector shiftleft**](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
