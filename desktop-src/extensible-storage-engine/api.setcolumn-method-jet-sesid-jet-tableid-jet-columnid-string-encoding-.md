---
description: 'Weitere Informationen finden Sie unter: Api.SetColumn-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, Zeichenfolge, Codierung)'
title: Api.SetColumn-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, String, Encoding)
TOCTitle: SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, String, Encoding)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.String,System.Text.Encoding)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumn(v=EXCHG.10)
ms:contentKeyID: 55100935
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.SetColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dfa67d3aba1ee79226bad4a52a688e60e0532f720d338c6efc20e3c95b05e6ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118084409"
---
# <a name="apisetcolumn-method-jet_sesid-jet_tableid-jet_columnid-string-encoding"></a>Api.SetColumn-Methode (JET_SESID, JET_TABLEID, JET_COLUMNID, String, Encoding)

Ändert einen einzelnen Spaltenwert in einem geänderten Datensatz, der eingefügt oder aktualisiert werden soll.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub SetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As String, _
    encoding As Encoding _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As String
Dim encoding As EncodingApi.SetColumn(sesid, tableid, columnid, _
    data, encoding)
```

``` csharp
public static void SetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    string data,
    Encoding encoding
)
```

#### <a name="parameters"></a>Parameter

  - sesid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - tableid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Der zu aktualisierende Cursor. Ein Update sollte vorbereitet werden.

<!-- end list -->

  - columnid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    Die columnid, die festgelegt werden soll.

<!-- end list -->

  - data  
    Typ: [System.String](/dotnet/api/system.string)  
    
    Die festzulegenden Daten.

<!-- end list -->

  - encoding  
    Typ: [System.Text.Encoding](/dotnet/api/system.text.encoding)  
    
    Die Codierung, die zum Konvertieren der Zeichenfolge verwendet wird.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[API-Klasse](./api-class.md)

[API-Member](./api-members.md)

[SetColumn-Überladung](./api.setcolumn-method.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
