---
description: Weitere Informationen finden Sie in der JET_TABLECREATE. szcallback-Eigenschaft.
title: JET_TABLECREATE. szcallback-Eigenschaft
TOCTitle: 'szCallback property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_TABLECREATE.szCallback
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tablecreate.szcallback(v=EXCHG.10)
ms:contentKeyID: 55103969
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.szCallback
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.set_szCallback
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.get_szCallback
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.szCallback
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3a987f274cf82ebdc3c2113fd1636174c51382f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339739"
---
# <a name="jet_tablecreateszcallback-property"></a>JET_TABLECREATE. szcallback-Eigenschaft

Ruft eine Rückruffunktion ab, die für die Tabelle verwendet wird, oder legt Sie fest. Diese weist das Format "Module \! FunctionName" auf und geht von nicht verwaltetem Code aus. Eine Alternative finden Sie **unter jetregistercallback (JET_SESID, JET_TABLEID, JET_cbtyp, JET_CALLBACK, IntPtr, JET_HANDLE)** .

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property szCallback As String
    Get
    Set
'Usage
Dim instance As JET_TABLECREATE
Dim value As String

value = instance.szCallback

instance.szCallback = value
```

``` csharp
public string szCallback { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System. String](/dotnet/api/system.string)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_TABLECREATE-Klasse](./jet-tablecreate-class.md)

[Mitglieder JET_TABLECREATE](./jet-tablecreate-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
