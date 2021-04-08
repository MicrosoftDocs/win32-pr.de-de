---
description: 'Weitere Informationen finden Sie unter: esentusageexception-Konstruktor (SerializationInfo, StreamingContext)'
title: Esentusageexception-Konstruktor (SerializationInfo, StreamingContext)
TOCTitle: EsentUsageException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentUsageException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentusageexception.esentusageexception(v=EXCHG.10)
ms:contentKeyID: 55103026
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentUsageException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 46100a5f359616b18e5eae0d7b9d9a04b0c2fc25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760585"
---
# <a name="esentusageexception-constructor-serializationinfo-streamingcontext"></a>Esentusageexception-Konstruktor (SerializationInfo, StreamingContext)

Initialisiert eine neue Instanz der esentusageexception-Klasse. Dieser Konstruktor wird verwendet, um eine serialisierte Ausnahme zu deserialisieren.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

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

Dim instance As New EsentUsageException(info, context)
```

``` csharp
protected EsentUsageException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a>Parameter

  - info  
    Typ: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)  
    
    Die Daten, die zum Deserialisieren des-Objekts benötigt werden.

<!-- end list -->

  - context  
    Typ: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)  
    
    Der Deserialisierungskontext.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[EsentUsageException-Klasse](./esentusageexception-class.md)

[Esentusageexception-Member](./esentusageexception-members.md)

[Esentusageexception-Überladung](./esentusageexception-constructor.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
