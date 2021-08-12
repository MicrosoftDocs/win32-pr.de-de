---
description: 'Weitere Informationen finden Sie unter: Api.JetDefragment-Methode'
title: Api.JetDefragment-Methode
TOCTitle: 'JetDefragment method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDefragment(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.Int32@,System.Int32@,Microsoft.Isam.Esent.Interop.DefragGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdefragment(v=EXCHG.10)
ms:contentKeyID: 55100679
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9761782e2c6522752d6a05f69005a4db6844542c700cbc5c942ea80d96bf4c2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118272654"
---
# <a name="apijetdefragment-method"></a>Api.JetDefragment-Methode

Startet und beendet Datenbankdefragmentierungsaufgaben, die die Datenorganisation innerhalb einer Datenbank verbessern.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Function JetDefragment ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableName As String, _
    ByRef passes As Integer, _
    ByRef seconds As Integer, _
    grbit As DefragGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tableName As String
Dim passes As Integer
Dim seconds As Integer
Dim grbit As DefragGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetDefragment(sesid, _
    dbid, tableName, passes, seconds, _
    grbit)
```

``` csharp
public static JET_wrn JetDefragment(
    JET_SESID sesid,
    JET_DBID dbid,
    string tableName,
    ref int passes,
    ref int seconds,
    DefragGrbit grbit
)
```

#### <a name="parameters"></a>Parameter

  - sesid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die Sitzung, die für den Aufruf verwendet werden soll.

<!-- end list -->

  - dbid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    Die zu defragmentierte Datenbank.

<!-- end list -->

  - tableName  
    Typ: [System.String](/dotnet/api/system.string)  
    
    Nicht verwendeter Parameter. Die Defragmentierung wird für die gesamte Datenbank durchgeführt, die von der angegebenen Datenbank-ID beschrieben wird.

<!-- end list -->

  - Übergibt  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Beim Starten einer Onlinedefragmentierungsaufgabe legt dieser Parameter die maximale Anzahl von Defragmentierungsüberläufen fest. Beim Beenden einer Onlinedefragmentierungsaufgabe wird dieser Parameter auf die Anzahl der ausgeführten Durchläufe festgelegt.

<!-- end list -->

  - Sekunden  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Beim Starten einer Onlinedefragmentierungsaufgabe legt dieser Parameter die maximale Zeit für die Defragmentierung fest. Beim Beenden eines Onlinedefragmentierungs-Task wird dieser Ausgabepuffer auf die Dauer festgelegt, die für die Defragmentierung verwendet wird.

<!-- end list -->

  - grbit  
    Typ: [Microsoft.Isam.Esent.Interop.DefragGrbit](./defraggrbit-enumeration.md)  
    
    Defragmentierungsoptionen.

#### <a name="return-value"></a>Rückgabewert

Typ: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Ein Warnungscode.  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[API-Klasse](./api-class.md)

[API-Member](./api-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
