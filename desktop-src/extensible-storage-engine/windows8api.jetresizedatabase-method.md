---
description: 'Weitere Informationen finden Sie unter: Windows8Api.JetResizeDatabase-Methode'
title: Windows8Api.JetResizeDatabase-Methode (Microsoft.Isam.Esent.Interop.Windows8)
TOCTitle: 'JetResizeDatabase method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetResizeDatabase(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetresizedatabase(v=EXCHG.10)
ms:contentKeyID: 55104462
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetResizeDatabase
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetResizeDatabase
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 02ffc2aed2a5bf9a24ef086d244ae0917830ee9e0f3280d39fa78b18d11a4b06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966810"
---
# <a name="windows8apijetresizedatabase-method"></a>Windows8Api.JetResizeDatabase-Methode

Ändern der Größe einer derzeit geöffneten Datenbank.

**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetResizeDatabase ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    desiredPages As Integer, _
    <OutAttribute> ByRef actualPages As Integer, _
    grbit As ResizeDatabaseGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim desiredPages As Integer
Dim actualPages As Integer
Dim grbit As ResizeDatabaseGrbitWindows8Api.JetResizeDatabase(sesid, dbid, _
    desiredPages, actualPages, grbit)
```

``` csharp
public static void JetResizeDatabase(
    JET_SESID sesid,
    JET_DBID dbid,
    int desiredPages,
    out int actualPages,
    ResizeDatabaseGrbit grbit
)
```

#### <a name="parameters"></a>Parameter

  - sesid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die zu verwendende Sitzung.

<!-- end list -->

  - dbid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    Die zu wächstde Datenbank.

<!-- end list -->

  - desiredPages  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Die gewünschte Größe der Datenbank in Seiten.

<!-- end list -->

  - actualPages  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Die Größe der Datenbank in Seiten nach dem Aufruf.

<!-- end list -->

  - grbit  
    Typ: [Microsoft.Isam.Esent.Interop.Windows8.ResizeDatabaseGrbit](./resizedatabasegrbit-enumeration.md)  
    
    Größenvergrößerungsoptionen.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[Windows8Api-Klasse](./windows8api-class.md)

[Windows8Api-Member](./windows8api-members.md)

[Microsoft.Isam.Esent.Interop.Windows8-Namespace](./microsoft.isam.esent.interop.windows8-namespace.md)
