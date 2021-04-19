---
description: 'Weitere Informationen über: vistaapi. JetInit3-Methode'
title: Vistaapi. JetInit3-Methode (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'JetInit3 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetInit3(Microsoft.Isam.Esent.Interop.JET_INSTANCE@,Microsoft.Isam.Esent.Interop.JET_RSTINFO,Microsoft.Isam.Esent.Interop.InitGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetinit3(v=EXCHG.10)
ms:contentKeyID: 55104198
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetInit3
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetInit3
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7c5fa7d1450240a8250e66e2bbe6d8ef0b97c136
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372860"
---
# <a name="vistaapijetinit3-method"></a>Vistaapi. JetInit3-Methode

Initialisieren Sie die ESENT-Datenbank-Engine.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Function JetInit3 ( _
    ByRef instance As JET_INSTANCE, _
    recoveryOptions As JET_RSTINFO, _
    grbit As InitGrbit _
) As JET_wrn
'Usage
Dim instance As JET_INSTANCE
Dim recoveryOptions As JET_RSTINFO
Dim grbit As InitGrbit
Dim returnValue As JET_wrn

returnValue = VistaApi.JetInit3(instance, _
    recoveryOptions, grbit)
```

``` csharp
public static JET_wrn JetInit3(
    ref JET_INSTANCE instance,
    JET_RSTINFO recoveryOptions,
    InitGrbit grbit
)
```

#### <a name="parameters"></a>Parameter

  - instance  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Die-Instanz, die initialisiert werden soll. Wenn eine Instanz nicht zugeordnet wurde, wird ein neuer erstellt, und die Engine wird im einzelinstanzmodus betrieben.

<!-- end list -->

  - Wiederherstellungsoptionen  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_RSTINFO](./jet-rstinfo-class.md)  
    
    Zusätzliche Wiederherstellungs Parameter zum erneuten Zuordnen von Datenbanken während der Wiederherstellung, zur Position, an der die Wiederherstellung beendet werden soll, oder zur

<!-- end list -->

  - grbit  
    Type: [Microsoft.Isam.Esent.Interop.Initgrbit](./initgrbit-enumeration.md)  
    
    Initialisierungs Optionen.

#### <a name="return-value"></a>Rückgabewert

Typ: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Ein Warnungs Code.  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Vistaapi-Klasse](./vistaapi-class.md)

[Vistaapi-Member](./vistaapi-members.md)

[Microsoft. ISAM. ESENT. Interop. Vista-Namespace](./microsoft.isam.esent.interop.vista-namespace.md)
