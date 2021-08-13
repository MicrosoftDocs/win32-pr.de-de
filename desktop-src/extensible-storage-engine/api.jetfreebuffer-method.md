---
description: 'Weitere Informationen finden Sie unter: Api.JetFreeBuffer-Methode'
title: Api.JetFreeBuffer-Methode
TOCTitle: 'JetFreeBuffer method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetFreeBuffer(System.IntPtr)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetfreebuffer(v=EXCHG.10)
ms:contentKeyID: 55100694
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetFreeBuffer
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetFreeBuffer
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 902fb39a566c7c61f652d1a3796b20d550ce4bd2b61d706b955469af5762011d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118272484"
---
# <a name="apijetfreebuffer-method"></a>Api.JetFreeBuffer-Methode

Gibt Arbeitsspeicher frei, der durch einen Datenbank-Engine-Aufruf zugeordnet wurde.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetFreeBuffer ( _
    buffer As IntPtr _
)
'Usage
Dim buffer As IntPtrApi.JetFreeBuffer(buffer)
```

``` csharp
public static void JetFreeBuffer(
    IntPtr buffer
)
```

#### <a name="parameters"></a>Parameter

  - Puffer  
    Typ: [System.IntPtr](/dotnet/api/system.intptr)  
    
    Der Puffer, der durch einen Aufruf der Datenbank-Engine zugeordnet wird. [0](/dotnet/api/system.intptr.zero) ist akzeptabel und wird ignoriert.

## <a name="remarks"></a>Hinweise

Diese Methode ist intern, da wir niemals den von ESENT zugewiesenen Arbeitsspeicher für unsere Aufrufer verfügbar machen.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[API-Klasse](./api-class.md)

[API-Member](./api-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
