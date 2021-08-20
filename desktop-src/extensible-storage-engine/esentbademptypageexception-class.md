---
description: 'Weitere Informationen finden Sie unter: EsentBadEmptyPageException-Klasse'
title: EsentBadEmptyPageException-Klasse
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
ms.openlocfilehash: b06c76dcb807625e03712c8e5fd7d4f347dfc9b57f64310f3059134f6de7c2a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786130"
---
# <a name="esentbademptypageexception-class"></a>EsentBadEmptyPageException-Klasse

Basisklasse für JET_err. BadEmptyPage-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentCorruptionException](./esentcorruptionexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentBadEmptyPageException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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

#### <a name="reference"></a>Verweis

[EsentBadEmptyPageException-Member](./esentbademptypageexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
