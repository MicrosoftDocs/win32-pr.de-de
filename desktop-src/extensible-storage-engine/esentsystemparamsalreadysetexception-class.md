---
description: 'Weitere Informationen finden Sie unter: EsentSystemParamsAlreadySetException-Klasse'
title: EsentSystemParamsAlreadySetException-Klasse
TOCTitle: EsentSystemParamsAlreadySetException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSystemParamsAlreadySetException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentsystemparamsalreadysetexception(v=EXCHG.10)
ms:contentKeyID: 55103003
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSystemParamsAlreadySetException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSystemParamsAlreadySetException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d401f284f29cecdc117433b3dbf692fc94c9b7278a65ba96a1e1e4f1ed9c8e45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119113633"
---
# <a name="esentsystemparamsalreadysetexception-class"></a>EsentSystemParamsAlreadySetException-Klasse

Basisklasse für JET_err.SystemParamsAlreadySet-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentUsageException](./esentusageexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentSystemParamsAlreadySetException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSystemParamsAlreadySetException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentSystemParamsAlreadySetException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSystemParamsAlreadySetException : EsentUsageException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[EsentSystemParamsAlreadySetException-Member](./esentsystemparamsalreadysetexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
