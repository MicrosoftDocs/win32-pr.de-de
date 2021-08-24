---
description: Rotiert einen Vektor nach links um eine bestimmte Anzahl von 32-Bit-Komponenten und fügt ausgewählte Elemente dieses Ergebnisses in einen anderen Vektor ein.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorinsert(xmvector,xmvector)
title: XMVectorInsert-Vorlage (DirectXMath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b90eb7348639e6993cb69ef9e82ab78ed989999ea8423f1f6ff8bd9deb7c70d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739751"
---
# <a name="xmvectorinsert-template"></a>XMVectorInsert-Vorlage

Rotiert einen Vektor nach links um eine bestimmte Anzahl von 32-Bit-Komponenten und fügt ausgewählte Elemente dieses Ergebnisses in einen anderen Vektor ein.

## <a name="syntax"></a>Syntax

``` syntax
template<uint32_t VSLeftRotateElements, uint32_t Select0, uint32_t Select1, uint32_t Select2, uint32_t Select3> XMVECTOR XMVectorInsert(
  [in]  XMVECTOR VD,
  [in]  XMVECTOR VS
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="VD"></span><span id="vd"></span>*Vd*
</dt> <dd>

\[in \] Vektor, in den eingefügt werden soll.

</dd> <dt>

<span id="VS"></span><span id="vs"></span>*Vs*
</dt> <dd>

\[in \] Vektor, der nach links gedreht werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den [**XMVECTOR**](xmvector-data-type.md) zurück, der sich aus der Drehung und Einfügung ergibt.

## <a name="remarks"></a>Hinweise

Diese Funktion ist eine Vorlagenversion von [**XMVectorInsert,**](/windows/win32/api/directxmath/nf-directxmath-xmvectorinsert) wobei die *Select-Argumente \** Vorlagenwerte sind.

Um eine optimale Leistung zu erzielen, sollte das Ergebnis von `XMVectorInsert` wieder *vd* zugewiesen werden.

> [!Note]  
> Die `XMVectorInsert` Vorlage ist neu für DirectXMath und nicht für XNAMath 2.x verfügbar.

 

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
</dt> <dt>

[**XMVectorShiftLeft**](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
