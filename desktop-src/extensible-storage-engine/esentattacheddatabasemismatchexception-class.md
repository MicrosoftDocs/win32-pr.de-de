---
description: 'Weitere Informationen finden Sie unter: EsentAttachedDatabaseMismatchException-Klasse'
title: EsentAttachedDatabaseMismatchException-Klasse
TOCTitle: EsentAttachedDatabaseMismatchException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentAttachedDatabaseMismatchException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentattacheddatabasemismatchexception(v=EXCHG.10)
ms:contentKeyID: 55101019
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentAttachedDatabaseMismatchException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentAttachedDatabaseMismatchException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cbf30cc758fac35cb881759ad6c1e3c916ab0159906e4767bc1739f4b6ff6884
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119404200"
---
# <a name="esentattacheddatabasemismatchexception-class"></a>EsentAttachedDatabaseMismatchException-Klasse

Basisklasse für JET_err. AttachedDatabaseMismatch-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentInconsistentException](./esentinconsistentexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentAttachedDatabaseMismatchException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentAttachedDatabaseMismatchException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentAttachedDatabaseMismatchException
```

``` csharp
[SerializableAttribute]
public sealed class EsentAttachedDatabaseMismatchException : EsentInconsistentException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[EsentAttachedDatabaseMismatchException-Member](./esentattacheddatabasemismatchexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
