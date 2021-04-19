---
description: Dreht einen Vektor nach links um eine bestimmte Anzahl von 32-Bit-Komponenten und fügt ausgewählte Elemente dieses Ergebnisses in einen anderen Vektor ein.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorinsert(xmvector,xmvector)
title: Xmvector INSERT-Vorlage (directxmath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3250ad52ab19a127b110b02ecf71543f44708681
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354224"
---
# <a name="xmvectorinsert-template"></a>Xmvector INSERT-Vorlage

Dreht einen Vektor nach links um eine bestimmte Anzahl von 32-Bit-Komponenten und fügt ausgewählte Elemente dieses Ergebnisses in einen anderen Vektor ein.

## <a name="syntax"></a>Syntax

``` syntax
template<uint32_t VSLeftRotateElements, uint32_t Select0, uint32_t Select1, uint32_t Select2, uint32_t Select3> XMVECTOR XMVectorInsert(
  [in]  XMVECTOR VD,
  [in]  XMVECTOR VS
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="VD"></span><span id="vd"></span>*Abbiegen*
</dt> <dd>

\[in \] Vektor, das in eingefügt werden soll.

</dd> <dt>

<span id="VS"></span><span id="vs"></span>*Jews*
</dt> <dd>

\[im \] Vektor zum Drehen nach links.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den [**xmvector**](xmvector-data-type.md) zurück, der sich aus der Drehung und dem Einfügen ergibt.

## <a name="remarks"></a>Bemerkungen

Bei dieser Funktion handelt es sich um eine Vorlagen Version von [**xmvectorinsert**](/windows/win32/api/directxmath/nf-directxmath-xmvectorinsert) , bei der die *Select \** -Argumente Vorlagen Werte sind.

Um die optimale Leistung zu erzielen, sollte das Ergebnis von `XMVectorInsert` zurück zu *VD* zugewiesen werden.

> [!Note]  
> Die `XMVectorInsert` Vorlage ist neu für directxmath und für xnamath 2. x nicht verfügbar.

 

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
</dt> <dt>

[**Xmvector shiftleft**](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
