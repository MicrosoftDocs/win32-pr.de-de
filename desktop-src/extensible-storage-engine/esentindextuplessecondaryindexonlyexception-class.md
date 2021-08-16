---
description: 'Weitere Informationen finden Sie unter: EsentIndexTuplesSecondaryIndexOnlyException-Klasse'
title: EsentIndexTuplesSecondaryIndexOnlyException-Klasse
TOCTitle: EsentIndexTuplesSecondaryIndexOnlyException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentIndexTuplesSecondaryIndexOnlyException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentindextuplessecondaryindexonlyexception(v=EXCHG.10)
ms:contentKeyID: 55101794
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentIndexTuplesSecondaryIndexOnlyException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentIndexTuplesSecondaryIndexOnlyException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 30f3b510984e12a71eee0b39a6228d8b6d5b768c445017cbbdefc5122d596e37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783960"
---
# <a name="esentindextuplessecondaryindexonlyexception-class"></a>EsentIndexTuplesSecondaryIndexOnlyException-Klasse

Basisklasse für JET_err. IndexTuplesSecondaryIndexOnly-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentUsageException](./esentusageexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentIndexTuplesSecondaryIndexOnlyException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentIndexTuplesSecondaryIndexOnlyException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentIndexTuplesSecondaryIndexOnlyException
```

``` csharp
[SerializableAttribute]
public sealed class EsentIndexTuplesSecondaryIndexOnlyException : EsentUsageException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[EsentIndexTuplesSecondaryIndexOnlyException-Member](./esentindextuplessecondaryindexonlyexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
