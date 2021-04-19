---
description: 'Weitere Informationen finden Sie unter: esentfragmentationexception-Klasse'
title: EsentFragmentationException-Klasse
TOCTitle: EsentFragmentationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFragmentationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfragmentationexception(v=EXCHG.10)
ms:contentKeyID: 55101771
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFragmentationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFragmentationException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 081198a696be9982e1fd8a7e4f1468e6d63d1c97
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106355091"
---
# <a name="esentfragmentationexception-class"></a>EsentFragmentationException-Klasse

Basisklasse für Fragmentierungs Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. esentexception](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. esenterrorexception](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. esentdataexception](./esentdataexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. esentfragmentationexception  
            

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentFragmentationException _
    Inherits EsentDataException
'Usage
Dim instance As EsentFragmentationException
```

``` csharp
[SerializableAttribute]
public abstract class EsentFragmentationException : EsentDataException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Esentfragmentationexception-Member](./esentfragmentationexception-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Abgeleitete Typen

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. esentexception](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. esenterrorexception](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. esentdataexception](./esentdataexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. esentfragmentationexception  
            [Microsoft. ISAM. ESENT. Interop. esentlogsector sizemismatchexception](./esentlogsectorsizemismatchexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. EsentLogSequenceEndDatabasesConsistentException](./esentlogsequenceenddatabasesconsistentexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentlogsequenceendexception](./esentlogsequenceendexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentouesf autoincrementvaluesexception](./esentoutofautoincrementvaluesexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentouesf dbtimevaluesexception](./esentoutofdbtimevaluesexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentouesflongvalueidsexception](./esentoutoflongvalueidsexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentouesfobjectidsexception](./esentoutofobjectidsexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentouesf sequentialindexvaluesexception](./esentoutofsequentialindexvaluesexception-class.md)