---
description: 'Weitere Informationen finden Sie unter: esentoperationexception-Klasse'
title: EsentOperationException-Klasse
TOCTitle: EsentOperationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOperationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoperationexception(v=EXCHG.10)
ms:contentKeyID: 55102414
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOperationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOperationException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 314ae88a674f6bd59b0111d40ff3ca5a9eab8a2f
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106349756"
---
# <a name="esentoperationexception-class"></a>EsentOperationException-Klasse

Basisklasse für Vorgangs Ausnahmen.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. esentexception](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. esenterrorexception](./esenterrorexception-class.md)  
        Microsoft. ISAM. ESENT. Interop. esentoperationexception  
          

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentOperationException _
    Inherits EsentErrorException
'Usage
Dim instance As EsentOperationException
```

``` csharp
[SerializableAttribute]
public abstract class EsentOperationException : EsentErrorException
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Esentoperationexception-Member](./esentoperationexception-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Abgeleitete Typen

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. esentexception](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. esenterrorexception](./esenterrorexception-class.md)  
        Microsoft. ISAM. ESENT. Interop. esentoperationexception  
          [Microsoft. ISAM. ESENT. Interop. esentbackupabortbyserverexception](./esentbackupabortbyserverexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. esentcheckpointdepthopodeepexception](./esentcheckpointdepthtoodeepexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. esentclientrequesttostopjetserviceexception](./esentclientrequesttostopjetserviceexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. esentfatalexception](./esentfatalexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. esentinitinprogressexception](./esentinitinprogressexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. esentinternalerrorexception](./esentinternalerrorexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. esentioexception](./esentioexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. esentntsystemcallfailedexception](./esentntsystemcallfailedexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. esentossnapshottimeoutexception](./esentossnapshottimeoutexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. esentrecordnotdeletedexception](./esentrecordnotdeletedexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. esentresourceexception](./esentresourceexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. esentterminprogressexception](./esentterminprogressexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. esentunicodelta anguagevalidationfailureexception](./esentunicodelanguagevalidationfailureexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. esentunicodetranslationfailexception](./esentunicodetranslationfailexception-class.md)