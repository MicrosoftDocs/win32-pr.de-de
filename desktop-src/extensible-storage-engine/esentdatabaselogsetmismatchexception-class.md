---
description: 'Weitere Informationen finden Sie unter: EsentDatabaseLogSetMismatchException-Klasse'
title: EsentDatabaseLogSetMismatchException-Klasse
TOCTitle: EsentDatabaseLogSetMismatchException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseLogSetMismatchException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabaselogsetmismatchexception(v=EXCHG.10)
ms:contentKeyID: 55101422
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseLogSetMismatchException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseLogSetMismatchException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fcc389dd7727627eee0d06f4c153787879b9b0ae9b61de8260c19fe65500a2ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117712339"
---
# <a name="esentdatabaselogsetmismatchexception-class"></a>EsentDatabaseLogSetMismatchException-Klasse

Basisklasse für JET_err. DatabaseLogSetMismatch-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentInconsistentException](./esentinconsistentexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentDatabaseLogSetMismatchException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseLogSetMismatchException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentDatabaseLogSetMismatchException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseLogSetMismatchException : EsentInconsistentException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[EsentDatabaseLogSetMismatchException-Member](./esentdatabaselogsetmismatchexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
