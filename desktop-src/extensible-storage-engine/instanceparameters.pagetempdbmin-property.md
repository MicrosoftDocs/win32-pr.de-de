---
description: 'Weitere Informationen zu: InstanceParameters.PageTempDBMin-Eigenschaft'
title: InstanceParameters.PageTempDBMin-Eigenschaft
TOCTitle: 'PageTempDBMin property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.PageTempDBMin
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.pagetempdbmin(v=EXCHG.10)
ms:contentKeyID: 55103558
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.PageTempDBMin
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_PageTempDBMin
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_PageTempDBMin
- Microsoft.Isam.Esent.Interop.InstanceParameters.PageTempDBMin
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8a2b8ceddaa6aa333c7d55f1fc68a525f2190ef36be6372df85c3c4fa4648960
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119618030"
---
# <a name="instanceparameterspagetempdbmin-property"></a>InstanceParameters.PageTempDBMin-Eigenschaft

Ruft die Anfangsgröße der temporären Datenbank ab oder legt diese fest. Die Größe wird auf Datenbankseiten angezeigt. Die Größe 0 (null) gibt an, dass die Standardgröße einer normalen Datenbank verwendet werden soll. Es ist häufig wünschenswert, dass kleine Anwendungen die temporäre Datenbank so klein wie möglich konfigurieren. Wenn Sie diesen Parameter auf [PageTempDBSmallest](./systemparameters.pagetempdbsmallest-field.md) festlegen, wird die kleinstmögliche temporäre Datenbank erreicht.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property PageTempDBMin As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.PageTempDBMin

instance.PageTempDBMin = value
```

``` csharp
public int PageTempDBMin { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[InstanceParameters-Klasse](./instanceparameters-class.md)

[InstanceParameters-Member](./instanceparameters-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
