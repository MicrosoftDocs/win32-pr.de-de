---
description: Der Operator + concatenation verbindet zwei Zeichenfolgen und gibt ein CHString-Objekt zurück.
ms.assetid: b7ed6379-ccfa-40f9-9607-d9033179b674
ms.tgt_platform: multiple
title: CHString::operator+ (ChString.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69ce52e8740fcd420600aaebb192c23ab7269c4ddf14c068a4980c59df3e7773
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097350"
---
# <a name="chstringoperator"></a>CHString::operator+

\[Die [**CHString-Klasse**](chstring.md) ist Teil des WMI-Anbieterframeworks, das jetzt als endgültiger Zustand betrachtet wird. Für nicht sicherheitsrelevante Probleme, die sich auf diese Bibliotheken auswirken, sind keine weiteren Entwicklungen, Erweiterungen oder Updates verfügbar. Die [MI-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle Neuentwicklungen verwendet werden.\]

Der Operator + concatenation verbindet zwei Zeichenfolgen und gibt ein [**CHString-Objekt**](chstring.md) zurück.

``` syntax
friend CHString operator +(
  const CHString& str1,
  const CHString& str2 )
throw( CHeap_Exception );

friend CHString operator +(
  const CHString& str,
  WCHAR ch )
throw( CHeap_Exception );

friend CHString operator +(
  WCHAR ch,
  const CHString& str )
throw( CHeap_Exception );

friend CHString operator +(
  const CHString& str,
  LPCWSTR lpsz )
throw( CHeap_Exception );

friend CHString operator +(
  LPCWSTR lpsz,
  const CHString& str )
throw( CHeap_Exception );

friend CHString operator +(
  const CHString& str,
  char ch )
throw( CHeap_Exception );

friend CHString operator +(
  char ch,
  const CHString& str )
throw( CHeap_Exception );
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="str__str1__str2"></span><span id="STR__STR1__STR2"></span>*str, str1, str2*
</dt> <dd>

[**CHString-Zeichenfolgen,**](chstring.md) die verkettet sind.

</dd> <dt>

<span id="ch"></span><span id="CH"></span>*Ch*
</dt> <dd>

Ein Zeichen, das mit einer Zeichenfolge verkettet wird, oder eine Zeichenfolge, die mit einem Zeichen verkettet wird.

</dd> <dt>

<span id="lpsz"></span><span id="LPSZ"></span>*lpsz*
</dt> <dd>

Zeiger auf eine NULL-terminierte Zeichenfolge.

</dd> </dl>

## <a name="return-values"></a>Rückgabewerte

Dieser Verkettungsoperator gibt ein [**CHString-Objekt**](chstring.md) zurück, das das temporäre Ergebnis der Verkettung ist. Dieser Rückgabewert ermöglicht es, mehrere Verkettungen im gleichen Ausdruck zu kombinieren.

## <a name="remarks"></a>Hinweise

Eine der beiden Argumentzeichenfolgen muss ein [**CHString-Objekt**](chstring.md) sein. der andere kann ein Zeichenzeiger oder ein Zeichen sein. Beachten Sie, dass Arbeitsspeicherausnahmen auftreten können, wenn Sie den Verkettungsoperator verwenden, da neuer Speicher möglicherweise für temporäre Daten zugeordnet wird.

## <a name="examples"></a>Beispiele

Das folgende Codebeispiel zeigt die Verwendung von **CHString::operator +**:


```C++
CHString s1( L"abc" );
CHString s2( L"def" );
assert( (s1 + s2 ) == L"abcdef" );

CHString s3;
s3 = CHString( L"abc" ) + "def" ; // Correct
s3 = "abc" + "def"; // Wrong. The first argument must be a CHString.
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

 

