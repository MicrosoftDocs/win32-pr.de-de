---
description: Vergleicht zwei numerische Datentyp Instanzen oder zwei Instanzen eines Objekts, das eine Überladung von < unterstützt, und gibt die größere einer der beiden-Instanzen zurück. Der Datentyp der Argumente und der Rückgabewert sind identisch.
ms.assetid: m:microsoft.directx_sdk.reference.xmmax(t,t)
title: Xmmax-Vorlage (directxmath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6f8de32a32004289249cea269400d711831d640
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364747"
---
# <a name="xmmax-template"></a>Xmmax-Vorlage

Vergleicht zwei numerische Datentyp Instanzen oder zwei Instanzen eines Objekts, das eine Überladung von < unterstützt, und gibt die größere einer der beiden-Instanzen zurück. Der Datentyp der Argumente und der Rückgabewert sind identisch.

## <a name="syntax"></a>Syntax

``` syntax
template<class T> T XMMax(
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

Gibt die größere der beiden Eingabe Objekte zurück.

## <a name="remarks"></a>Bemerkungen

`XMMax` ist eine Vorlage, und der T-Typ wird angegeben, wenn die Vorlage instanziiert wird.

> [!Note]  
> Die `XMMax` Vorlage ist neu für directxmath und für xnamath 2. x nicht verfügbar. `XMMax` ist als Makro in xnamath 2. x verfügbar.

 

> [!Note]  
> Verwenden Sie idealerweise Std:: Max anstelle von `XMMax` . Um Konflikte mit Windows-Headern mit Std:: Max zu vermeiden, müssen Sie \# nominmax definieren, bevor Sie Windows-Header einschließen.

 

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

[**Xmmin**](xmmin-template.md)
</dt> </dl>

 

 




