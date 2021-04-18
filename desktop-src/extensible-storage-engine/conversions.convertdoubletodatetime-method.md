---
description: 'Weitere Informationen finden Sie hier: Konvertierungen. convertdoublededatetime-Methode'
title: Konvertierungen. convertdoublededatetime-Methode
TOCTitle: 'ConvertDoubleToDateTime method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Conversions.ConvertDoubleToDateTime(System.Double)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conversions.convertdoubletodatetime(v=EXCHG.10)
ms:contentKeyID: 55101133
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Conversions.ConvertDoubleToDateTime
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Conversions.ConvertDoubleToDateTime
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a1d066780ade3da95f4d4d5500143700f7a7d5bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352605"
---
# <a name="conversionsconvertdoubletodatetime-method"></a>Konvertierungen. convertdoublededatetime-Methode

Konvertiert ein Double (OA-Datums-/Uhrzeitformat) in einen DateTime-Wert. Anders als DateTime. fromuadate löst dies keine Ausnahmen aus.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Function ConvertDoubleToDateTime ( _
    d As Double _
) As DateTime
'Usage
Dim d As Double
Dim returnValue As DateTime

returnValue = Conversions.ConvertDoubleToDateTime(d)
```

``` csharp
public static DateTime ConvertDoubleToDateTime(
    double d
)
```

#### <a name="parameters"></a>Parameter

  - d  
    Typ: [System. Double](/dotnet/api/system.double)  
    
    Der Double-Wert.

#### <a name="return-value"></a>Rückgabewert

Typ: [System. DateTime](/dotnet/api/system.datetime)  
Ein DateTime-Wert.  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Konvertierungs Klasse](./conversions-class.md)

[Konvertierungs Elemente](./conversions-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
