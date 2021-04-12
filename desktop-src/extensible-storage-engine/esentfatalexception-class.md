---
description: 'Weitere Informationen finden Sie unter: esentfatalexception-Klasse'
title: EsentFatalException-Klasse
TOCTitle: EsentFatalException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFatalException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfatalexception(v=EXCHG.10)
ms:contentKeyID: 55101653
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFatalException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFatalException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c38df447f2eb816772713ba930204e75aa38a88c
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104218938"
---
# <a name="esentfatalexception-class"></a>EsentFatalException-Klasse

Basisklasse für schwerwiegende Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. esentexception](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. esenterrorexception](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. esentoperationexception](./esentoperationexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. esentfatalexception  
            

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentFatalException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentFatalException
```

``` csharp
[SerializableAttribute]
public abstract class EsentFatalException : EsentOperationException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Esentfatalexception-Member](./esentfatalexception-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Abgeleitete Typen

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. esentexception](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. esenterrorexception](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. esentoperationexception](./esentoperationexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. esentfatalexception  
            [Microsoft. ISAM. ESENT. Interop. esentinstanceunavailableduetofatemangdiskfullexception](./esentinstanceunavailableduetofatallogdiskfullexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentinstanceunavailableexception](./esentinstanceunavailableexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentlogdisabledduetorecoveryfailureexception](./esentlogdisabledduetorecoveryfailureexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentrollbackerrorexception](./esentrollbackerrorexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentsector sizenotsupportedexception](./esentsectorsizenotsupportedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. esentunloadableosfunctionalityexception](./esentunloadableosfunctionalityexception-class.md)