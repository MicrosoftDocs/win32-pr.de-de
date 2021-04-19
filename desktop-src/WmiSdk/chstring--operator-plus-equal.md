---
description: Der Operator + = Concatenations Operator verknüpft Zeichen am Ende dieser Zeichenfolge. Der Operator akzeptiert ein anderes chstring-Objekt, einen Zeichen Zeiger oder ein einzelnes Zeichen.
ms.assetid: 026ff9af-4cda-4261-aa27-e215d49b80ce
ms.tgt_platform: multiple
title: 'Chstring:: Operator + = (chstring. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 683ca6b6264169cd156e89c3447c63fa59f03585
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356207"
---
# <a name="chstringoperator"></a>Chstring:: Operator + =

\[Die [**chstring**](chstring.md) -Klasse ist Teil des WMI-Anbieter-Frameworks, das jetzt im Endzustand behandelt wird, und keine weiteren Entwicklungen, Verbesserungen oder Updates werden für nicht sicherheitsrelevante Probleme verfügbar sein, die diese Bibliotheken betreffen. Die [Mi-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]

Der Operator + = Concatenations Operator verknüpft Zeichen am Ende dieser Zeichenfolge. Der Operator akzeptiert ein anderes [**chstring**](chstring.md) -Objekt, einen Zeichen Zeiger oder ein einzelnes Zeichen.

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

<span id="string"></span><span id="STRING"></span>*Schnür*
</dt> <dd>

Eine [**Zeichen**](chstring.md) folgen Zeichenfolge, die diese Zeichenfolge verkettet.

</dd> <dt>

<span id="ch"></span><span id="CH"></span>*ch*
</dt> <dd>

Ein Zeichen, das mit dieser Zeichenfolge verkettet werden soll.

</dd> <dt>

<span id="lpsz"></span><span id="LPSZ"></span>*lpsz*
</dt> <dd>

Zeiger auf eine mit **null** endenden Zeichenfolge, die mit dieser Zeichenfolge verkettet werden soll.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass Arbeitsspeicher Ausnahmen immer auftreten können, wenn Sie diesen Verkettungs Operator verwenden, da neuer Speicher für Zeichen zugeordnet werden kann, die diesem [**chstring**](chstring.md) -Objekt hinzugefügt werden.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt die Verwendung von **chstring:: Operator + =**:


```C++
CHString s( L"abc" );
assert( ( s += L"def" ) == L"abcdef" );
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

 

