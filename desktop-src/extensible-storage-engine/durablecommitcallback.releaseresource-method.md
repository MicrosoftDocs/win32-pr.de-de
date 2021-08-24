---
description: 'Weitere Informationen zu: DurableCommitCallback.ReleaseResource-Methode'
title: DurableCommitCallback.ReleaseResource-Methode (Microsoft.Isam.Esent.Interop.Windows8)
TOCTitle: 'ReleaseResource method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.ReleaseResource
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.durablecommitcallback.releaseresource(v=EXCHG.10)
ms:contentKeyID: 55104293
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.ReleaseResource
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.ReleaseResource
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 758c27b1b3a67b91b7921276ec26e9c9776b65255c4cfa88d32b839f9950c2af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725270"
---
# <a name="durablecommitcallbackreleaseresource-method"></a>DurableCommitCallback.ReleaseResource-Methode

Gibt die permanente Commitsitzung frei.

**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
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

## <a name="remarks"></a>Hinweise

Versuchen Sie nicht, den Instanzparameter auf NULL festzulegen, da der Rückruf nach JetTerm verworfen wird und der Rückruf nicht nach JetTerm festgelegt werden kann.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[DurableCommitCallback-Klasse](./durablecommitcallback-class.md)

[DurableCommitCallback-Member](./durablecommitcallback-members.md)

[Microsoft.Isam.Esent.Interop.Windows8-Namespace](./microsoft.isam.esent.interop.windows8-namespace.md)
