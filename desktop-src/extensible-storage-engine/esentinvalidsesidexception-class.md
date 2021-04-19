---
description: 'Weitere Informationen finden Sie unter: esentinvalidabsidexception-Klasse'
title: Esentinvalid* sidexception-Klasse
TOCTitle: EsentInvalidSesidException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidSesidException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidsesidexception(v=EXCHG.10)
ms:contentKeyID: 55102020
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidSesidException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidSesidException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 53d841343c78720efd0f867d4b7a8ce5262cd1ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353489"
---
# <a name="esentinvalidsesidexception-class"></a>Esentinvalid* sidexception-Klasse

Basisklasse für JET_err. Invalidgsid-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. esentexception](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. esenterrorexception](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. esentapiexception](./esentapiexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. esentusageexception](./esentusageexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. esentinvalidsesidexception  

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidSesidException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentInvalidSesidException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidSesidException : EsentUsageException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Esentinvalid-sidexception-Elemente](./esentinvalidsesidexception-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
