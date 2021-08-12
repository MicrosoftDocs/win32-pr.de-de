---
description: 'Weitere Informationen zu: EsentGivenLogFileIsNotContiguousException-Klasse'
title: EsentGivenLogFileIsNotContiguousException-Klasse
TOCTitle: EsentGivenLogFileIsNotContiguousException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentGivenLogFileIsNotContiguousException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentgivenlogfileisnotcontiguousexception(v=EXCHG.10)
ms:contentKeyID: 55101788
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentGivenLogFileIsNotContiguousException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentGivenLogFileIsNotContiguousException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2e1ed504581d47c4c20072aed320080351ca2f42cc15296d42aac1386a1a86f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118268307"
---
# <a name="esentgivenlogfileisnotcontiguousexception-class"></a>EsentGivenLogFileIsNotContiguousException-Klasse

Basisklasse für JET_err. GivenLogFileIsNotContiguous-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentInconsistentException](./esentinconsistentexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentGivenLogFileIsNotContiguousException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentGivenLogFileIsNotContiguousException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentGivenLogFileIsNotContiguousException
```

``` csharp
[SerializableAttribute]
public sealed class EsentGivenLogFileIsNotContiguousException : EsentInconsistentException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[EsentGivenLogFileIsNotContiguousException-Member](./esentgivenlogfileisnotcontiguousexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
