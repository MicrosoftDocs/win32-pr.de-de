---
description: Der Verkettungsoperator += verbindet Zeichen am Ende dieser Zeichenfolge. Der Operator akzeptiert ein anderes CHString-Objekt, einen Zeichenzeiger oder ein einzelnes Zeichen.
ms.assetid: 026ff9af-4cda-4261-aa27-e215d49b80ce
ms.tgt_platform: multiple
title: CHString::operator+= (ChString.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 316f5272c7b5a4ef5b59e93dd480ade215e3279ea754f1da5432448d46fcce17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679879"
---
# <a name="chstringoperator"></a>CHString::operator+=

\[Die [**CHString-Klasse**](chstring.md) ist Teil des WMI-Anbieterframeworks, das jetzt als endgültiger Zustand betrachtet wird. Für nicht sicherheitsrelevante Probleme, die sich auf diese Bibliotheken auswirken, sind keine weiteren Entwicklungen, Erweiterungen oder Updates verfügbar. Die [MI-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle Neuentwicklungen verwendet werden.\]

Der Verkettungsoperator += verbindet Zeichen am Ende dieser Zeichenfolge. Der Operator akzeptiert ein anderes [**CHString-Objekt,**](chstring.md) einen Zeichenzeiger oder ein einzelnes Zeichen.

``` syntax
const CHString& operator +=(
  const CHString& string )
throw( CHeap_Exception );

const CHString& operator +=(
  WCHAR ch )
throw( CHeap_Exception );

const CHString& operator +=(
  LPCWSTR lpsz )
throw( CHeap_Exception );

const CHString operator +=(
  char ch )
throw( CHeap_Exception );
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="string"></span><span id="STRING"></span>*Schnur*
</dt> <dd>

Eine [**CHString-Zeichenfolge,**](chstring.md) die mit dieser Zeichenfolge verkettet wird.

</dd> <dt>

<span id="ch"></span><span id="CH"></span>*Ch*
</dt> <dd>

Ein Zeichen, das mit dieser Zeichenfolge verkettet werden soll.

</dd> <dt>

<span id="lpsz"></span><span id="LPSZ"></span>*lpsz*
</dt> <dd>

Zeiger auf eine **MIT NULL** endende Zeichenfolge, die mit dieser Zeichenfolge verkettet werden soll.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Beachten Sie, dass Speicherausnahmen auftreten können, wenn Sie diesen Verkettungsoperator verwenden, da diesem [**CHString-Objekt**](chstring.md) möglicherweise neuer Speicher für Zeichen zugeordnet wird.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt die Verwendung von **CHString::operator +=**:


```C++
CHString s( L"abc" );
assert( ( s += L"def" ) == L"abcdef" );
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                                                                                |
| Header<br/>                   | <dl> <dt>ChString.h (include FwCommon.h)</dt> </dl>                                                    |
| Bibliothek<br/>                  | <dl> <dt>FrameDyn.lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CHString**](chstring.md)
</dt> </dl>

 

