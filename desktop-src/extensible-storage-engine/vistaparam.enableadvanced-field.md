---
description: 'Weitere Informationen finden Sie unter: VistaParam.EnableAdvanced-Feld'
title: VistaParam.EnableAdvanced-Feld (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: EnableAdvanced field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Vista.VistaParam.EnableAdvanced
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaparam.enableadvanced(v=EXCHG.10)
ms:contentKeyID: 55104335
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.EnableAdvanced
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.EnableAdvanced
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 70616409cd09652456734eecda67ca2a1ba3f999f997d87be27c5b0e8f87ff05
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119603520"
---
# <a name="vistaparamenableadvanced-field"></a>VistaParam.EnableAdvanced-Feld

Dieser Parameter wird verwendet, um zu steuern, wann die Datenbank-Engine Änderungen an einer Teilmenge der Systemparameter akzeptiert oder zurückgibt. Dieser Parameter wird in Verbindung mit [Configuration](./vistaparam.configuration-field.md) verwendet, um zu verhindern, dass einige Systemparameter von den Standardeinstellungen der ausgewählten Konfiguration entfernt werden.

**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Const EnableAdvanced As JET_param
'Usage
Dim value As JET_param

value = VistaParam.EnableAdvanced
```

``` csharp
public const JET_param EnableAdvanced
```

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[VistaParam-Klasse](./vistaparam-class.md)

[VistaParam-Member](./vistaparam-members.md)

[Microsoft.Isam.Esent.Interop.Vista-Namespace](./microsoft.isam.esent.interop.vista-namespace.md)
