---
description: 'Weitere Informationen finden Sie unter: EsentMemoryException-Konstruktor (SerializationInfo, StreamingContext)'
title: EsentMemoryException-Konstruktor (SerializationInfo, StreamingContext)
TOCTitle: EsentMemoryException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentMemoryException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmemoryexception.esentmemoryexception(v=EXCHG.10)
ms:contentKeyID: 55102121
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentMemoryException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 51ac6b24c2b50e33f7b805705de193140c9b0657ad07390cf534d47bb143aef8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119115601"
---
# <a name="esentmemoryexception-constructor-serializationinfo-streamingcontext"></a>EsentMemoryException-Konstruktor (SerializationInfo, StreamingContext)

Initialisiert eine neue Instanz der EsentMemoryException-Klasse. Dieser Konstruktor wird verwendet, um eine serialisierte Ausnahme zu deserialisieren.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentMemoryException(info, context)
```

``` csharp
protected EsentMemoryException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a>Parameter

  - info  
    Typ: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)  
    
    Die Daten, die zum Deserialisieren des Objekts erforderlich sind.

<!-- end list -->

  - context  
    Typ: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)  
    
    Der Deserialisierungskontext.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[EsentMemoryException-Klasse](./esentmemoryexception-class.md)

[EsentMemoryException-Member](./esentmemoryexception-members.md)

[EsentMemoryException-Überladung](./esentmemoryexception-constructor.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
