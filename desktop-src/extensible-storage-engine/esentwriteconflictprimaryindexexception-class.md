---
description: 'Weitere Informationen zu: EsentWriteConflictPrimaryIndexException-Klasse'
title: EsentWriteConflictPrimaryIndexException-Klasse
TOCTitle: EsentWriteConflictPrimaryIndexException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentWriteConflictPrimaryIndexException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentwriteconflictprimaryindexexception(v=EXCHG.10)
ms:contentKeyID: 55107366
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentWriteConflictPrimaryIndexException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentWriteConflictPrimaryIndexException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: de1cbe1c5cadcc0a19354d6eec9f19f78c996cd333763029f5ce6f911d0a9263
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119233990"
---
# <a name="esentwriteconflictprimaryindexexception-class"></a>EsentWriteConflictPrimaryIndexException-Klasse

Basisklasse für JET_err. WriteConflictPrimaryIndex-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentStateException](./esentstateexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentWriteConflictPrimaryIndexException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentWriteConflictPrimaryIndexException _
    Inherits EsentStateException
'Usage
Dim instance As EsentWriteConflictPrimaryIndexException
```

``` csharp
[SerializableAttribute]
public sealed class EsentWriteConflictPrimaryIndexException : EsentStateException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[EsentWriteConflictPrimaryIndexException-Member](./esentwriteconflictprimaryindexexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
