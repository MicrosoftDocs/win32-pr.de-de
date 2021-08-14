---
description: 'Weitere Informationen finden Sie unter: JET_OPENTEMPORARYTABLE.pidxunicode-Eigenschaft'
title: JET_OPENTEMPORARYTABLE.pidxunicode-Eigenschaft (Microsoft.Isam.Esent.Interop.Vista)
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
ms.openlocfilehash: 378c1497d57e3d904398d92d654579cc4a8702271db3525a2943e50ae3d03726
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118074024"
---
# <a name="jet_opentemporarytablepidxunicode-property"></a>JET_OPENTEMPORARYTABLE.pidxunicode-Eigenschaft

Ruft die Locale ID und die Normalisierungsflags ab, die zum Vergleichen von Unicode-Schlüsselspaltendaten in der temporären Tabelle verwendet werden, oder legt diese fest. Wenn dieser Parameter NULL ist, wird die Standard-LCID verwendet, um alle Unicode-Schlüsselspalten in der temporären Tabelle zu vergleichen. Die Standard-LCID ist das us-englische Locale. Wenn dieser Parameter NULL ist, werden die Standardnormalisierungsflags verwendet, um alle Unicode-Schlüsselspaltendaten in der temporären Tabelle zu vergleichen. Die Standardnormalisierungsflags sind: NORM_IGNORECASE, NORM_IGNOREKANATYPE und NORM_IGNOREWIDTH.

**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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

Typ: [Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX](./jet-unicodeindex-class.md)  

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[JET_OPENTEMPORARYTABLE-Klasse](./jet-opentemporarytable-class.md)

[JET_OPENTEMPORARYTABLE Member](./jet-opentemporarytable-members.md)

[Microsoft.Isam.Esent.Interop.Vista-Namespace](./microsoft.isam.esent.interop.vista-namespace.md)
