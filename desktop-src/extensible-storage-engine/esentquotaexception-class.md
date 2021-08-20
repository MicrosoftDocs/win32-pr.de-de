---
description: 'Weitere Informationen zu: EsentQuotaException-Klasse'
title: EsentQuotaException-Klasse
TOCTitle: EsentQuotaException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentQuotaException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentquotaexception(v=EXCHG.10)
ms:contentKeyID: 55102495
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentQuotaException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentQuotaException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6350dfa9cbdddcf935b4f87fab964d40c1fc65765a254219c542d29b676fed36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119782270"
---
# <a name="esentquotaexception-class"></a>EsentQuotaException-Klasse

Basisklasse für Quota-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentOperationException](./esentoperationexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentResourceException](./esentresourceexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentQuotaException  
              [Microsoft.Isam.Esent.Interop.EsentOutOfDatabaseSpaceException](./esentoutofdatabasespaceexception-class.md)  
              [Microsoft.Isam.Esent.Interop.EsentTooManyInstancesException](./esenttoomanyinstancesexception-class.md)  
              [Microsoft.Isam.Esent.Interop.EsentTooManyOpenTablesException](./esenttoomanyopentablesexception-class.md)  
              [Microsoft.Isam.Esent.Interop.EsentVersionStoreOutOfMemoryException](./esentversionstoreoutofmemoryexception-class.md)  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentQuotaException _
    Inherits EsentResourceException
'Usage
Dim instance As EsentQuotaException
```

``` csharp
[SerializableAttribute]
public abstract class EsentQuotaException : EsentResourceException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[EsentQuotaException-Member](./esentquotaexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
