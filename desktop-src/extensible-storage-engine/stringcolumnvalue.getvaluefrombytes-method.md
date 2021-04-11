---
description: Weitere Informationen finden Sie in der stringcolumnvalue. getvaluefromb tes-Methode.
title: Stringcolumnvalue. getvaluefrombytes-Methode
TOCTitle: 'GetValueFromBytes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.StringColumnValue.GetValueFromBytes(System.Byte[],System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.stringcolumnvalue.getvaluefrombytes(v=EXCHG.10)
ms:contentKeyID: 55104020
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.StringColumnValue.GetValueFromBytes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.StringColumnValue.GetValueFromBytes
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 20e8f0f3d30adf73959650415c12018eceeb2642
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218251"
---
# <a name="stringcolumnvaluegetvaluefrombytes-method"></a>Stringcolumnvalue. getvaluefrombytes-Methode

Wenn Sie Daten aus ESENT abrufen, decodieren Sie die Daten, und legen Sie den Wert im ColumnValue-Objekt fest.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Protected Overrides Sub GetValueFromBytes ( _
    value As Byte(), _
    startIndex As Integer, _
    count As Integer, _
    err As Integer _
)
'Usage
Dim value As Byte()
Dim startIndex As Integer
Dim count As Integer
Dim err As Integer

Me.GetValueFromBytes(value, startIndex, _
    count, err)
```

``` csharp
protected override void GetValueFromBytes(
    byte[] value,
    int startIndex,
    int count,
    int err
)
```

#### <a name="parameters"></a>Parameter

  - value  
    Sorte \[\]  
    
    Ein Bytearray.

<!-- end list -->

  - startIndex  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Die Anfangsposition innerhalb der Bytes.

<!-- end list -->

  - count  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Die Anzahl der zu decodierenden Bytes.

<!-- end list -->

  - irre  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Der von ESENT zurückgegebene Fehler.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Stringcolumnvalue-Klasse](./stringcolumnvalue-class.md)

[Stringcolumnvalue-Member](./stringcolumnvalue-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
