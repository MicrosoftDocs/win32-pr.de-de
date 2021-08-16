---
description: 'Weitere Informationen zu: EsentRecoveredWithoutUndoDatabasesConsistentException-Klasse'
title: EsentRecoveredWithoutUndoDatabasesConsistentException-Klasse
TOCTitle: EsentRecoveredWithoutUndoDatabasesConsistentException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRecoveredWithoutUndoDatabasesConsistentException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrecoveredwithoutundodatabasesconsistentexception(v=EXCHG.10)
ms:contentKeyID: 55102610
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRecoveredWithoutUndoDatabasesConsistentException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRecoveredWithoutUndoDatabasesConsistentException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 03d4983047121f55d8ef239719384b3c5a40a126f2f5d5b90028eb1209bbb4e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119115250"
---
# <a name="esentrecoveredwithoutundodatabasesconsistentexception-class"></a>EsentRecoveredWithoutUndoDatabasesConsistentException-Klasse

Basisklasse für JET_err. RecoveredWithoutUndoDatabasesConsistent-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentStateException](./esentstateexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentRecoveredWithoutUndoDatabasesConsistentException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRecoveredWithoutUndoDatabasesConsistentException _
    Inherits EsentStateException
'Usage
Dim instance As EsentRecoveredWithoutUndoDatabasesConsistentException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRecoveredWithoutUndoDatabasesConsistentException : EsentStateException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[EsentRecoveredWithoutUndoDatabasesConsistentException-Member](./esentrecoveredwithoutundodatabasesconsistentexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
