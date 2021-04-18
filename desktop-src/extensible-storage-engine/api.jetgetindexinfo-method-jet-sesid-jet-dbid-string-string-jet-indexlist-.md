---
description: 'Weitere Informationen finden Sie unter: API. jetgetindexinfo-Methode (JET_SESID, JET_DBID, Zeichenfolge, Zeichenfolge, JET_INDEXLIST)'
title: API. jetgetindexinfo-Methode (JET_SESID, JET_DBID, String, String, JET_INDEXLIST)
TOCTitle: JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, JET_INDEXLIST)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_INDEXLIST@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100770
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2320b72a90ff97326c027b00cfeb5bf38453f68c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340173"
---
# <a name="apijetgetindexinfo-method-jet_sesid-jet_dbid-string-string-jet_indexlist"></a>API. jetgetindexinfo-Methode (JET_SESID, JET_DBID, String, String, JET_INDEXLIST)

**Hinweis: Diese API ist mittlerweile veraltet.**

Ruft Informationen zu Indizes in einer Tabelle ab.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<ObsoleteAttribute("Use the overload that takes a JET_IdxInfo parameter, passing in JET_IdxInfo.List")> _
Public Shared Sub JetGetIndexInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    ignored As String, _
    <OutAttribute> ByRef indexlist As JET_INDEXLIST _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim ignored As String
Dim indexlist As JET_INDEXLISTApi.JetGetIndexInfo(sesid, dbid, _
    tablename, ignored, indexlist)
```

``` csharp
[ObsoleteAttribute("Use the overload that takes a JET_IdxInfo parameter, passing in JET_IdxInfo.List")]
public static void JetGetIndexInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string ignored,
    out JET_INDEXLIST indexlist
)
```

#### <a name="parameters"></a>Parameter

  - -sid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - dbid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    Die zu verwendende Datenbank.

<!-- end list -->

  - Tabellenname  
    Typ: [System. String](/dotnet/api/system.string)  
    
    Der Name der Tabelle, zu der Indexinformationen abgerufen werden sollen.

<!-- end list -->

  - wird ignoriert.  
    Typ: [System. String](/dotnet/api/system.string)  
    
    Konvertiert die Zeichenfolgendarstellung einer Zahl in einem angegebenen Stil und einem kulturspezifischen Format in die entsprechende 32-Bit-Ganzzahl mit Vorzeichen.

<!-- end list -->

  - indexlist  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_INDEXLIST](./jet-indexlist-class.md)  
    
    Wird mit Informationen zu Indizes für die Tabelle ausgefüllt.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[API-Klasse](./api-class.md)

[API-Mitglieder](./api-members.md)

[Jetgetindexinfo-Überladung](./api.jetgetindexinfo-method.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
