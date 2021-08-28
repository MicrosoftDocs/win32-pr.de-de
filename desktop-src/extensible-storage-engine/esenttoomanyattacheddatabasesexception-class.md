---
description: 'Weitere Informationen finden Sie unter: EsentTooManyAttachedDatabasesException-Klasse'
title: EsentTooManyAttachedDatabasesException-Klasse
TOCTitle: EsentTooManyAttachedDatabasesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManyAttachedDatabasesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanyattacheddatabasesexception(v=EXCHG.10)
ms:contentKeyID: 55103075
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManyAttachedDatabasesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManyAttachedDatabasesException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 567e8d138c2a145b15b9632ebe65602a49fa19d41a6c5b653ea5bf5b701b093d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119668580"
---
# <a name="esenttoomanyattacheddatabasesexception-class"></a>EsentTooManyAttachedDatabasesException-Klasse

Basisklasse für JET_err. TooManyAttachedDatabases-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentUsageException](./esentusageexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentTooManyAttachedDatabasesException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManyAttachedDatabasesException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentTooManyAttachedDatabasesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManyAttachedDatabasesException : EsentUsageException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[EsentTooManyAttachedDatabasesException-Member](./esenttoomanyattacheddatabasesexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
