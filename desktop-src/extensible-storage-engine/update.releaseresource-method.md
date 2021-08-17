---
description: Weitere Informationen finden Sie unter Update.ReleaseResource-Methode.
title: Update.ReleaseResource-Methode
TOCTitle: 'ReleaseResource method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.ReleaseResource
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.releaseresource(v=EXCHG.10)
ms:contentKeyID: 55104200
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Update.ReleaseResource
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Update.ReleaseResource
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3a188b60aeba16aab1d5e4a07c27b42ca57e2fc4eadde5b56333900102d383db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471430"
---
# <a name="updatereleaseresource-method"></a>Update.ReleaseResource-Methode

Wird aufgerufen, wenn die Transaktion verworfen wird, während sie aktiv ist. Dadurch sollte ein Rollback für die Transaktion ausgeführt werden.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Protected Overrides Sub ReleaseResource
'Usage

Me.ReleaseResource()
```

``` csharp
protected override void ReleaseResource()
```

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[Update-Klasse](./update-class.md)

[Aktualisieren von Mitgliedern](./update-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
