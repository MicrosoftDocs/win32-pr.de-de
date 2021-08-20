---
description: 'Weitere Informationen zu: EsentCheckpointDepthTooDeepException-Klasse'
title: EsentCheckpointDepthTooDeepException-Klasse
TOCTitle: EsentCheckpointDepthTooDeepException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCheckpointDepthTooDeepException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcheckpointdepthtoodeepexception(v=EXCHG.10)
ms:contentKeyID: 55101222
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCheckpointDepthTooDeepException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCheckpointDepthTooDeepException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 73eb60f795d285186474de73a175f19e95a3a6dafb2b9db04356dc4f5e6851c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117714506"
---
# <a name="esentcheckpointdepthtoodeepexception-class"></a>EsentCheckpointDepthTooDeepException-Klasse

Basisklasse für JET_err. CheckpointDepthTooDeep-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentOperationException](./esentoperationexception-class.md)  
          Microsoft.Isam.Esent.Interop.EsentCheckpointDepthTooDeepException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentCheckpointDepthTooDeepException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentCheckpointDepthTooDeepException
```

``` csharp
[SerializableAttribute]
public sealed class EsentCheckpointDepthTooDeepException : EsentOperationException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[EsentCheckpointDepthTooDeepException-Member](./esentcheckpointdepthtoodeepexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
