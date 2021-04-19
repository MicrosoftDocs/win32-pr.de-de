---
description: Vergleicht zwei numerische Datentyp Instanzen oder zwei Instanzen eines Objekts, das eine Überladung von < unterstützt, und gibt die kleinere der beiden-Instanzen zurück. Der Datentyp der Argumente und der Rückgabewert sind identisch.
ms.assetid: m:microsoft.directx_sdk.reference.xmmin(t,t)
title: Xmmin-Vorlage (directxmath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 550fd93c9776ad8547502b50817446e64f9bdd64
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106363210"
---
# <a name="xmmin-template"></a>Xmmin-Vorlage

Vergleicht zwei numerische Datentyp Instanzen oder zwei Instanzen eines Objekts, das eine Überladung von < unterstützt, und gibt die kleinere der beiden-Instanzen zurück. Der Datentyp der Argumente und der Rückgabewert sind identisch.

## <a name="syntax"></a>Syntax

``` syntax
template<class T> T XMMin(
  [in]  T a,
  [in]  T b
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="a"></span><span id="A"></span>*ein*
</dt> <dd>

\[in \] gibt das erste von zwei-Objekten an.

</dd> <dt>

<span id="b"></span><span id="B"></span>*b*
</dt> <dd>

\[in \] gibt die zwei von zwei-Objekten an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die kleinere der beiden Eingabe Objekte zurück.

## <a name="remarks"></a>Bemerkungen

`XMMin` ist eine Vorlage, und der T-Typ wird angegeben, wenn die Vorlage instanziiert wird.

> [!Note]  
> Die `XMMin` Vorlage ist neu für directxmath und für xnamath 2. x nicht verfügbar. `XMMin` ist als Makro in xnamath 2. x verfügbar.

 

> [!Note]  
> Verwenden Sie idealerweise Std:: min anstelle von `XMMin` . Um Konflikte mit Windows-Headern mit Std:: min zu vermeiden, müssen Sie \# nominmax definieren, bevor Sie Windows-Header einschließen.

 

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

[**Xmmax**](xmmax-template.md)
</dt> </dl>

 

 




