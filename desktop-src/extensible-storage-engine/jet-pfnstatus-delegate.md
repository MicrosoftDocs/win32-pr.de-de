---
description: 'Weitere Informationen finden Sie hier: JET_PFNSTATUS-Delegaten'
title: JET_PFNSTATUS Delegat
TOCTitle: JET_PFNSTATUS delegate
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_PFNSTATUS
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_pfnstatus(v=EXCHG.10)
ms:contentKeyID: 39515654
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS..ctor
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS.EndInvoke
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS.Invoke
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS.BeginInvoke
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 16cc5807d858f964f995b449a0a0eee78659aefd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347729"
---
# <a name="jet_pfnstatus-delegate"></a>JET_PFNSTATUS Delegat

Empfängt Informationen zum Fortschritt von Vorgängen mit langer Ausführungszeit, z. b. Defragmentierungs-, Sicherungs-oder Wiederherstellungs Vorgänge. Bei solchen Vorgängen Ruft die Datenbank-Engine diese Rückruffunktion auf, um ein Update für den Fortschritt des Vorgangs zu erhalten.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Delegate Function JET_PFNSTATUS ( _
    sesid As JET_SESID, _
    snp As JET_SNP, _
    snt As JET_SNT, _
    data As Object _
) As JET_err
'Usage
Dim instance As New JET_PFNSTATUS(AddressOf HandlerMethod)
```

``` csharp
public delegate JET_err JET_PFNSTATUS(
    JET_SESID sesid,
    JET_SNP snp,
    JET_SNT snt,
    Object data
)
```

#### <a name="parameters"></a>Parameter

  - -sid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die Sitzung, mit der der Vorgang mit langer Laufzeit aufgerufen wurde.

<!-- end list -->

  - SNP  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_SNP](./jet-snp-enumeration.md)  
    
    Der Typ des Vorgangs.

<!-- end list -->

  - SNT  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_SNT](./jet-snt-enumeration.md)  
    
    Der Status des Vorgangs.

<!-- end list -->

  - Daten  
    Type: [System. Object](/dotnet/api/system.object)  
    
    Optionale Daten. Kann ein [JET_SNPROG](./jet-snprog-class.md)sein.

#### <a name="return-value"></a>Rückgabewert

Typ: [Microsoft.ISAM.ESENT.Interop.JET_err](./jet-err-enumeration.md)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
