---
description: Vergleicht zwei numerische Datentypinstanzen oder zwei Instanzen eines Objekts, das eine Überladung von < unterstützt, und gibt die kleinere der beiden Instanzen zurück. Der Datentyp der Argumente und der Rückgabewert sind identisch.
ms.assetid: m:microsoft.directx_sdk.reference.xmmin(t,t)
title: XMMin-Vorlage (DirectXMath.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c2d78b64a66411c31570267c66a7e75171dcf9da039871c07c8bfc31df49149
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118499855"
---
# <a name="xmmin-template"></a>XMMin-Vorlage

Vergleicht zwei numerische Datentypinstanzen oder zwei Instanzen eines Objekts, das eine Überladung von < unterstützt, und gibt die kleinere der beiden Instanzen zurück. Der Datentyp der Argumente und der Rückgabewert sind identisch.

## <a name="syntax"></a>Syntax

``` syntax
template<class T> T XMMin(
  [in]  T a,
  [in]  T b
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="a"></span><span id="A"></span>*Eine*
</dt> <dd>

\[in \] Gibt das erste von zwei -Objekten an.

</dd> <dt>

<span id="b"></span><span id="B"></span>*B*
</dt> <dd>

\[in \] Gibt die beiden von zwei -Objekten an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das kleinere der beiden Eingabeobjekte zurück.

## <a name="remarks"></a>Hinweise

`XMMin` ist eine Vorlage, und der T-Typ wird angegeben, wenn die Vorlage instanziiert wird.

> [!Note]  
> Die `XMMin` Vorlage ist neu für DirectXMath und nicht für XNAMath 2.x verfügbar. `XMMin` ist als Makro in XNAMath 2.x verfügbar.

 

> [!Note]  
> Verwenden Sie im Idealfall std::min anstelle von `XMMin` . Um Konflikte mit Windows Headern mit std::min zu vermeiden, müssen Sie \# NOMINMAX definieren, bevor Sie Windows Header einschließen.

 

**Namespace:** Verwenden von DirectX

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

[**XMMax**](xmmax-template.md)
</dt> </dl>

 

 




