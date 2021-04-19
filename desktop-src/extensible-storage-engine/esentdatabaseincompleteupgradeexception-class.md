---
description: 'Weitere Informationen finden Sie unter: esentdatabasein completeupgradeexception-Klasse'
title: Esentdatabaseingecompleteupgradeexception-Klasse
TOCTitle: EsentDatabaseIncompleteUpgradeException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteUpgradeException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabaseincompleteupgradeexception(v=EXCHG.10)
ms:contentKeyID: 55101371
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteUpgradeException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteUpgradeException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8ae6272559c537ae870794a9d5a7a76bb8672b26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345131"
---
# <a name="esentdatabaseincompleteupgradeexception-class"></a>Esentdatabaseingecompleteupgradeexception-Klasse

Basisklasse für JET_err. Databaseingecompleteupgrade-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. esentexception](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. esenterrorexception](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. esentapiexception](./esentapiexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. esentstateexception](./esentstateexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. esentdatabasincompleteupgrade Exception  

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseIncompleteUpgradeException _
    Inherits EsentStateException
'Usage
Dim instance As EsentDatabaseIncompleteUpgradeException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseIncompleteUpgradeException : EsentStateException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Esentdatabaseingecompleteupgrade Exception-Member](./esentdatabaseincompleteupgradeexception-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
