---
description: Weitere Informationen finden Sie unter Api.GetColumnDictionary-Methode.
title: Api.GetColumnDictionary-Methode
TOCTitle: 'GetColumnDictionary method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetColumnDictionary(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.getcolumndictionary(v=EXCHG.10)
ms:contentKeyID: 55100653
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.GetColumnDictionary
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetColumnDictionary
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 901b905ccdaccb19bc8a6b5ca1bbf88b7831dc98d97a00f1b81f6ddb3c2b146a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117719660"
---
# <a name="apigetcolumndictionary-method"></a>Api.GetColumnDictionary-Methode

Erstellt ein Wörterbuch, das Spaltennamen ihren Spalten-IDs zulädt.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Function GetColumnDictionary ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As IDictionary(Of String, JET_COLUMNID)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As IDictionary(Of String, JET_COLUMNID)

returnValue = Api.GetColumnDictionary(sesid, _
    tableid)
```

``` csharp
public static IDictionary<string, JET_COLUMNID> GetColumnDictionary(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a>Parameter

  - sesid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende sesid.

<!-- end list -->

  - tableid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Die Tabelle, für die die Informationen abgerufen werden.

#### <a name="return-value"></a>Rückgabewert

Typ: [System.Collections.Generic.IDictionary](/dotnet/api/system.collections.generic.idictionary-2)\<[String](/dotnet/api/system.string), [JET_COLUMNID](./jet-columnid-structure.md)\>  
Eine Wörterbuchzuordnung von Spaltennamen zu Spalten-IDs.  

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[API-Klasse](./api-class.md)

[API-Member](./api-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
