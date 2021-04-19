---
description: Weitere Informationen finden Sie in der API. jetkreateingedex-Methode.
title: API. jetkreateingedex-Methode
TOCTitle: 'JetCreateIndex method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateIndex(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.CreateIndexGrbit,System.String,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreateindex(v=EXCHG.10)
ms:contentKeyID: 55100693
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateIndex
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateIndex
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a9b3549461324f396408bb7d370531907248e8c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339768"
---
# <a name="apijetcreateindex-method"></a>API. jetkreateingedex-Methode

Erstellt einen Index über Daten in einer ESE-Datenbank. Ein Index kann verwendet werden, um bestimmte Daten schnell zu suchen.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetCreateIndex ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexName As String, _
    grbit As CreateIndexGrbit, _
    keyDescription As String, _
    keyDescriptionLength As Integer, _
    density As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexName As String
Dim grbit As CreateIndexGrbit
Dim keyDescription As String
Dim keyDescriptionLength As Integer
Dim density As IntegerApi.JetCreateIndex(sesid, tableid, _
    indexName, grbit, keyDescription, _
    keyDescriptionLength, density)
```

``` csharp
public static void JetCreateIndex(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string indexName,
    CreateIndexGrbit grbit,
    string keyDescription,
    int keyDescriptionLength,
    int density
)
```

#### <a name="parameters"></a>Parameter

  - -sid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - TableID  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Die Tabelle, für die der Index erstellt werden soll.

<!-- end list -->

  - indexName  
    Typ: [System. String](/dotnet/api/system.string)  
    
    Ein Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen des zu erstellenden Indexes angibt.

<!-- end list -->

  - grbit  
    Typ: [Microsoft. ISAM. ESENT. Interop. kreateindexgrbit](./createindexgrbit-enumeration.md)  
    
    Index Erstellungs Optionen.

<!-- end list -->

  - keydescription  
    Typ: [System. String](/dotnet/api/system.string)  
    
    Zeiger auf eine Double-NULL-terminierte Zeichenfolge von NULL-getrennten Token.

<!-- end list -->

  - keydescriptionlength  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Die Länge von szkey (in Zeichen), einschließlich der beiden abschließenden Nullen.

<!-- end list -->

  - Dichte (density)  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Anfängliche B +-Struktur Dichte.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[API-Klasse](./api-class.md)

[API-Mitglieder](./api-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
