---
description: 'Erfahren Sie mehr über: ColumnValueOfStruct <T> . CheckDataCount-Methode'
title: ColumnValueOfStruct(T). CheckDataCount-Methode
TOCTitle: 'CheckDataCount method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1.CheckDataCount(System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/Dn334178(v=EXCHG.10)
ms:contentKeyID: 55100977
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1.CheckDataCount
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1.CheckDataCount
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a9f70d2e26c8ee56e88f0405af19f17476612bd9a5f51ba624088ed9d58380d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120066940"
---
# <a name="columnvalueofstructtcheckdatacount-method"></a>ColumnValueOfStruct \<T\> . CheckDataCount-Methode

Stellen Sie sicher, dass die abgerufenen Daten genau die Größe haben, die für die Struktur erforderlich ist. Bei einem Konflikt wird eine Ausnahme ausgelöst.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Protected Sub CheckDataCount ( _
    count As Integer _
)
'Usage
Dim count As Integer

Me.CheckDataCount(count)
```

``` csharp
protected void CheckDataCount(
    int count
)
```

#### <a name="parameters"></a>Parameter

  - count  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Die Größe der abgerufenen Daten.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[ColumnValueOfStruct-Klasse \<T\>](./columnvalueofstruct-t-class.md)

[ColumnValueOfStruct-Elemente \<T\>](./columnvalueofstruct-t-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
