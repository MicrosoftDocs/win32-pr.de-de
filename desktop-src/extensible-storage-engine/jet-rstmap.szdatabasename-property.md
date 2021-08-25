---
description: 'Erfahren Sie mehr über: JET_RSTMAP.szDatabaseName-Eigenschaft'
title: JET_RSTMAP.szDatabaseName-Eigenschaft
TOCTitle: 'szDatabaseName property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RSTMAP.szDatabaseName
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_rstmap.szdatabasename(v=EXCHG.10)
ms:contentKeyID: 55103894
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RSTMAP.szDatabaseName
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RSTMAP.get_szDatabaseName
- Microsoft.Isam.Esent.Interop.JET_RSTMAP.set_szDatabaseName
- Microsoft.Isam.Esent.Interop.JET_RSTMAP.szDatabaseName
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7a66be5a854abee395a910596686dbc0a7f16b588fe4567e574da3efcae38d53
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850050"
---
# <a name="jet_rstmapszdatabasename-property"></a>JET_RSTMAP.szDatabaseName-Eigenschaft

Ruft den alten Namen/Pfad der Datenbank ab oder legt sie fest. Kann NULL sein, wenn er unverändert ist.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property szDatabaseName As String
    Get
    Set
'Usage
Dim instance As JET_RSTMAP
Dim value As String

value = instance.szDatabaseName

instance.szDatabaseName = value
```

``` csharp
public string szDatabaseName { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System.String](/dotnet/api/system.string)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[JET_RSTMAP-Klasse](./jet-rstmap-class.md)

[JET_RSTMAP-Member](./jet-rstmap-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
