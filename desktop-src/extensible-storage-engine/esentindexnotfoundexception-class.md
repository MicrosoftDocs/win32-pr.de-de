---
description: 'Weitere Informationen finden Sie unter: EsentIndexNotFoundException-Klasse'
title: EsentIndexNotFoundException-Klasse
TOCTitle: EsentIndexNotFoundException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentIndexNotFoundException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentindexnotfoundexception(v=EXCHG.10)
ms:contentKeyID: 55101767
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentIndexNotFoundException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentIndexNotFoundException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: efe5514814daa0078c4ee0bb033185328cfcfed33f2dda32bfc1f764128ccf22
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119724410"
---
# <a name="esentindexnotfoundexception-class"></a>EsentIndexNotFoundException-Klasse

Basisklasse für JET_err. IndexNotFound-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentStateException](./esentstateexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentIndexNotFoundException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentIndexNotFoundException _
    Inherits EsentStateException
'Usage
Dim instance As EsentIndexNotFoundException
```

``` csharp
[SerializableAttribute]
public sealed class EsentIndexNotFoundException : EsentStateException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[EsentIndexNotFoundException-Member](./esentindexnotfoundexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
