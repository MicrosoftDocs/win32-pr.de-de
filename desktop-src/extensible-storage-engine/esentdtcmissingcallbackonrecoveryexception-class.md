---
description: 'Weitere Informationen finden Sie unter: EsentDTCMissingCallbackOnRecoveryException-Klasse'
title: EsentDTCMissingCallbackOnRecoveryException-Klasse
TOCTitle: EsentDTCMissingCallbackOnRecoveryException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDTCMissingCallbackOnRecoveryException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdtcmissingcallbackonrecoveryexception(v=EXCHG.10)
ms:contentKeyID: 55101645
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDTCMissingCallbackOnRecoveryException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDTCMissingCallbackOnRecoveryException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d71baf2c5b82dd59bd06ffdc02b11a747111a6c88fb2c9e123c9e6e6b10d5059
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839503"
---
# <a name="esentdtcmissingcallbackonrecoveryexception-class"></a>EsentDTCMissingCallbackOnRecoveryException-Klasse

Basisklasse für JET_err. DTCMissingCallbackOnRecovery-Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft.Isam.Esent.EsentException](./esentexception-class.md)  
      [Microsoft.Isam.Esent.Interop.EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft.Isam.Esent.Interop.EsentApiException](./esentapiexception-class.md)  
          [Microsoft.Isam.Esent.Interop.EsentObsoleteException](./esentobsoleteexception-class.md)  
            Microsoft.Isam.Esent.Interop.EsentDTCMissingCallbackOnRecoveryException  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDTCMissingCallbackOnRecoveryException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentDTCMissingCallbackOnRecoveryException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDTCMissingCallbackOnRecoveryException : EsentObsoleteException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[EsentDTCMissingCallbackOnRecoveryException-Member](./esentdtcmissingcallbackonrecoveryexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
