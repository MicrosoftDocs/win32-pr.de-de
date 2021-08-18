---
description: 'Weitere Informationen finden Sie unter: VistaParam.CachedClosedTables-Feld'
title: VistaParam.CachedClosedTables-Feld (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: CachedClosedTables field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Vista.VistaParam.CachedClosedTables
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaparam.cachedclosedtables(v=EXCHG.10)
ms:contentKeyID: 55104337
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.CachedClosedTables
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.CachedClosedTables
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 444456bc49b1cf2358feb32cadb36bec85cef5585436639dcf38caa02308af34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038658"
---
# <a name="vistaparamcachedclosedtables-field"></a>VistaParam.CachedClosedTables-Feld

Dieser Parameter steuert die Anzahl der B+-Strukturressourcen, die von der -Instanz zwischengespeichert werden, nachdem die tabellen, die sie darstellen, von der Anwendung geschlossen wurden. Große Werte für diesen Parameter führen dazu, dass die Datenbank-Engine mehr Arbeitsspeicher verwendet, erhöht jedoch die Geschwindigkeit, mit der eine große Anzahl von Tabellen nach dem Zufallsprinzip von der Anwendung geöffnet werden kann. Dies ist nützlich für Anwendungen, die über ein Schema mit einer sehr großen Anzahl von Tabellen verfügen.

**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Const CachedClosedTables As JET_param
'Usage
Dim value As JET_param

value = VistaParam.CachedClosedTables
```

``` csharp
public const JET_param CachedClosedTables
```

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[VistaParam-Klasse](./vistaparam-class.md)

[VistaParam-Member](./vistaparam-members.md)

[Microsoft.Isam.Esent.Interop.Vista-Namespace](./microsoft.isam.esent.interop.vista-namespace.md)
