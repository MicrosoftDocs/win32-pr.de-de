---
description: 'Weitere Informationen finden Sie hier: Server2003Param. Alternative datasedatabaserecoverypath-Feld'
title: Server2003Param. alternativen datasedatabaserecoverypath-Feld (Microsoft. ISAM. ESENT. Interop. Server2003)
TOCTitle: AlternateDatabaseRecoveryPath field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Server2003.Server2003Param.AlternateDatabaseRecoveryPath
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003param.alternatedatabaserecoverypath(v=EXCHG.10)
ms:contentKeyID: 55104217
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Param.AlternateDatabaseRecoveryPath
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Param.AlternateDatabaseRecoveryPath
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 770ac27596b4385d0012cb65847754b4deb7e9fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343360"
---
# <a name="server2003paramalternatedatabaserecoverypath-field"></a>Server2003Param. Alternative datasedatabaserecoverypath-Feld

Der vollständige Pfad zu jeder Datenbank wird zur Laufzeit in den Transaktions Protokollen beibehalten. Normalerweise müssen diese Datenbanken am ursprünglichen Speicherort verbleiben, damit die Transaktions Wiedergabe ordnungsgemäß funktioniert. Dieser Parameter kann verwendet werden, um die Wiederherstellung von abstürzen oder einen Wiederherstellungs Vorgang zum Suchen nach den Datenbanken zu erzwingen, auf die im Transaktionsprotokoll im angegebenen Ordner verwiesen wird.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Const AlternateDatabaseRecoveryPath As JET_param
'Usage
Dim value As JET_param

value = Server2003Param.AlternateDatabaseRecoveryPath
```

``` csharp
public const JET_param AlternateDatabaseRecoveryPath
```

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Server2003Param-Klasse](./server2003param-class.md)

[Server2003Param-Member](./server2003param-members.md)

[Microsoft. ISAM. ESENT. Interop. Server2003-Namespace](./microsoft.isam.esent.interop.server2003-namespace.md)
