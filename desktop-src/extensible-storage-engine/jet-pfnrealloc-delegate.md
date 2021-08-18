---
description: 'Weitere Informationen finden Sie unter: JET_PFNREALLOC Delegaten'
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
ms.openlocfilehash: 445cd4084ff187fba0b94e210d587b04660c0fb4dfe9e882e0c5696bfd5392df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119730420"
---
# <a name="jet_pfnrealloc-delegate"></a>JET_PFNREALLOC Delegat

Rückruf, der von JetEnumerateColumns verwendet wird, um Arbeitsspeicher für seine Ausgabepuffer zu reservieren.

Diese API ist nicht CLS-kompatibel. 

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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
    Typ: [System.IntPtr](/dotnet/api/system.intptr)  
    
    Für JetEnumerateColumns angegebener Kontext.

<!-- end list -->

  - Arbeitsspeicher  
    Typ: [System.IntPtr](/dotnet/api/system.intptr)  
    
    Wenn nicht 0 (null) ist, ein Zeiger auf einen Speicherblock, der zuvor von diesem Rückruf zugeordnet wurde.

<!-- end list -->

  - requestedSize  
    Typ: [System.UInt32](/dotnet/api/system.uint32)  
    
    Die neue Größe des Speicherblocks (in Bytes). Wenn dieser Wert 0 ist und ein Speicherblock angegeben wird, wird dieser Speicherblock frei.

#### <a name="return-value"></a>Rückgabewert

Typ: [System.IntPtr](/dotnet/api/system.intptr)  
Ein Zeiger auf neu zugewiesenen Arbeitsspeicher. Wenn kein Arbeitsspeicher zugeordnet werden konnte, sollte [0](/dotnet/api/system.intptr.zero) zurückgegeben werden.  

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
