---
description: 'Weitere Informationen finden Sie hier: JET_LOGTIME. "DateTime"-Methode'
title: JET_LOGTIME. "DateTime"-Methode
TOCTitle: 'ToDateTime method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LOGTIME.ToDateTime
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_logtime.todatetime(v=EXCHG.10)
ms:contentKeyID: 39512964
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LOGTIME.ToDateTime
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LOGTIME.ToDateTime
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 14d427d1c7e4a6f37c27677ed9617d92eb8ff644
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760543"
---
# <a name="jet_logtimetodatetime-method"></a>JET_LOGTIME. "DateTime"-Methode

Generiert eine DateTime-Darstellung dieses JET_LOGTIME.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Function ToDateTime As Nullable(Of DateTime)
'Usage
Dim instance As JET_LOGTIME
Dim returnValue As Nullable(Of DateTime)

returnValue = instance.ToDateTime()
```

``` csharp
public Nullable<DateTime> ToDateTime()
```

#### <a name="return-value"></a>Rückgabewert

Typ: [System. Nullable](/dotnet/api/system.nullable-1)\<[DateTime](/dotnet/api/system.datetime)\>  
Ein DateTime-Wert, der die JET_LOGTIME darstellt. Wenn die JET_LOGTIME NULL ist, wird NULL zurückgegeben.  

#### <a name="implements"></a>Implementiert

[IJET_LOGTIME. "DateTime ()"](./ijet-logtime.todatetime-method.md)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_LOGTIME Struktur](./jet-logtime-structure2.md)

[Mitglieder JET_LOGTIME](./jet-logtime-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
