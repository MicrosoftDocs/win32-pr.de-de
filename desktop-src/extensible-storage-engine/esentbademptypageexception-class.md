---
description: 'Weitere Informationen finden Sie unter: esentbademptypageexception-Klasse'
title: Esentbademptypageexception-Klasse
TOCTitle: EsentBadEmptyPageException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentBadEmptyPageException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentbademptypageexception(v=EXCHG.10)
ms:contentKeyID: 55101115
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentBadEmptyPageException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentBadEmptyPageException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 144f42c42eaf3ccb804344214d396cd8ac2f8aa3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217275"
---
# <a name="esentbademptypageexception-class"></a>Esentbademptypageexception-Klasse

Basisklasse für JET_err. "Bademptypage"-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. esentexception](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. esenterrorexception](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. esentdataexception](./esentdataexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. esentverdertionexception](./esentcorruptionexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. esentbademptypageexception  

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentBadEmptyPageException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentBadEmptyPageException
```

``` csharp
[SerializableAttribute]
public sealed class EsentBadEmptyPageException : EsentCorruptionException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Esentbademptypageexception-Member](./esentbademptypageexception-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
