---
description: 'Weitere Informationen finden Sie unter: EsentMustCommitDistributedTransactionToLevel0Exception-Klasse'
title: EsentMustCommitDistributedTransactionToLevel0Exception-Klasse
TOCTitle: EsentMustCommitDistributedTransactionToLevel0Exception class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMustCommitDistributedTransactionToLevel0Exception
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmustcommitdistributedtransactiontolevel0exception(v=EXCHG.10)
ms:contentKeyID: 55102329
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMustCommitDistributedTransactionToLevel0Exception
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMustCommitDistributedTransactionToLevel0Exception
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: efd2469c0f3adeeb56062cd1cd889df9aa70fe94dc4266045d8957fbd82f5311
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119782660"
---
# <a name="esentmustcommitdistributedtransactiontolevel0exception-class"></a>EsentMustCommitDistributedTransactionToLevel0Exception-Klasse

Basisklasse für JET_err. MustCommitDistributedTransactionToLevel0-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentObsoleteException](./esentobsoleteexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentMustCommitDistributedTransactionToLevel0Exception  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMustCommitDistributedTransactionToLevel0Exception _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentMustCommitDistributedTransactionToLevel0Exception
```

``` csharp
[SerializableAttribute]
public sealed class EsentMustCommitDistributedTransactionToLevel0Exception : EsentObsoleteException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[EsentMustCommitDistributedTransactionToLevel0Exception-Member](./esentmustcommitdistributedtransactiontolevel0exception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
