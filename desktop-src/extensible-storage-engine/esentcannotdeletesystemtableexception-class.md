---
description: 'Weitere Informationen zu: EsentCannotDeleteSystemTableException-Klasse'
title: EsentCannotDeleteSystemTableException-Klasse
TOCTitle: EsentCannotDeleteSystemTableException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCannotDeleteSystemTableException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcannotdeletesystemtableexception(v=EXCHG.10)
ms:contentKeyID: 55101231
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCannotDeleteSystemTableException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCannotDeleteSystemTableException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8a07f33fe85bb6841804425c15e9392a4fdacece4e67b93e56fbf9fdc2f0d54f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117715387"
---
# <a name="esentcannotdeletesystemtableexception-class"></a>EsentCannotDeleteSystemTableException-Klasse

Basisklasse für JET_err. CannotDeleteSystemTable-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentUsageException](./esentusageexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentCannotDeleteSystemTableException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentCannotDeleteSystemTableException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentCannotDeleteSystemTableException
```

``` csharp
[SerializableAttribute]
public sealed class EsentCannotDeleteSystemTableException : EsentUsageException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[EsentCannotDeleteSystemTableException-Member](./esentcannotdeletesystemtableexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
