---
description: 'Weitere Informationen zu: EsentBadRestoreTargetInstanceException-Klasse'
title: EsentBadRestoreTargetInstanceException-Klasse
TOCTitle: EsentBadRestoreTargetInstanceException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentBadRestoreTargetInstanceException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentbadrestoretargetinstanceexception(v=EXCHG.10)
ms:contentKeyID: 55101100
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentBadRestoreTargetInstanceException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentBadRestoreTargetInstanceException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 868f9ec88c744b90d35f5fe4cff7baafb7f5a371118d994a153b09c8ba4d51cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117715600"
---
# <a name="esentbadrestoretargetinstanceexception-class"></a>EsentBadRestoreTargetInstanceException-Klasse

Basisklasse für JET_err. BadRestoreTargetInstance-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentUsageException](./esentusageexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentBadRestoreTargetInstanceException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentBadRestoreTargetInstanceException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentBadRestoreTargetInstanceException
```

``` csharp
[SerializableAttribute]
public sealed class EsentBadRestoreTargetInstanceException : EsentUsageException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[EsentBadRestoreTargetInstanceException-Member](./esentbadrestoretargetinstanceexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
