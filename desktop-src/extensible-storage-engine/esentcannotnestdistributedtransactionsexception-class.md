---
description: 'Weitere Informationen zu: EsentCannotNestDistributedTransactionsException-Klasse'
title: EsentCannotNestDistributedTransactionsException-Klasse
TOCTitle: EsentCannotNestDistributedTransactionsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCannotNestDistributedTransactionsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcannotnestdistributedtransactionsexception(v=EXCHG.10)
ms:contentKeyID: 55101211
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCannotNestDistributedTransactionsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCannotNestDistributedTransactionsException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 93c13ce7d5593890c734705292f6be33fcb60eef21d8b5123c8c59f7e3f6e866
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120066410"
---
# <a name="esentcannotnestdistributedtransactionsexception-class"></a>EsentCannotNestDistributedTransactionsException-Klasse

Basisklasse für JET_err. CannotNestDistributedTransactions-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentObsoleteException](./esentobsoleteexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentCannotNestDistributedTransactionsException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentCannotNestDistributedTransactionsException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentCannotNestDistributedTransactionsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentCannotNestDistributedTransactionsException : EsentObsoleteException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[EsentCannotNestDistributedTransactionsException-Member](./esentcannotnestdistributedtransactionsexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
