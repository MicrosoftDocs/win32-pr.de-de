---
description: 'Weitere Informationen zu: EsentMultiValuedColumnMustBeTaggedException-Klasse'
title: EsentMultiValuedColumnMustBeTaggedException-Klasse
TOCTitle: EsentMultiValuedColumnMustBeTaggedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMultiValuedColumnMustBeTaggedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmultivaluedcolumnmustbetaggedexception(v=EXCHG.10)
ms:contentKeyID: 55102318
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMultiValuedColumnMustBeTaggedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMultiValuedColumnMustBeTaggedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ac13c4539511b9b63f8e16beb7ed510f3cc438b985e9ecdd84dd15e4466e9e03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119115396"
---
# <a name="esentmultivaluedcolumnmustbetaggedexception-class"></a>EsentMultiValuedColumnMustBeTaggedException-Klasse

Basisklasse für JET_err. MultiValuedColumnMustBeTagged-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentUsageException](./esentusageexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentMultiValuedColumnMustBeTaggedException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMultiValuedColumnMustBeTaggedException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentMultiValuedColumnMustBeTaggedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMultiValuedColumnMustBeTaggedException : EsentUsageException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[EsentMultiValuedColumnMustBeTaggedException-Member](./esentmultivaluedcolumnmustbetaggedexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
