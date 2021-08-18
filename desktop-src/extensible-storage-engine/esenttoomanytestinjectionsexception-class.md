---
description: 'Weitere Informationen zu: EsentTooManyTestInjectionsException-Klasse'
title: EsentTooManyTestInjectionsException-Klasse
TOCTitle: EsentTooManyTestInjectionsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManyTestInjectionsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanytestinjectionsexception(v=EXCHG.10)
ms:contentKeyID: 55107367
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManyTestInjectionsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManyTestInjectionsException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9e5c90ccda8585f208917447ec3b1f331b1743bdbd0be3f24800c08d50233818
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119112900"
---
# <a name="esenttoomanytestinjectionsexception-class"></a>EsentTooManyTestInjectionsException-Klasse

Basisklasse für JET_err. TooManyTestInjections-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentUsageException](./esentusageexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentTooManyTestInjectionsException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManyTestInjectionsException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentTooManyTestInjectionsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManyTestInjectionsException : EsentUsageException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[EsentTooManyTestInjectionsException-Member](./esenttoomanytestinjectionsexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
