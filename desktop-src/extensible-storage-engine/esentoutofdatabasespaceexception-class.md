---
description: 'Weitere Informationen finden Sie unter: esentouesfdatabasespaceexception-Klasse'
title: Esentouto fdatabasespaceexception-Klasse
TOCTitle: EsentOutOfDatabaseSpaceException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfDatabaseSpaceException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutofdatabasespaceexception(v=EXCHG.10)
ms:contentKeyID: 55102410
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfDatabaseSpaceException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfDatabaseSpaceException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ece3a81fa0687299edba0857b15f4c0abc50e403
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345897"
---
# <a name="esentoutofdatabasespaceexception-class"></a>Esentouto fdatabasespaceexception-Klasse

Basisklasse für JET_err. Ouesfdatabasespace-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. esentexception](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. esenterrorexception](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. esentoperationexception](./esentoperationexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. esentresourceexception](./esentresourceexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentquotaexception](./esentquotaexception-class.md)  
              Microsoft. ISAM. ESENT. Interop. esentouesfdatabasespaceexception  

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfDatabaseSpaceException _
    Inherits EsentQuotaException
'Usage
Dim instance As EsentOutOfDatabaseSpaceException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfDatabaseSpaceException : EsentQuotaException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Esentouto fdatabasespaceexception-Member](./esentoutofdatabasespaceexception-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
