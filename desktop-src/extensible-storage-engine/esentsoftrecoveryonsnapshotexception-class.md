---
description: 'Weitere Informationen finden Sie unter: EsentSoftRecoveryOnSnapshotException-Klasse'
title: EsentSoftRecoveryOnSnapshotException-Klasse
TOCTitle: EsentSoftRecoveryOnSnapshotException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSoftRecoveryOnSnapshotException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentsoftrecoveryonsnapshotexception(v=EXCHG.10)
ms:contentKeyID: 55102866
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSoftRecoveryOnSnapshotException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSoftRecoveryOnSnapshotException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 711595f8fcd3025376e2fbf5ab88aca1cd3eed22a461a20e449e9d8ad5caf755
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119039668"
---
# <a name="esentsoftrecoveryonsnapshotexception-class"></a>EsentSoftRecoveryOnSnapshotException-Klasse

Basisklasse für JET_err. SoftRecoveryOnSnapshot-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentObsoleteException](./esentobsoleteexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentSoftRecoveryOnSnapshotException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSoftRecoveryOnSnapshotException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentSoftRecoveryOnSnapshotException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSoftRecoveryOnSnapshotException : EsentObsoleteException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[EsentSoftRecoveryOnSnapshotException-Member](./esentsoftrecoveryonsnapshotexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
