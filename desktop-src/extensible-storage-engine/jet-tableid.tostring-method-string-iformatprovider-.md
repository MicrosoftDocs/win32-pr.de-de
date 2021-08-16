---
description: 'Weitere Informationen finden Sie unter: JET_TABLEID. ToString-Methode (String, IFormatProvider)'
title: JET_TABLEID. ToString-Methode (String, IFormatProvider)
TOCTitle: ToString method (String, IFormatProvider)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_TABLEID.ToString(System.String,System.IFormatProvider)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tableid.tostring(v=EXCHG.10)
ms:contentKeyID: 39510805
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_TABLEID.ToString
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a674e980f86b57e7dd12fe451bc413b5b9b2f90b4cdc218be8753d7955376997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118979200"
---
# <a name="jet_tableidtostring-method-string-iformatprovider"></a>JET_TABLEID. ToString-Methode (String, IFormatProvider)

Formatiert den Wert der aktuellen Instanz mit dem angegebenen Format.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Function ToString ( _
    format As String, _
    formatProvider As IFormatProvider _
) As String
'Usage
Dim instance As JET_TABLEID
Dim format As String
Dim formatProvider As IFormatProvider
Dim returnValue As String

returnValue = instance.ToString(format, _
    formatProvider)
```

``` csharp
public string ToString(
    string format,
    IFormatProvider formatProvider
)
```

#### <a name="parameters"></a>Parameter

  - format  
    Typ: [System.String](/dotnet/api/system.string)  
    
    Die [Zeichenfolge,](/dotnet/api/system.string) die das zu verwendende Format angibt; oder NULL, um das für den Typ der [IFormattable-Implementierung](/dotnet/api/system.iformattable) definierte Standardformat zu verwenden.

<!-- end list -->

  - Formatprovider  
    Typ: [System.IFormatProvider](/dotnet/api/system.iformatprovider)  
    
    Der [IFormatProvider, der](/dotnet/api/system.iformatprovider) zum Formatieren des Werts verwendet werden soll. oder NULL, um die numerischen Formatinformationen aus der aktuellen Locale-Einstellung des Betriebssystems zu erhalten.

#### <a name="return-value"></a>Rückgabewert

Typ: [System.String](/dotnet/api/system.string)  
Eine [Zeichenfolge,](/dotnet/api/system.string) die den Wert der aktuellen Instanz im angegebenen Format enthält.  

#### <a name="implements"></a>Implementiert

[IFormattable.ToString(String, IFormatProvider)](/dotnet/api/system.iformattable.tostring#System_IFormattable_ToString_System_String_System_IFormatProvider_)  

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[JET_TABLEID-Struktur](./jet-tableid-structure.md)

[JET_TABLEID Mitglieder](./jet-tableid-members.md)

[ToString-Überladung](./jet-tableid.tostring-method.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
