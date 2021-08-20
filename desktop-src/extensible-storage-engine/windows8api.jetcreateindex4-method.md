---
description: 'Weitere Informationen finden Sie unter: Windows8Api.JetCreateIndex4-Methode'
title: Windows8Api.JetCreateIndex4-Methode (Microsoft.Isam.Esent.Interop.Windows8)
TOCTitle: 'JetCreateIndex4 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCreateIndex4(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_INDEXCREATE[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetcreateindex4(v=EXCHG.10)
ms:contentKeyID: 55104455
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCreateIndex4
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCreateIndex4
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e69e9937167262d87fee788d38191d23d32b9bdcb83ce587aac3f286c2aee260
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117700857"
---
# <a name="windows8apijetcreateindex4-method"></a>Windows8Api.JetCreateIndex4-Methode

Erstellt Indizes für Daten in einer ESE-Datenbank.

**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetCreateIndex4 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexcreates As JET_INDEXCREATE(), _
    numIndexCreates As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexcreates As JET_INDEXCREATE()
Dim numIndexCreates As IntegerWindows8Api.JetCreateIndex4(sesid, tableid, _
    indexcreates, numIndexCreates)
```

``` csharp
public static void JetCreateIndex4(
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
    
    Array von -Objekten, die die zu erstellenden Indizes beschreiben.

<!-- end list -->

  - numIndexCreates  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Anzahl der Indexbeschreibungsobjekte.

## <a name="remarks"></a>Hinweise

Beim Erstellen mehrerer Indizes (d. h. mit numIndexCreates größer als 1) MUSS diese Methode außerhalb von Transaktionen und mit exklusivem Zugriff auf die Tabelle aufgerufen werden. Die von "Api.JetCreateTable" zurückgegebenen JET_TABLEID verfügen über einen exklusiven Zugriff, oder die Tabelle kann für exklusiven Zugriff geöffnet werden, indem [DenyRead](./opentablegrbit-enumeration.md) an [JetOpenTable(JET_SESID, JET_DBID, String, \[ \] , Int32, OpenTableGrbit, JET_TABLEID)](./api.jetopentable-method.md)übergeben wird.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[Windows8Api-Klasse](./windows8api-class.md)

[Windows8Api-Member](./windows8api-members.md)

[Microsoft.Isam.Esent.Interop.Windows8-Namespace](./microsoft.isam.esent.interop.windows8-namespace.md)
