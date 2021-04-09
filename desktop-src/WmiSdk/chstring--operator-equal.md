---
description: Der Operator "chstring-Zuweisung (=)" Initialisiert ein vorhandenes "chstring"-Objekt mit neuen Daten erneut.
ms.assetid: 6864aacf-ac18-4b5a-be3e-3a0d8bb31e74
ms.tgt_platform: multiple
title: 'Chstring:: Operator = (chstring. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9abfa9ea2b72aa8f6830d9fb6388861c8c3b82d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042368"
---
# <a name="chstringoperator"></a>Chstring:: Operator =

\[Die [**chstring**](chstring.md) -Klasse ist Teil des WMI-Anbieter-Frameworks, das jetzt im Endzustand behandelt wird, und keine weiteren Entwicklungen, Verbesserungen oder Updates werden für nicht sicherheitsrelevante Probleme verfügbar sein, die diese Bibliotheken betreffen. Die [Mi-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]

Der Operator " [**chstring**](chstring.md) -Zuweisung (=)" Initialisiert ein vorhandenes "chstring"-Objekt mit neuen Daten erneut.

``` syntax
const CHString& operator =(
  const CHString& stringSrc )
throw( CHeap_Exception );

const CHString& operator =(
  WCHAR ch )
throw( CHeap_Exception );

const CHString& operator =(
  const unsigned char* psz )
throw( CHeap_Exception );

const CHString& operator =(
  LPCWSTR lpsz )
throw( CHeap_Exception );

const CHString& operator =(
  LPCSTR lpsz )
throw( CHeap_Exception );

const CHString& operator =(
  CHString *p )
throw( CHeap_Exception );

const CHString& operator =(
  char ch )
throw( CHeap_Exception );
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="stringSrc__p"></span><span id="stringsrc__p"></span><span id="STRINGSRC__P"></span>*stringsrc*, *p*
</dt> <dd>

Weist diesem- [**Objekt eine Zeichen**](chstring.md) folgen Zeichenfolge zu.

</dd> <dt>

<span id="ch"></span><span id="CH"></span>*ch*
</dt> <dd>

Weist diesem-Objekt ein Zeichen zu.

</dd> <dt>

<span id="lpsz__psz"></span><span id="LPSZ__PSZ"></span>*lpsz*, *PSZ*
</dt> <dd>

Weist diesem-Objekt eine **null**-terminierte Zeichenfolge zu.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn die Ziel Zeichenfolge (d. h. die linke Seite) bereits groß genug ist, um die neuen Daten zu speichern, erfolgt keine neue Speicher Belegung. Arbeitsspeicher Ausnahmen können jedoch immer auftreten, wenn Sie den Zuweisungs Operator verwenden, da der neue Speicher häufig dem resultierenden [**chstring**](chstring.md) -Objekt zugeordnet wird.

## <a name="examples"></a>Beispiele

Das folgende Codebeispiel zeigt die Verwendung von **chstring:: Operator =**:


```C++
CHString s1, s2;        // Empty CHString objects

s1 = L"cat";            // s1 = "cat"
s2 = s1;                // s1 and s2 each = "cat"
s1 = L"the " + s1;      // Or expressions
s1 = 'x';               // Or just individual characters
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

 

