---
description: 'Weitere Informationen zu: EsentDTCCallbackUnexpectedErrorException-Klasse'
title: EsentDTCCallbackUnexpectedErrorException-Klasse
TOCTitle: EsentDTCCallbackUnexpectedErrorException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDTCCallbackUnexpectedErrorException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdtccallbackunexpectederrorexception(v=EXCHG.10)
ms:contentKeyID: 55107266
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDTCCallbackUnexpectedErrorException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDTCCallbackUnexpectedErrorException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 68ca839427d5f8ae15725bd1ae80b34c82918907f5f23a8a1e3ddf27d8453504
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117711180"
---
# <a name="esentdtccallbackunexpectederrorexception-class"></a>EsentDTCCallbackUnexpectedErrorException-Klasse

Basisklasse für JET_err. DTCCallbackUnexpectedError-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentObsoleteException](./esentobsoleteexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentDTCCallbackUnexpectedErrorException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDTCCallbackUnexpectedErrorException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentDTCCallbackUnexpectedErrorException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDTCCallbackUnexpectedErrorException : EsentObsoleteException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[EsentDTCCallbackUnexpectedErrorException-Member](./esentdtccallbackunexpectederrorexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
