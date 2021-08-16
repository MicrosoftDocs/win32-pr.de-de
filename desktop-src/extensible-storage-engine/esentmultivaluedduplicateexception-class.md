---
description: 'Weitere Informationen finden Sie unter: EsentMultiValuedDuplicateException-Klasse'
title: EsentMultiValuedDuplicateException-Klasse
TOCTitle: EsentMultiValuedDuplicateException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmultivaluedduplicateexception(v=EXCHG.10)
ms:contentKeyID: 55102340
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4ff8d4284f9e726a267a4b1e8cd5e8052ed72feb8919d199dacc0b382ab0010e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119115379"
---
# <a name="esentmultivaluedduplicateexception-class"></a>EsentMultiValuedDuplicateException-Klasse

Basisklasse für JET_err. MultiValuedDuplicate-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentStateException](./esentstateexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMultiValuedDuplicateException _
    Inherits EsentStateException
'Usage
Dim instance As EsentMultiValuedDuplicateException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMultiValuedDuplicateException : EsentStateException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[EsentMultiValuedDuplicateException-Member](./esentmultivaluedduplicateexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
