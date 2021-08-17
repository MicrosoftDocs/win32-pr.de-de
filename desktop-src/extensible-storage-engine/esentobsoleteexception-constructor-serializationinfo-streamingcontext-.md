---
description: 'Weitere Informationen zu: EsentObsoleteException-Konstruktor (SerializationInfo, StreamingContext)'
title: EsentObsoleteException-Konstruktor (SerializationInfo, StreamingContext)
TOCTitle: EsentObsoleteException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentObsoleteException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentobsoleteexception.esentobsoleteexception(v=EXCHG.10)
ms:contentKeyID: 55102167
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentObsoleteException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0b114078e25cd394caa294dac5604502a4a2f783945914a44423b1c8681c105a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119040108"
---
# <a name="esentobsoleteexception-constructor-serializationinfo-streamingcontext"></a>EsentObsoleteException-Konstruktor (SerializationInfo, StreamingContext)

Initialisiert eine neue Instanz der EsentObsoleteException-Klasse. Dieser Konstruktor wird verwendet, um eine serialisierte Ausnahme zu deserialisieren.

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

Dim instance As New EsentObsoleteException(info, context)
```

``` csharp
protected EsentObsoleteException(
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

[EsentObsoleteException-Klasse](./esentobsoleteexception-class.md)

[EsentObsoleteException-Member](./esentobsoleteexception-members.md)

[EsentObsoleteException-Überladung](./esentobsoleteexception-constructor.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
