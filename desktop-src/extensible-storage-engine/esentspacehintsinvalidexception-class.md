---
description: 'Weitere Informationen finden Sie unter: EsentSpaceHintsInvalidException-Klasse'
title: EsentSpaceHintsInvalidException-Klasse
TOCTitle: EsentSpaceHintsInvalidException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSpaceHintsInvalidException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentspacehintsinvalidexception(v=EXCHG.10)
ms:contentKeyID: 55102857
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSpaceHintsInvalidException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSpaceHintsInvalidException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 96f1b4b92dc00b4d2e3422f3fc9f03e949f77bb0674c5b710cb6fc4b4f7277cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118258959"
---
# <a name="esentspacehintsinvalidexception-class"></a>EsentSpaceHintsInvalidException-Klasse

Basisklasse für JET_err. SpaceHintsInvalid-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentUsageException](./esentusageexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentSpaceHintsInvalidException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSpaceHintsInvalidException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentSpaceHintsInvalidException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSpaceHintsInvalidException : EsentUsageException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[EsentSpaceHintsInvalidException-Member](./esentspacehintsinvalidexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
