---
description: 'Weitere Informationen zu: EsentBackupDirectoryNotEmptyException-Klasse'
title: EsentBackupDirectoryNotEmptyException-Klasse
TOCTitle: EsentBackupDirectoryNotEmptyException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentBackupDirectoryNotEmptyException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentbackupdirectorynotemptyexception(v=EXCHG.10)
ms:contentKeyID: 55101028
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentBackupDirectoryNotEmptyException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentBackupDirectoryNotEmptyException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c7147fc0bec897fda4119edc8be5f56c28af9037b413a8d786dd33c0e79542f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737470"
---
# <a name="esentbackupdirectorynotemptyexception-class"></a>EsentBackupDirectoryNotEmptyException-Klasse

Basisklasse für JET_err. BackupDirectoryNotEmpty-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentUsageException](./esentusageexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentBackupDirectoryNotEmptyException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentBackupDirectoryNotEmptyException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentBackupDirectoryNotEmptyException
```

``` csharp
[SerializableAttribute]
public sealed class EsentBackupDirectoryNotEmptyException : EsentUsageException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[EsentBackupDirectoryNotEmptyException-Member](./esentbackupdirectorynotemptyexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
