---
description: 'Weitere Informationen zu: EsentCannotSeparateIntrinsicLVException-Klasse'
title: EsentCannotSeparateIntrinsicLVException-Klasse
TOCTitle: EsentCannotSeparateIntrinsicLVException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCannotSeparateIntrinsicLVException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcannotseparateintrinsiclvexception(v=EXCHG.10)
ms:contentKeyID: 55101176
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCannotSeparateIntrinsicLVException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCannotSeparateIntrinsicLVException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 20389614c2222031be28ee472efcdd7504ceb193e021c09ef935d00a1877ffe6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119561370"
---
# <a name="esentcannotseparateintrinsiclvexception-class"></a>EsentCannotSeparateIntrinsicLVException-Klasse

Basisklasse für JET_err. CannotSeparateIntrinsicLV-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentUsageException](./esentusageexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentCannotSeparateIntrinsicLVException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentCannotSeparateIntrinsicLVException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentCannotSeparateIntrinsicLVException
```

``` csharp
[SerializableAttribute]
public sealed class EsentCannotSeparateIntrinsicLVException : EsentUsageException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[EsentCannotSeparateIntrinsicLVException-Member](./esentcannotseparateintrinsiclvexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
