---
description: 'Weitere Informationen finden Sie unter: EsentExistingLogFileIsNotContiguousException-Klasse'
title: EsentExistingLogFileIsNotContiguousException-Klasse
TOCTitle: EsentExistingLogFileIsNotContiguousException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentExistingLogFileIsNotContiguousException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentexistinglogfileisnotcontiguousexception(v=EXCHG.10)
ms:contentKeyID: 55101598
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentExistingLogFileIsNotContiguousException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentExistingLogFileIsNotContiguousException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5c9179f3ee34e93ac84785f6232968ab82ec172578e08a4c90dcafc1fa29f40f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118496819"
---
# <a name="esentexistinglogfileisnotcontiguousexception-class"></a>EsentExistingLogFileIsNotContiguousException-Klasse

Basisklasse für JET_err. ExistingLogFileIsNotContiguous-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentInconsistentException](./esentinconsistentexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentExistingLogFileIsNotContiguousException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentExistingLogFileIsNotContiguousException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentExistingLogFileIsNotContiguousException
```

``` csharp
[SerializableAttribute]
public sealed class EsentExistingLogFileIsNotContiguousException : EsentInconsistentException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[EsentExistingLogFileIsNotContiguousException-Member](./esentexistinglogfileisnotcontiguousexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
