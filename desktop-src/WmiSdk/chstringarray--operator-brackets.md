---
description: Diese Index Operatoren legen das Element am angegebenen Index fest oder erhalten es. Diese Operatoren sind eine bequeme Ersetzung für die Methoden "Methode" und "GetAt".
ms.assetid: 93b10bef-908e-4c5e-aac3-b13051b2e7c9
ms.tgt_platform: multiple
title: 'Chstringarray:: Operator [] (chstrarr. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e92b30768b9d013bfca672548a7c58b0eeffb455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351031"
---
# <a name="chstringarrayoperator--"></a>Chstringarray::-Operator \[\]

\[Die [**chstringarray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) -Klasse ist Teil des WMI-Anbieter-Frameworks, das jetzt als Endzustand betrachtet wird, und keine weiteren Entwicklungen, Verbesserungen oder Updates werden für nicht sicherheitsrelevante Probleme verfügbar sein, die diese Bibliotheken betreffen. Die [Mi-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]

Diese Index Operatoren legen das Element am angegebenen Index fest oder erhalten es. Diese Operatoren sind eine bequeme Ersetzung für die Methoden "Methode [**" und "**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr)) [**GetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int)) ".

``` syntax
CHString& operator []( 
  int nIndex
);

CHString operator []( 
  int nIndex
) const;
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="nIndex"></span><span id="nindex"></span><span id="NINDEX"></span>*nIndex*
</dt> <dd>

Ein ganzzahliger Index, der größer oder gleich 0 (null) und kleiner oder gleich dem von [ **GetUpperBound** zurückgegebenen Wert ist.](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getupperbound)

</dd> </dl>

## <a name="return-values"></a>Rückgabewerte

Die Index Operatoren geben das [**chstring**](chstring.md) -Zeiger Element zurück, das sich derzeit an diesem Index befindet.

## <a name="remarks"></a>Bemerkungen

Sie können den ersten Operator verwenden, der für Arrays, die nicht **konstant** sind, entweder auf der rechten (r-Wert) oder der linken (l-Wert)-Seite einer Zuweisungsanweisung aufruft. Die zweite, die für **Konstanten** Arrays aufruft, kann nur auf der rechten Seite verwendet werden.

Die Debugversion der Bibliothek bestätigt, ob der Index (entweder auf der linken oder rechten Seite einer Zuweisungsanweisung) außerhalb des gültigen Bereichs liegt.

## <a name="examples"></a>Beispiele

Das folgende Codebeispiel zeigt die Verwendung von [**chstringarray:: Operator \[ \]**](/previous-versions/windows/desktop/legacy/aa384934(v=vs.85)).


```C++
CHStringArray array;
CHString s;

array.Add( L"String 1" ); // Element 0 
array.Add( L"String 2" ); // Element 1 
s = array[0]; // Get element 0
assert( s == L"String 1" ); 

array[0] = L"String 3"; // Replace element 0 
assert( array[0] == L"String 3" );
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                                                                                |
| Header<br/>                   | <dl> <dt>Chstrauarr. h (Include-Datei "f")</dt> </dl>                                                    |
| Bibliothek<br/>                  | <dl> <dt>Framedyn. lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Chstringarray:: Add**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-add)
</dt> <dt>

[**Chstringarray:: GetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int))
</dt> <dt>

[**Chstringarray::**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr))
</dt> </dl>

