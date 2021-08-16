---
description: 'Weitere Informationen finden Sie unter: JET_LS Struktur'
title: JET_LS-Struktur
TOCTitle: JET_LS structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_LS
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_ls(v=EXCHG.10)
ms:contentKeyID: 39510760
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LS
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1fa85ea0f3117d6f4f9c0c9102f21f2fb1f626f8c115144998c1a4c94c300626
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118765086"
---
# <a name="jet_ls-structure"></a>JET_LS-Struktur

Lokaler Speicher für ein ESENT-Handle. Wird von [JetGetLS(JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetgetls-method.md) und [JetSetLS(JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetsetls-method.md)verwendet.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Structure JET_LS _
    Implements IEquatable(Of JET_LS), IFormattable
'Usage
Dim instance As JET_LS
```

``` csharp
public struct JET_LS : IEquatable<JET_LS>, 
    IFormattable
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[JET_LS Mitglieder](./jet-ls-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
