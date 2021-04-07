---
description: Der Operator + Concatenations Operator verknüpft zwei Zeichen folgen und gibt ein chstring-Objekt zurück.
ms.assetid: b7ed6379-ccfa-40f9-9607-d9033179b674
ms.tgt_platform: multiple
title: 'Chstring:: Operator + (chstring. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5053a4d3059a66cb2c8e4a89a3bdd531d5f42de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758220"
---
# <a name="chstringoperator"></a>Chstring:: Operator +

\[Die [**chstring**](chstring.md) -Klasse ist Teil des WMI-Anbieter-Frameworks, das jetzt im Endzustand behandelt wird, und keine weiteren Entwicklungen, Verbesserungen oder Updates werden für nicht sicherheitsrelevante Probleme verfügbar sein, die diese Bibliotheken betreffen. Die [Mi-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]

Der Operator + Concatenations Operator verknüpft zwei Zeichen folgen und gibt ein [**chstring**](chstring.md) -Objekt zurück.

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

<span id="str__str1__str2"></span><span id="STR__STR1__STR2"></span>*Str, str1, str2*
</dt> <dd>

[**Chstring-Zeichen**](chstring.md) folgen, die verkettet werden.

</dd> <dt>

<span id="ch"></span><span id="CH"></span>*ch*
</dt> <dd>

Ein Zeichen, das eine Zeichenfolge oder eine Zeichenfolge verkettet, die ein Zeichen verkettet.

</dd> <dt>

<span id="lpsz"></span><span id="LPSZ"></span>*lpsz*
</dt> <dd>

Zeiger auf eine mit **null** endenden Zeichenfolge.

</dd> </dl>

## <a name="return-values"></a>Rückgabewerte

Dieser Verkettungs Operator gibt ein [**chstring**](chstring.md) -Objekt zurück, das das temporäre Ergebnis der Verkettung ist. Dieser Rückgabewert ermöglicht das Kombinieren mehrerer Verkettungen im gleichen Ausdruck.

## <a name="remarks"></a>Bemerkungen

Eine der beiden Argument Zeichenfolgen muss ein [**chstring**](chstring.md) -Objekt sein. der andere kann ein Zeichen Zeiger oder ein Zeichen sein. Beachten Sie, dass Arbeitsspeicher Ausnahmen immer auftreten können, wenn Sie den Verkettungs Operator verwenden, da neuer Speicher zugeordnet werden kann, um temporäre Daten zu speichern.

## <a name="examples"></a>Beispiele

Das folgende Codebeispiel zeigt die Verwendung von **chstring:: Operator +**:


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
| Header<br/>                   | <dl> <dt>Chstring. h (Include-Datei "f")</dt> </dl>                                                    |
| Bibliothek<br/>                  | <dl> <dt>Framedyn. lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Zeichenfolge**](chstring.md)
</dt> </dl>

 

