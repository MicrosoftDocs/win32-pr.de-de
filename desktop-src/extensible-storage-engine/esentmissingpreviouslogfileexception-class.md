---
description: 'Weitere Informationen finden Sie unter: esentmissingpreviouslogfileexception-Klasse'
title: Esentmissingpreviouslogfileexception-Klasse
TOCTitle: EsentMissingPreviousLogFileException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMissingPreviousLogFileException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmissingpreviouslogfileexception(v=EXCHG.10)
ms:contentKeyID: 55102244
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMissingPreviousLogFileException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMissingPreviousLogFileException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5db6203093a85dabc317876d4c3d1544356b31b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347823"
---
# <a name="esentmissingpreviouslogfileexception-class"></a>Esentmissingpreviouslogfileexception-Klasse

Basisklasse für JET_err. Missingpreviouslogfile-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. esentexception](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. esenterrorexception](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. esentdataexception](./esentdataexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. esentverdertionexception](./esentcorruptionexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. esentmissingpreviouslogfileexception  

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMissingPreviousLogFileException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentMissingPreviousLogFileException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMissingPreviousLogFileException : EsentCorruptionException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Esentmissingpreviouslogfileexception-Member](./esentmissingpreviouslogfileexception-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
