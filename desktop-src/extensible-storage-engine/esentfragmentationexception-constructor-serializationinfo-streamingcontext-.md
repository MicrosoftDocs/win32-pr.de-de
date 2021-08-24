---
description: 'Weitere Informationen zu: EsentFragmentationException-Konstruktor (SerializationInfo, StreamingContext)'
title: EsentFragmentationException-Konstruktor (SerializationInfo, StreamingContext)
TOCTitle: EsentFragmentationException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentFragmentationException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfragmentationexception.esentfragmentationexception(v=EXCHG.10)
ms:contentKeyID: 55101633
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentFragmentationException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ae29411554d8a734fc250c3d8c8a04b381b2013c79dcb5c2c7aad22ff34963cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119838630"
---
# <a name="esentfragmentationexception-constructor-serializationinfo-streamingcontext"></a>EsentFragmentationException-Konstruktor (SerializationInfo, StreamingContext)

Initialisiert eine neue Instanz der EsentFragmentationException-Klasse. Dieser Konstruktor wird verwendet, um eine serialisierte Ausnahme zu deserialisieren.

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

Dim instance As New EsentFragmentationException(info, context)
```

``` csharp
protected EsentFragmentationException(
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

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[EsentFragmentationException-Klasse](./esentfragmentationexception-class.md)

[EsentFragmentationException-Member](./esentfragmentationexception-members.md)

[EsentFragmentationException-Überladung](./esentfragmentationexception-constructor.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
