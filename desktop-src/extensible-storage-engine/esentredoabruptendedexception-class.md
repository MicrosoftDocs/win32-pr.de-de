---
description: 'Weitere Informationen finden Sie unter: EsentRedoAbruptEndedException-Klasse'
title: EsentRedoAbruptEndedException-Klasse
TOCTitle: EsentRedoAbruptEndedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRedoAbruptEndedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentredoabruptendedexception(v=EXCHG.10)
ms:contentKeyID: 55102536
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRedoAbruptEndedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRedoAbruptEndedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 78e29f61bae90e35439d78c607f3b87355156d5e14d743660951e8f794dbaa26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118982020"
---
# <a name="esentredoabruptendedexception-class"></a>EsentRedoAbruptEndedException-Klasse

Basisklasse für JET_err. RedoAbruptEnded-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentCorruptionException](./esentcorruptionexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentRedoAbruptEndedException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRedoAbruptEndedException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentRedoAbruptEndedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRedoAbruptEndedException : EsentCorruptionException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[EsentRedoAbruptEndedException-Member](./esentredoabruptendedexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
