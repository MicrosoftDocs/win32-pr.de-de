---
description: Diese Tiefgestelltoperatoren legen das Element am angegebenen Index fest oder erhalten es. Diese Operatoren sind ein praktischer Ersatz für die Methoden SetAt und GetAt.
ms.assetid: 93b10bef-908e-4c5e-aac3-b13051b2e7c9
ms.tgt_platform: multiple
title: CHStringArray::operator [ ] (ChStrArr.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 859cfe52535aea0fb43d6195648215431f80cff86f0525b9ef7c5247b6a831a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131772"
---
# <a name="chstringarrayoperator--"></a>CHStringArray::operator \[\]

\[Die [**CHStringArray-Klasse**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) ist Teil des WMI-Anbieterframeworks, das jetzt als endgültiger Zustand betrachtet wird. Für nicht sicherheitsrelevante Probleme, die sich auf diese Bibliotheken auswirken, sind keine weiteren Entwicklungen, Erweiterungen oder Updates verfügbar. Die [MI-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle Neuentwicklungen verwendet werden.\]

Diese Tiefgestelltoperatoren legen das Element am angegebenen Index fest oder erhalten es. Diese Operatoren sind ein praktischer Ersatz für die [**Methoden SetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr)) und [**GetAt.**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int))

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

Ein ganzzahliger Index, der größer oder gleich 0 (null) und kleiner oder gleich dem von [ **GetUpperBound** zurückgegebenen Wert ist](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getupperbound)

</dd> </dl>

## <a name="return-values"></a>Rückgabewerte

Die Subscript-Operatoren geben das [**CHString-Zeigerelement**](chstring.md) zurück, das sich derzeit an diesem Index befindet.

## <a name="remarks"></a>Hinweise

Sie können den ersten Operator verwenden, der Arrays **aufruft,** die nicht const sind, entweder rechts (r-value) oder links (l-value) einer Zuweisungs-Anweisung. Die zweite , die **const-Arrays aufruft,** kann nur auf der rechten Seite verwendet werden.

Die Debugversion der Bibliothek bestätigt, ob der Tiefskript (auf der linken oder rechten Seite einer Zuweisungsaufstellung) außerhalb der Grenzen liegt.

## <a name="examples"></a>Beispiele

Das folgende Codebeispiel zeigt die Verwendung von [**\[ \] CHStringArray::operator**](/previous-versions/windows/desktop/legacy/aa384934(v=vs.85)).


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
| Header<br/>                   | <dl> <dt>ChStrArr.h (include FwCommon.h)</dt> </dl>                                                    |
| Bibliothek<br/>                  | <dl> <dt>FrameDyn.lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CHStringArray::Add**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-add)
</dt> <dt>

[**CHStringArray::GetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int))
</dt> <dt>

[**CHStringArray::SetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr))
</dt> </dl>

