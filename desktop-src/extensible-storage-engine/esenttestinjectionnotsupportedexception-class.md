---
description: 'Weitere Informationen finden Sie unter: EsentTestInjectionNotSupportedException-Klasse'
title: EsentTestInjectionNotSupportedException-Klasse
TOCTitle: EsentTestInjectionNotSupportedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTestInjectionNotSupportedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttestinjectionnotsupportedexception(v=EXCHG.10)
ms:contentKeyID: 55103041
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTestInjectionNotSupportedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTestInjectionNotSupportedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ec7df505a27d3c3b72e36143cd2546450e9bb43d43aced465048a289950e18c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120116540"
---
# <a name="esenttestinjectionnotsupportedexception-class"></a>EsentTestInjectionNotSupportedException-Klasse

Basisklasse für JET_err. TestInjectionNotSupported-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentStateException](./esentstateexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentTestInjectionNotSupportedException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTestInjectionNotSupportedException _
    Inherits EsentStateException
'Usage
Dim instance As EsentTestInjectionNotSupportedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTestInjectionNotSupportedException : EsentStateException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[EsentTestInjectionNotSupportedException-Member](./esenttestinjectionnotsupportedexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
