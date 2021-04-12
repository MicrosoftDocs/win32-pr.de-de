---
description: 'Weitere Informationen finden Sie unter: JET_INDEXCREATE. szkey-Eigenschaft'
title: JET_INDEXCREATE. szkey-Eigenschaft
TOCTitle: 'szKey property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.szKey
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate.szkey(v=EXCHG.10)
ms:contentKeyID: 55103656
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.szKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.get_szKey
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.set_szKey
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.szKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 86ade65ee28eef6314d31653772b0c22657476d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348799"
---
# <a name="jet_indexcreateszkey-property"></a>JET_INDEXCREATE. szkey-Eigenschaft

Ruft die Beschreibung des Index Schlüssels ab oder legt Sie fest. Dies ist eine Double-NULL-terminierte Zeichenfolge mit durch Null getrennten Token. Jedes Token hat die Form " \[ Direction-specifier \] \[ Column-Name \] ", wobei "Direction-Specification" entweder "+" oder "-" ist. beispielsweise indiziert ein szkey-Wert von "+ ABC \\ 0-DEF \\ 0 + ghi \\ 0" die drei Spalten "ABC" (in aufsteigender Reihenfolge), "Def" (in absteigender Reihenfolge) und "ghi" (in aufsteigender Reihenfolge).

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property szKey As String
    Get
    Set
'Usage
Dim instance As JET_INDEXCREATE
Dim value As String

value = instance.szKey

instance.szKey = value
```

``` csharp
public string szKey { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System. String](/dotnet/api/system.string)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_INDEXCREATE-Klasse](./jet-indexcreate-class.md)

[Mitglieder JET_INDEXCREATE](./jet-indexcreate-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
