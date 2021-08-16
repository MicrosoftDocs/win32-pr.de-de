---
description: 'Weitere Informationen zu: Feld "Server2003Param.AlternateDatabaseRecoveryPath"'
title: Feld "Server2003Param.AlternateDatabaseRecoveryPath" (Microsoft.Isam.Esent.Interop.Server2003)
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
ms.openlocfilehash: 4a85673979a3b65d8c78ca06fae4496c11f8d2b31c810d411142e6c40bfd62cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119107243"
---
# <a name="server2003paramalternatedatabaserecoverypath-field"></a>Feld "Server2003Param.AlternateDatabaseRecoveryPath"

Der vollständige Pfad zu jeder Datenbank wird zur Laufzeit in den Transaktionsprotokollen beibehalten. Normalerweise müssen diese Datenbanken am ursprünglichen Speicherort verbleiben, damit die Transaktionswiedergabe ordnungsgemäß funktioniert. Dieser Parameter kann verwendet werden, um die Wiederherstellung nach einem Absturz oder einen Wiederherstellungsvorgang zu erzwingen, um nach den Datenbanken zu suchen, auf die im Transaktionsprotokoll im angegebenen Ordner verwiesen wird.

**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[Server2003Param-Klasse](./server2003param-class.md)

[Server2003Param-Member](./server2003param-members.md)

[Microsoft.Isam.Esent.Interop.Server2003-Namespace](./microsoft.isam.esent.interop.server2003-namespace.md)
