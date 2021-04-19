---
description: Weitere Informationen finden Sie in der API. JetDefragment2-Methode.
title: API. JetDefragment2-Methode
TOCTitle: 'JetDefragment2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDefragment2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.Int32@,System.Int32@,Microsoft.Isam.Esent.Interop.JET_CALLBACK,Microsoft.Isam.Esent.Interop.DefragGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdefragment2(v=EXCHG.10)
ms:contentKeyID: 55100696
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b22c89b304103954a2088bf05ba98797777489be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346501"
---
# <a name="apijetdefragment2-method"></a>API. JetDefragment2-Methode

Startet und beendet datenbankdefragmentierungsaufgaben, die die Datenorganisation innerhalb einer Datenbank verbessern.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Function JetDefragment2 ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableName As String, _
    ByRef passes As Integer, _
    ByRef seconds As Integer, _
    callback As JET_CALLBACK, _
    grbit As DefragGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tableName As String
Dim passes As Integer
Dim seconds As Integer
Dim callback As JET_CALLBACK
Dim grbit As DefragGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetDefragment2(sesid, _
    dbid, tableName, passes, seconds, _
    callback, grbit)
```

``` csharp
public static JET_wrn JetDefragment2(
    JET_SESID sesid,
    JET_DBID dbid,
    string tableName,
    ref int passes,
    ref int seconds,
    JET_CALLBACK callback,
    DefragGrbit grbit
)
```

#### <a name="parameters"></a>Parameter

  - -sid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die für den-Befehl zu verwendende Sitzung.

<!-- end list -->

  - dbid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    Die Datenbank, die deaktiviert werden soll.

<!-- end list -->

  - tableName  
    Typ: [System. String](/dotnet/api/system.string)  
    
    Nicht verwendeter Parameter. Die Defragmentierung wird für die gesamte Datenbank ausgeführt, die durch die angegebene Datenbank-ID beschrieben wird.

<!-- end list -->

  - ausweisen  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Wenn eine Online Defragmentierung gestartet wird, wird mit diesem Parameter die maximale Anzahl von defragmentierungsläufen festgelegt. Wenn Sie eine Online Defragmentierung beenden, wird dieser Parameter auf die Anzahl der durchgeführten Durchläufen festgelegt.

<!-- end list -->

  - Sekunden  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Wenn eine Online Defragmentierung gestartet wird, legt dieser Parameter die maximale Zeit für die Defragmentierung fest. Wenn Sie eine Online Defragmentierung beenden, wird dieser Ausgabepuffer auf die für die Defragmentierung verwendete Zeitspanne festgelegt.

<!-- end list -->

  - Rückruf  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_CALLBACK](./jet-callback-delegate.md)  
    
    Rückruffunktion, die defragmentiert, um den Fortschritt zu melden.

<!-- end list -->

  - grbit  
    Typ: [Microsoft. ISAM. ESENT. Interop. defraggrbit](./defraggrbit-enumeration.md)  
    
    Defragmentierungsoptionen.

#### <a name="return-value"></a>Rückgabewert

Typ: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Ein Warnungs Code.  

## <a name="remarks"></a>Bemerkungen

Der an JetDefragment2 über gegebene Rückruf kann asynchron ausgeführt werden. Der GC weiß nicht, dass der nicht verwaltete Code einen Verweis auf den Rückruf hat, daher ist es wichtig sicherzustellen, dass der Rückruf nicht erfasst wird.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[API-Klasse](./api-class.md)

[API-Mitglieder](./api-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
