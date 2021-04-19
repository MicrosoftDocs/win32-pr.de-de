---
description: Weitere Informationen finden Sie in der Eigenschaft "instanceparameters. maxtemporarytables".
title: Instanceparameters. maxtemporarytables (Eigenschaft)
TOCTitle: 'MaxTemporaryTables property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.MaxTemporaryTables
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.maxtemporarytables(v=EXCHG.10)
ms:contentKeyID: 55103560
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxTemporaryTables
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_MaxTemporaryTables
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxTemporaryTables
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_MaxTemporaryTables
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e5802e512a4ea6a4916ae54c24357dbdad057540
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368885"
---
# <a name="instanceparametersmaxtemporarytables-property"></a>Instanceparameters. maxtemporarytables (Eigenschaft)

Ruft die Anzahl der temporären Tabellen Ressourcen für die Verwendung durch eine-Instanz ab oder legt diese fest. Diese Einstellung wirkt sich darauf aus, wie viele temporäre Tabellen gleichzeitig verwendet werden können. Wenn dieser Systemparameter auf 0 (null) festgelegt ist, wird keine temporäre Datenbank erstellt, und jede Aktivität, die die temporäre Datenbank benötigt, schlägt fehl. Diese Einstellung kann hilfreich sein, um die e/a-Vorgänge zu vermeiden, die zum Erstellen der temporären Datenbank erforderlich sind, wenn bekannt ist, dass Sie nicht verwendet wird.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property MaxTemporaryTables As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.MaxTemporaryTables

instance.MaxTemporaryTables = value
```

``` csharp
public int MaxTemporaryTables { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System. Int32](/dotnet/api/system.int32)  

## <a name="remarks"></a>Bemerkungen

Die Verwendung einer temporären Tabelle erfordert auch eine Cursor Ressource.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Instanceparameters-Klasse](./instanceparameters-class.md)

[Instanceparameters-Elemente](./instanceparameters-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
