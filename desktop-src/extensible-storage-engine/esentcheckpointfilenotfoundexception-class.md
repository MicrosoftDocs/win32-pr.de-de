---
description: 'Weitere Informationen zu: EsentCheckpointFileNotFoundException-Klasse'
title: EsentCheckpointFileNotFoundException-Klasse
TOCTitle: EsentCheckpointFileNotFoundException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCheckpointFileNotFoundException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcheckpointfilenotfoundexception(v=EXCHG.10)
ms:contentKeyID: 55101224
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCheckpointFileNotFoundException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCheckpointFileNotFoundException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8f2572ac979477005d7b417c4df6efa13ad016cabbaaf49cbb4a239f701d1fe5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119116940"
---
# <a name="esentcheckpointfilenotfoundexception-class"></a>EsentCheckpointFileNotFoundException-Klasse

Basisklasse für JET_err. CheckpointFileNotFound-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentInconsistentException](./esentinconsistentexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentCheckpointFileNotFoundException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentCheckpointFileNotFoundException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentCheckpointFileNotFoundException
```

``` csharp
[SerializableAttribute]
public sealed class EsentCheckpointFileNotFoundException : EsentInconsistentException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[EsentCheckpointFileNotFoundException-Member](./esentcheckpointfilenotfoundexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
