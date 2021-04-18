---
description: 'Weitere Informationen finden Sie hier: vistaapi. jetgetthreadstats-Methode'
title: Vistaapi. jetgetthreadstats-Methode (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'JetGetThreadStats method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetThreadStats(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetgetthreadstats(v=EXCHG.10)
ms:contentKeyID: 55104192
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetThreadStats
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetThreadStats
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 92572fd538f0c6c2643e7b40a07ac168ae6980d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347882"
---
# <a name="vistaapijetgetthreadstats-method"></a>Vistaapi. jetgetthreadstats-Methode

Ruft Leistungsinformationen aus der Datenbank-Engine für den aktuellen Thread ab. Mehrere Aufrufe können verwendet werden, um Statistiken zu sammeln, die die Aktivität der Datenbank-Engine in diesem Thread zwischen diesen Aufrufen widerspiegeln.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetGetThreadStats ( _
    <OutAttribute> ByRef threadstats As JET_THREADSTATS _
)
'Usage
Dim threadstats As JET_THREADSTATSVistaApi.JetGetThreadStats(threadstats)
```

``` csharp
public static void JetGetThreadStats(
    out JET_THREADSTATS threadstats
)
```

#### <a name="parameters"></a>Parameter

  - threadstats  
    Typ: [Microsoft.ISAM.ESENT.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)  
    
    Gibt die Thread Statistikdaten zurück.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Vistaapi-Klasse](./vistaapi-class.md)

[Vistaapi-Member](./vistaapi-members.md)

[Microsoft. ISAM. ESENT. Interop. Vista-Namespace](./microsoft.isam.esent.interop.vista-namespace.md)
