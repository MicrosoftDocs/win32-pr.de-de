---
description: 'Weitere Informationen zu: JET_INDEXCREATE.szKey-Eigenschaft'
title: JET_INDEXCREATE.szKey-Eigenschaft
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
ms.openlocfilehash: 905bc6e72704121617a2fcc2b9b368bee9014f897ce157f473e3f9ced5a92c72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119720570"
---
# <a name="jet_indexcreateszkey-property"></a>JET_INDEXCREATE.szKey-Eigenschaft

Ruft die Beschreibung des Indexschlüssels ab oder legt sie fest. Dies ist eine doppelt auf NULL endende Zeichenfolge von Token mit NULL-Trennzeichen. Jedes Token hat den \[ \] Formrichtungsspezifiziererspaltennamen \[ \] , wobei direction-specification entweder "+" oder "-" ist. Beispielsweise indiziert ein szKey von "+abc \\ 0-def \\ 0+ähl \\ 0" die drei Spalten "abc" (in aufsteigender Reihenfolge), "def" (in absteigender Reihenfolge) und " whi" (in aufsteigender Reihenfolge).

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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

Typ: [System.String](/dotnet/api/system.string)  

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[JET_INDEXCREATE-Klasse](./jet-indexcreate-class.md)

[JET_INDEXCREATE-Member](./jet-indexcreate-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
