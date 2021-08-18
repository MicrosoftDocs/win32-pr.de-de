---
description: 'Weitere Informationen zu: JET_RECPOS-Klasse'
title: JET_RECPOS-Klasse
TOCTitle: JET_RECPOS class
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_RECPOS
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_recpos(v=EXCHG.10)
ms:contentKeyID: 55103839
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RECPOS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RECPOS
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c25fd9cb9af531f134627ffcc54cd9fa5d37a33b340c53129a83c6538b33b1f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119107519"
---
# <a name="jet_recpos-class"></a>JET_RECPOS-Klasse

Stellt eine Bruchposition innerhalb eines Indexes dar. Dies wird von JetGotoPosition und JetGetRecordPosition verwendet.

## <a name="inheritance-hierarchy"></a>Vererbungshierarchie

[System.Object](/dotnet/api/system.object)  
  Microsoft.Isam.Esent.Interop.JET_RECPOS  

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class JET_RECPOS _
    Implements IContentEquatable(Of JET_RECPOS), IDeepCloneable(Of JET_RECPOS)
'Usage
Dim instance As JET_RECPOS
```

``` csharp
[SerializableAttribute]
public sealed class JET_RECPOS : IContentEquatable<JET_RECPOS>, 
    IDeepCloneable<JET_RECPOS>
```

## <a name="thread-safety"></a>Threadsicherheit

Alle öffentlichen statischen Elemente dieses Typs (Shared in Microsoft Visual Basic) sind threadsicher. Bei Instanzmembern ist die Threadsicherheit nicht gewährleistet.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[JET_RECPOS-Member](./jet-recpos-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
