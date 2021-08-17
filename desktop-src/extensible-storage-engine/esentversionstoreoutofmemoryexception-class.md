---
description: 'Weitere Informationen finden Sie unter: EsentVersionStoreOutOfMemoryException-Klasse'
title: EsentVersionStoreOutOfMemoryException-Klasse
TOCTitle: EsentVersionStoreOutOfMemoryException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentVersionStoreOutOfMemoryException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentversionstoreoutofmemoryexception(v=EXCHG.10)
ms:contentKeyID: 55103197
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentVersionStoreOutOfMemoryException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentVersionStoreOutOfMemoryException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e8db95ff21192ae3d5d11465a14731e2f6f074b8a8da44e62b68fcb70e157c6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119112679"
---
# <a name="esentversionstoreoutofmemoryexception-class"></a>EsentVersionStoreOutOfMemoryException-Klasse

Basisklasse für JET_err. VersionsstoreOutOfMemory-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentOperationException](./esentoperationexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentResourceException](./esentresourceexception-class.md)  
            [Microsoft.Isam.Esent.Interop.EsentQuotaException](./esentquotaexception-class.md)  
              Microsoft.Isam.Esent.Interop.EsentVersionStoreOutOfMemoryException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentVersionStoreOutOfMemoryException _
    Inherits EsentQuotaException
'Usage
Dim instance As EsentVersionStoreOutOfMemoryException
```

``` csharp
[SerializableAttribute]
public sealed class EsentVersionStoreOutOfMemoryException : EsentQuotaException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[EsentVersionStoreOutOfMemoryException-Member](./esentversionstoreoutofmemoryexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
