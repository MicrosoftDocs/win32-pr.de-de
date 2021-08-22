---
description: 'Weitere Informationen finden Sie unter: EsentSecondaryIndexCorruptedException-Klasse'
title: EsentSecondaryIndexCorruptedException-Klasse
TOCTitle: EsentSecondaryIndexCorruptedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSecondaryIndexCorruptedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentsecondaryindexcorruptedexception(v=EXCHG.10)
ms:contentKeyID: 55102677
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSecondaryIndexCorruptedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSecondaryIndexCorruptedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3c99c7fb52466722a505949499175f2718f8d3eb81b7a4a58bdfb4e2fc115e6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118981724"
---
# <a name="esentsecondaryindexcorruptedexception-class"></a>EsentSecondaryIndexCorruptedException-Klasse

Basisklasse für JET_err. SecondaryIndexCorrupted-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentCorruptionException](./esentcorruptionexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentSecondaryIndexCorruptedException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSecondaryIndexCorruptedException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentSecondaryIndexCorruptedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSecondaryIndexCorruptedException : EsentCorruptionException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[EsentSecondaryIndexCorruptedException-Member](./esentsecondaryindexcorruptedexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
