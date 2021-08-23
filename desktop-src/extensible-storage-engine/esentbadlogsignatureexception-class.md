---
description: 'Weitere Informationen zu: EsentBadLogSignatureException-Klasse'
title: EsentBadLogSignatureException-Klasse
TOCTitle: EsentBadLogSignatureException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentBadLogSignatureException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentbadlogsignatureexception(v=EXCHG.10)
ms:contentKeyID: 55101128
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentBadLogSignatureException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentBadLogSignatureException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 00bfdc6a2653eaa315516375f5296fd14b1e5b44403b9651bf0dc119c20b4933
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622736"
---
# <a name="esentbadlogsignatureexception-class"></a>EsentBadLogSignatureException-Klasse

Basisklasse für JET_err. BadLogSignature-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentInconsistentException](./esentinconsistentexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentBadLogSignatureException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentBadLogSignatureException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentBadLogSignatureException
```

``` csharp
[SerializableAttribute]
public sealed class EsentBadLogSignatureException : EsentInconsistentException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[EsentBadLogSignatureException-Member](./esentbadlogsignatureexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
