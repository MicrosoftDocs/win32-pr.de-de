---
description: 'Weitere Informationen zu: EsentSessionContextNotSetByThisThreadException-Klasse'
title: EsentSessionContextNotSetByThisThreadException-Klasse
TOCTitle: EsentSessionContextNotSetByThisThreadException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSessionContextNotSetByThisThreadException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentsessioncontextnotsetbythisthreadexception(v=EXCHG.10)
ms:contentKeyID: 55102698
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSessionContextNotSetByThisThreadException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSessionContextNotSetByThisThreadException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 64339a51d0c2afe917ff1fbd41cab996ac0765bf24e2b4b6ae97e98d366f3a64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119039958"
---
# <a name="esentsessioncontextnotsetbythisthreadexception-class"></a>EsentSessionContextNotSetByThisThreadException-Klasse

Basisklasse für JET_err. SessionContextNotSetByThisThread-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentUsageException](./esentusageexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentSessionContextNotSetByThisThreadException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSessionContextNotSetByThisThreadException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentSessionContextNotSetByThisThreadException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSessionContextNotSetByThisThreadException : EsentUsageException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[EsentSessionContextNotSetByThisThreadException-Member](./esentsessioncontextnotsetbythisthreadexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
