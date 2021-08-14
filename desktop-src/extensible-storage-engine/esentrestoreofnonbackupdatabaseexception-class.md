---
description: 'Weitere Informationen zu: EsentRestoreOfNonBackupDatabaseException-Klasse'
title: EsentRestoreOfNonBackupDatabaseException-Klasse
TOCTitle: EsentRestoreOfNonBackupDatabaseException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRestoreOfNonBackupDatabaseException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrestoreofnonbackupdatabaseexception(v=EXCHG.10)
ms:contentKeyID: 55102655
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRestoreOfNonBackupDatabaseException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRestoreOfNonBackupDatabaseException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cdac997bfed469129e2b1999c0ddf75cd01b3d237be529f85e8614a77a534d01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118774008"
---
# <a name="esentrestoreofnonbackupdatabaseexception-class"></a>EsentRestoreOfNonBackupDatabaseException-Klasse

Basisklasse für JET_err. RestoreOfNonBackupDatabase-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentUsageException](./esentusageexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentRestoreOfNonBackupDatabaseException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRestoreOfNonBackupDatabaseException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentRestoreOfNonBackupDatabaseException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRestoreOfNonBackupDatabaseException : EsentUsageException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[EsentRestoreOfNonBackupDatabaseException-Member](./esentrestoreofnonbackupdatabaseexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
