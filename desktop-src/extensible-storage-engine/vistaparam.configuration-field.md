---
description: 'Weitere Informationen finden Sie hier: VistaParam.Configurationsfeld'
title: VistaParam.Configurationsfeld (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: Configuration field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Vista.VistaParam.Configuration
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaparam.configuration(v=EXCHG.10)
ms:contentKeyID: 55104229
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.Configuration
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.Configuration
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b330afb7158c616ba7bb9683a7bbe226d8d63542
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749696"
---
# <a name="vistaparamconfiguration-field"></a>VistaParam.Configurationsfeld

Dieser Parameter macht mehrere Sätze von Standardwerten für den gesamten Satz von Systemparametern verfügbar. Wenn dieser Parameter auf eine bestimmte Konfiguration festgelegt ist, werden alle Systemparameter Werte auf ihre Standardwerte für diese Konfiguration zurückgesetzt. Wenn die Konfiguration für eine bestimmte Instanz festgelegt ist, werden die globalen Systemparameter nicht auf ihre Standardwerte zurückgesetzt. Kleine Konfiguration (0): die Datenbank-Engine ist für die Speichernutzung optimiert. Legacy Konfiguration (1): die Datenbank-Engine verfügt über die herkömmlichen Standardeinstellungen.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Const Configuration As JET_param
'Usage
Dim value As JET_param

value = VistaParam.Configuration
```

``` csharp
public const JET_param Configuration
```

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Vistaparam-Klasse](./vistaparam-class.md)

[Vistaparam-Member](./vistaparam-members.md)

[Microsoft. ISAM. ESENT. Interop. Vista-Namespace](./microsoft.isam.esent.interop.vista-namespace.md)
