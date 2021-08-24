---
description: 'Weitere Informationen finden Sie unter: Windows8Api.JetCreateTableColumnIndex4-Methode'
title: Windows8Api.JetCreateTableColumnIndex4-Methode (Microsoft.Isam.Esent.Interop.Windows8)
TOCTitle: 'JetCreateTableColumnIndex4 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCreateTableColumnIndex4(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,Microsoft.Isam.Esent.Interop.JET_TABLECREATE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetcreatetablecolumnindex4(v=EXCHG.10)
ms:contentKeyID: 55107827
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCreateTableColumnIndex4
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCreateTableColumnIndex4
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c13b269318d62d4c264bc5b8d9503a4d011c2727b79030f64bb5a6545ba0df70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038528"
---
# <a name="windows8apijetcreatetablecolumnindex4-method"></a>Windows8Api.JetCreateTableColumnIndex4-Methode

Erstellt eine Tabelle, fügt Spalten und Indizes für diese Tabelle hinzu. [JetCreateTableColumnIndex3(JET_SESID, JET_DBID, JET_TABLECREATE)](./api.jetcreatetablecolumnindex3-method.md)

**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetCreateTableColumnIndex4 ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablecreate As JET_TABLECREATE _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablecreate As JET_TABLECREATEWindows8Api.JetCreateTableColumnIndex4(sesid, _
    dbid, tablecreate)
```

``` csharp
public static void JetCreateTableColumnIndex4(
    JET_SESID sesid,
    JET_DBID dbid,
    JET_TABLECREATE tablecreate
)
```

#### <a name="parameters"></a>Parameter

  - sesid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - dbid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    Die Datenbank, der die neue Tabelle hinzugefügt werden soll.

<!-- end list -->

  - tablecreate  
    Typ: [Microsoft.Isam.Esent.Interop.JET_TABLECREATE](./jet-tablecreate-class.md)  
    
    Objekt, das die zu erstellende Tabelle beschreibt.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[Windows8Api-Klasse](./windows8api-class.md)

[Windows8Api-Member](./windows8api-members.md)

[Microsoft.Isam.Esent.Interop.Windows8-Namespace](./microsoft.isam.esent.interop.windows8-namespace.md)
