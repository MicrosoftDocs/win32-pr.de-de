---
description: 'Weitere Informationen zu: EsentBackupNotAllowedYetException-Klasse'
title: EsentBackupNotAllowedYetException-Klasse
TOCTitle: EsentBackupNotAllowedYetException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentBackupNotAllowedYetException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentbackupnotallowedyetexception(v=EXCHG.10)
ms:contentKeyID: 55101088
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentBackupNotAllowedYetException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentBackupNotAllowedYetException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a1c6876c0b5b793f2dd0a3c8a19ddf4f8e4b4cf447a1323a49f0e0a5cbd8f15d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118083201"
---
# <a name="esentbackupnotallowedyetexception-class"></a>EsentBackupNotAllowedYetException-Klasse

Basisklasse für JET_err. BackupNotAllowedYet-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentStateException](./esentstateexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentBackupNotAllowedYetException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentBackupNotAllowedYetException _
    Inherits EsentStateException
'Usage
Dim instance As EsentBackupNotAllowedYetException
```

``` csharp
[SerializableAttribute]
public sealed class EsentBackupNotAllowedYetException : EsentStateException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[EsentBackupNotAllowedYetException-Member](./esentbackupnotallowedyetexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
