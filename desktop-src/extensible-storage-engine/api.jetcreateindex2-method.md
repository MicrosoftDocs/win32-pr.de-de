---
description: 'Weitere Informationen finden Sie unter: Api.JetCreateIndex2-Methode'
title: Api.JetCreateIndex2-Methode
TOCTitle: 'JetCreateIndex2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateIndex2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_INDEXCREATE[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreateindex2(v=EXCHG.10)
ms:contentKeyID: 55100673
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateIndex2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateIndex2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e58048098b137c4a0443cddc725c61622ee8bef94cf3752abf5b45a24d385734
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118272664"
---
# <a name="apijetcreateindex2-method"></a>Api.JetCreateIndex2-Methode

Erstellt Indizes für Daten in einer ESE-Datenbank.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetCreateIndex2 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexcreates As JET_INDEXCREATE(), _
    numIndexCreates As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexcreates As JET_INDEXCREATE()
Dim numIndexCreates As IntegerApi.JetCreateIndex2(sesid, tableid, _
    indexcreates, numIndexCreates)
```

``` csharp
public static void JetCreateIndex2(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_INDEXCREATE[] indexcreates,
    int numIndexCreates
)
```

#### <a name="parameters"></a>Parameter

  - sesid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - tableid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Die Tabelle, für die der Index erstellt werden soll.

<!-- end list -->

  - indexcreates  
    Typ: \[\]  
    
    Array von -Objekten, das die zu erstellenden Indizes beschreibt.

<!-- end list -->

  - numIndexCreates  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Anzahl der Indexbeschreibungsobjekte.

## <a name="remarks"></a>Hinweise

Beim Erstellen mehrerer Indizes (d. h. mit numIndexCreates größer als 1) MUSS diese Methode außerhalb von Transaktionen und mit exklusivem Zugriff auf die Tabelle aufgerufen werden. Die JET_TABLEID,die von "JetCreateTable" zurückgegeben wird, hat exklusiven Zugriff, oder die Tabelle kann für exklusiven Zugriff geöffnet werden, indem [DenyRead](./opentablegrbit-enumeration.md) an [JetOpenTable(JET_SESID, JET_DBID, String, \[ \] , Int32, OpenTableGrbit, JET_TABLEID) übergeben](./api.jetopentable-method.md)wird.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[API-Klasse](./api-class.md)

[API-Member](./api-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
