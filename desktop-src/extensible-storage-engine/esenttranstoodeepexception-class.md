---
description: 'Weitere Informationen zu: EsentTransTooDeepException-Klasse'
title: EsentTransTooDeepException-Klasse
TOCTitle: EsentTransTooDeepException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTransTooDeepException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttranstoodeepexception(v=EXCHG.10)
ms:contentKeyID: 55107315
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTransTooDeepException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTransTooDeepException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1d01c9216d7d386889411e60afc88ecbdd53af1a174f607b7ed4073443b7787d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117706630"
---
# <a name="esenttranstoodeepexception-class"></a>EsentTransTooDeepException-Klasse

Basisklasse für JET_err. TransTooDeep-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentUsageException](./esentusageexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentTransTooDeepException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTransTooDeepException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentTransTooDeepException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTransTooDeepException : EsentUsageException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[EsentTransTooDeepException-Member](./esenttranstoodeepexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
