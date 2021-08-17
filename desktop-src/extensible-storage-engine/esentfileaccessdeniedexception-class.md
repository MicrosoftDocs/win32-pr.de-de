---
description: 'Weitere Informationen finden Sie unter: EsentFileAccessDeniedException-Klasse'
title: EsentFileAccessDeniedException-Klasse
TOCTitle: EsentFileAccessDeniedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFileAccessDeniedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfileaccessdeniedexception(v=EXCHG.10)
ms:contentKeyID: 55101658
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFileAccessDeniedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFileAccessDeniedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6e5a04f48103adf96116893a00c15715b9ab2e81ff1c0181463ba6317cb87461
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118778325"
---
# <a name="esentfileaccessdeniedexception-class"></a>EsentFileAccessDeniedException-Klasse

Basisklasse für JET_err. FileAccessDenied-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentOperationException](./esentoperationexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentIOException](./esentioexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentFileAccessDeniedException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentFileAccessDeniedException _
    Inherits EsentIOException
'Usage
Dim instance As EsentFileAccessDeniedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentFileAccessDeniedException : EsentIOException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[EsentFileAccessDeniedException-Member](./esentfileaccessdeniedexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
