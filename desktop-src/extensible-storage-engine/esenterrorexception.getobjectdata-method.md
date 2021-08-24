---
description: 'Weitere Informationen finden Sie unter: EsentErrorException.GetObjectData-Methode'
title: EsentErrorException.GetObjectData-Methode
TOCTitle: 'GetObjectData method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentErrorException.GetObjectData(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenterrorexception.getobjectdata(v=EXCHG.10)
ms:contentKeyID: 55101432
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentErrorException.GetObjectData
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentErrorException.GetObjectData
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7a4388d9af4f7cc6dbc284296b121fb3366e210c0d174a3db8e2b726f748f23a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784360"
---
# <a name="esenterrorexceptiongetobjectdata-method"></a>EsentErrorException.GetObjectData-Methode

Legt beim Überschreiben in einer abgeleiteten Klasse [serializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo) mit Informationen zur Ausnahme fest.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Overrides Sub GetObjectData ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim instance As EsentErrorException
Dim info As SerializationInfo
Dim context As StreamingContext

instance.GetObjectData(info, context)
```

``` csharp
public override void GetObjectData(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a>Parameter

  - info  
    Typ: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)  
    
    Die [SerializationInfo,](/dotnet/api/system.runtime.serialization.serializationinfo) die die serialisierten Objektdaten über die ausgelöste Ausnahme enthält.

<!-- end list -->

  - context  
    Typ: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)  
    
    Der [StreamingContext,](/dotnet/api/system.runtime.serialization.streamingcontext) der Kontextinformationen zur Quelle oder zum Ziel enthält.

#### <a name="implements"></a>Implementiert

[ISerializable.GetObjectData(SerializationInfo, StreamingContext)](/dotnet/api/system.runtime.serialization.iserializable.getobjectdata#System_Runtime_Serialization_ISerializable_GetObjectData_System_Runtime_Serialization_SerializationInfo_System_Runtime_Serialization_StreamingContext_)  
[_Exception.GetObjectData(SerializationInfo, StreamingContext)](/dotnet/api/system.runtime.interopservices._exception.getobjectdata#System_Runtime_InteropServices__Exception_GetObjectData_System_Runtime_Serialization_SerializationInfo_System_Runtime_Serialization_StreamingContext_)  

## <a name="exceptions"></a>Ausnahmen

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Ausnahme</th>
<th>Bedingung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/dotnet/api/system.argumentnullexception">ArgumentNullException</a></td>
<td><p>Der Parameter info ist ein null-Verweis (Nothing in Visual Basic).</p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[EsentErrorException-Klasse](./esenterrorexception-class.md)

[EsentErrorException-Member](./esenterrorexception-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
