---
description: 'Weitere Informationen zu: EsentEndingRestoreLogTooLowException-Klasse'
title: EsentEndingRestoreLogTooLowException-Klasse
TOCTitle: EsentEndingRestoreLogTooLowException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentEndingRestoreLogTooLowException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentendingrestorelogtoolowexception(v=EXCHG.10)
ms:contentKeyID: 55101575
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentEndingRestoreLogTooLowException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentEndingRestoreLogTooLowException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d5ab46112e7328b8258bd2428c84b7d622d4af28e3b015a2c951d480e6c4880e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119973895"
---
# <a name="esentendingrestorelogtoolowexception-class"></a>EsentEndingRestoreLogTooLowException-Klasse

Basisklasse für JET_err. EndingRestoreLogTooLow-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentInconsistentException](./esentinconsistentexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentEndingRestoreLogTooLowException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentEndingRestoreLogTooLowException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentEndingRestoreLogTooLowException
```

``` csharp
[SerializableAttribute]
public sealed class EsentEndingRestoreLogTooLowException : EsentInconsistentException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[EsentEndingRestoreLogTooLowException-Member](./esentendingrestorelogtoolowexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
