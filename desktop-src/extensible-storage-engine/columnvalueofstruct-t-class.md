---
description: 'Weitere Informationen finden Sie unter: columnvalueof struct- <T> Klasse'
title: ColumnValueOfStruct(T)-Klasse
TOCTitle: ColumnValueOfStruct(T) class
ms:assetid: T:Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1
ms:mtpsurl: https://msdn.microsoft.com/library/Dn334171(v=EXCHG.10)
ms:contentKeyID: 55100962
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 82083adcaaf0d9f5b4f2a720da83e95cd4b39401
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104351089"
---
# <a name="columnvalueofstructt-class"></a>Columnvalueosstruct- \<T\> Klasse

Legen Sie eine Spalte eines Struktur Typs (z. b. Int32/GUID) fest.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [Microsoft. ISAM. ESENT. Interop. ColumnValue](./columnvalue-class.md)  
    Microsoft. ISAM. ESENT. Interop. columnvalueofistruct\<T\>  
      

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public MustInherit Class ColumnValueOfStruct(Of T As {Structure, New, IEquatable(Of T)}) _
    Inherits ColumnValue
'Usage
Dim instance As ColumnValueOfStruct(Of T)
```

``` csharp
public abstract class ColumnValueOfStruct<T> : ColumnValue
where T : struct, new(), IEquatable<T>
```

#### <a name="type-parameters"></a>Typparameter

  - T  
    Der festzulegende Typ.

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Columnvalueofstruct \<T\> -Member](./columnvalueofstruct-t-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Abgeleitete Typen

[System.Object](/dotnet/api/system.object)  
  [Microsoft. ISAM. ESENT. Interop. ColumnValue](./columnvalue-class.md)  
    Microsoft. ISAM. ESENT. Interop. columnvalueofistruct\<T\>  
      [Microsoft. ISAM. ESENT. Interop. boolcolumnvalue](./boolcolumnvalue-class.md)  
      [Microsoft. ISAM. ESENT. Interop. bytecolumnvalue](./bytecolumnvalue-class.md)  
      [Microsoft. ISAM. ESENT. Interop. datetimecolumnvalue](./datetimecolumnvalue-class.md)  
      [Microsoft. ISAM. ESENT. Interop. doublecolumnvalue](./doublecolumnvalue-class.md)  
      [Microsoft. ISAM. ESENT. Interop. floatcolumnvalue](./floatcolumnvalue-class.md)  
      [Microsoft. ISAM. ESENT. Interop. guidcolumnvalue](./guidcolumnvalue-class.md)  
      [Microsoft. ISAM. ESENT. Interop. Int16ColumnValue](./int16columnvalue-class.md)  
      [Microsoft. ISAM. ESENT. Interop. Int32ColumnValue](./int32columnvalue-class.md)  
      [Microsoft. ISAM. ESENT. Interop. Int64ColumnValue](./int64columnvalue-class.md)  
      [Microsoft. ISAM. ESENT. Interop. UInt16ColumnValue](./uint16columnvalue-class.md)  
      [Microsoft. ISAM. ESENT. Interop. UInt32ColumnValue](./uint32columnvalue-class.md)  
      [Microsoft. ISAM. ESENT. Interop. UInt64ColumnValue](./uint64columnvalue-class.md)