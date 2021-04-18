---
description: Weitere Informationen finden Sie in der JET_OPENTEMPORARYTABLE. pidxunicode-Eigenschaft.
title: JET_OPENTEMPORARYTABLE. pidxunicode-Eigenschaft (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'pidxunicode property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.pidxunicode
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable.pidxunicode(v=EXCHG.10)
ms:contentKeyID: 55104227
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.pidxunicode
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.set_pidxunicode
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.get_pidxunicode
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.pidxunicode
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 98e5beb4f4523f5e6a6da37a999b6c0a2ab7b4d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352722"
---
# <a name="jet_opentemporarytablepidxunicode-property"></a>JET_OPENTEMPORARYTABLE. pidxunicode (Eigenschaft)

Ruft die Gebiets Schema-ID und normalisierungs Flags ab, die zum Vergleichen von Unicode-Schlüssel Spaltendaten in der temporären Tabelle verwendet werden, oder legt diese fest Wenn dieser Parameter NULL ist, wird die Standard-LCID verwendet, um alle Unicode-Schlüssel Spalten in der temporären Tabelle zu vergleichen. Die Standard-LCID ist das US-englische Gebiets Schema. Wenn dieser Parameter NULL ist, werden die standardnormalisierungs-Flags verwendet, um alle Unicode-Schlüssel Spaltendaten in der temporären Tabelle zu vergleichen. Die standardnormalisierungs-Flags lauten: NORM_IGNORECASE, NORM_IGNOREKANATYPE und NORM_IGNOREWIDTH.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property pidxunicode As JET_UNICODEINDEX
    Get
    Set
'Usage
Dim instance As JET_OPENTEMPORARYTABLE
Dim value As JET_UNICODEINDEX

value = instance.pidxunicode

instance.pidxunicode = value
```

``` csharp
public JET_UNICODEINDEX pidxunicode { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [Microsoft.ISAM.ESENT.Interop.JET_UNICODEINDEX](./jet-unicodeindex-class.md)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_OPENTEMPORARYTABLE-Klasse](./jet-opentemporarytable-class.md)

[Mitglieder JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-members.md)

[Microsoft. ISAM. ESENT. Interop. Vista-Namespace](./microsoft.isam.esent.interop.vista-namespace.md)
