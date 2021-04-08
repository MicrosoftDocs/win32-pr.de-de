---
description: Weitere Informationen finden Sie in der API. JetAttachDatabase2-Methode.
title: API. JetAttachDatabase2-Methode
TOCTitle: 'JetAttachDatabase2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase2(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.Int32,Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetattachdatabase2(v=EXCHG.10)
ms:contentKeyID: 55107224
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 33d91f0746b3ebf178bd61de58919ab99d85b1f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750769"
---
# <a name="apijetattachdatabase2-method"></a>API. JetAttachDatabase2-Methode

Fügt eine Datenbankdatei für die Verwendung mit einer Daten Bank Instanz an. Damit die Datenbank verwendet werden kann, muss Sie anschließend mit [jetopendatabase (JET_SESID, String, String, JET_DBID, opendatabasegrbit)](./api.jetopendatabase-method.md)geöffnet werden.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Function JetAttachDatabase2 ( _
    sesid As JET_SESID, _
    database As String, _
    maxPages As Integer, _
    grbit As AttachDatabaseGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim maxPages As Integer
Dim grbit As AttachDatabaseGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetAttachDatabase2(sesid, _
    database, maxPages, grbit)
```

``` csharp
public static JET_wrn JetAttachDatabase2(
    JET_SESID sesid,
    string database,
    int maxPages,
    AttachDatabaseGrbit grbit
)
```

#### <a name="parameters"></a>Parameter

  - -sid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - database  
    Typ: [System. String](/dotnet/api/system.string)  
    
    Die anzufügende Datenbank.

<!-- end list -->

  - maxpages  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Die maximale Größe der Datenbank auf Datenbankseiten. Das übergeben von 0 bedeutet, dass kein erzwungenes Maximum vorhanden ist.

<!-- end list -->

  - grbit  
    Typ: [Microsoft. ISAM. ESENT. Interop. attachdatabasegrbit](./attachdatabasegrbit-enumeration.md)  
    
    Optionen anfügen.

#### <a name="return-value"></a>Rückgabewert

Typ: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Ein ESENT-Warnungs Code.  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[API-Klasse](./api-class.md)

[API-Mitglieder](./api-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
