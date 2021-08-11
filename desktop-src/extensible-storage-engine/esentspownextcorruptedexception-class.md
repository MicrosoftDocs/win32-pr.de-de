---
description: 'Weitere Informationen finden Sie unter: EsentSPOwnExtCorruptedException-Klasse'
title: EsentSPOwnExtCorruptedException-Klasse
TOCTitle: EsentSPOwnExtCorruptedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSPOwnExtCorruptedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentspownextcorruptedexception(v=EXCHG.10)
ms:contentKeyID: 55102983
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSPOwnExtCorruptedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSPOwnExtCorruptedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ab0499d607e245ca896d59579a5f280606c48768912b856d0220f35e71327a0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118258454"
---
# <a name="esentspownextcorruptedexception-class"></a>EsentSPOwnExtCorruptedException-Klasse

Basisklasse für JET_err. SPOwnExtCorrupted-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentDataException](./esentdataexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentCorruptionException](./esentcorruptionexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentSPOwnExtCorruptedException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSPOwnExtCorruptedException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentSPOwnExtCorruptedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSPOwnExtCorruptedException : EsentCorruptionException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[EsentSPOwnExtCorruptedException-Member](./esentspownextcorruptedexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
