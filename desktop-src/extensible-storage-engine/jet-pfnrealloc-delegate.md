---
description: 'Weitere Informationen finden Sie hier: JET_PFNREALLOC-Delegaten'
title: JET_PFNREALLOC Delegat
TOCTitle: JET_PFNREALLOC delegate
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_PFNREALLOC
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_pfnrealloc(v=EXCHG.10)
ms:contentKeyID: 39515764
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC..ctor
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC.BeginInvoke
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC.EndInvoke
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC.Invoke
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7aab9fef2d7a449c877f88d2ed77aa19cbb2409d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960865"
---
# <a name="jet_pfnrealloc-delegate"></a>JET_PFNREALLOC Delegat

Rückruf, der von jetenreeratecolrens verwendet wird, um Speicher für die Ausgabepuffer zuzuweisen.

Diese API ist nicht CLS-kompatibel. 

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Delegate Function JET_PFNREALLOC ( _
    context As IntPtr, _
    memory As IntPtr, _
    requestedSize As UInteger _
) As IntPtr
'Usage
Dim instance As New JET_PFNREALLOC(AddressOf HandlerMethod)
```

``` csharp
[CLSCompliantAttribute(false)]
public delegate IntPtr JET_PFNREALLOC(
    IntPtr context,
    IntPtr memory,
    uint requestedSize
)
```

#### <a name="parameters"></a>Parameter

  - context  
    Typ: [System. IntPtr](/dotnet/api/system.intptr)  
    
    Der für jetenreeratecolumschlag angegebene Kontext.

<!-- end list -->

  - Arbeitsspeicher  
    Typ: [System. IntPtr](/dotnet/api/system.intptr)  
    
    Wenn ungleich 0 (null), ein Zeiger auf einen Speicherblock, der zuvor von diesem Rückruf zugeordnet wurde.

<!-- end list -->

  - requestedSize  
    Typ: [System. UInt32](/dotnet/api/system.uint32)  
    
    Die neue Größe des Speicherblocks (in Bytes). Wenn dieser Wert 0 ist und ein Speicherblock angegeben wird, wird dieser Speicherblock freigegeben.

#### <a name="return-value"></a>Rückgabewert

Typ: [System. IntPtr](/dotnet/api/system.intptr)  
Ein Zeiger auf den neu belegten Arbeitsspeicher. Wenn kein Arbeitsspeicher zugeordnet werden konnte, sollte [0](/dotnet/api/system.intptr.zero) zurückgegeben werden.  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
