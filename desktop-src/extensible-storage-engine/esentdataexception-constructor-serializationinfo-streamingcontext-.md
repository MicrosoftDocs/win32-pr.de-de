---
description: 'Weitere Informationen finden Sie unter: esentdataexception-Konstruktor (SerializationInfo, StreamingContext)'
title: Esentdataexception-Konstruktor (SerializationInfo, StreamingContext)
TOCTitle: EsentDataException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentDataException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdataexception.esentdataexception(v=EXCHG.10)
ms:contentKeyID: 55101275
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentDataException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 43e7578adb10f607ff88062b48d3f2ebb73d34ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215282"
---
# <a name="esentdataexception-constructor-serializationinfo-streamingcontext"></a>Esentdataexception-Konstruktor (SerializationInfo, StreamingContext)

Initialisiert eine neue Instanz der esentdataexception-Klasse. Dieser Konstruktor wird verwendet, um eine serialisierte Ausnahme zu deserialisieren.

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

Dim instance As New EsentDataException(info, context)
```

``` csharp
protected EsentDataException(
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

[Esentdataexception-Klasse](./esentdataexception-class.md)

[Esentdataexception-Member](./esentdataexception-members.md)

[Esentdataexception-Überladung](./esentdataexception-constructor.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
