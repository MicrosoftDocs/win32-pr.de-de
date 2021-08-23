---
description: 'Erfahren Sie mehr über: JET_OSSNAPID. ToString-Methode (String, IFormatProvider)'
title: JET_OSSNAPID. ToString-Methode (String, IFormatProvider)
TOCTitle: ToString method (String, IFormatProvider)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_OSSNAPID.ToString(System.String,System.IFormatProvider)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_ossnapid.tostring(v=EXCHG.10)
ms:contentKeyID: 39512151
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_OSSNAPID.ToString
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 56e86765839434f2cd3a67c18f6395dd5443f21f8b905e6f86e6e85ad9915c3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038868"
---
# <a name="jet_ossnapidtostring-method-string-iformatprovider"></a>JET_OSSNAPID. ToString-Methode (String, IFormatProvider)

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
Dim instance As JET_OSSNAPID
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
    
    Die [Zeichenfolge,](/dotnet/api/system.string) die das zu verwendende Format angibt. Oder: NULL, um das Standardformat zu verwenden, das für den Typ der [IFormattable-Implementierung](/dotnet/api/system.iformattable) definiert ist.

<!-- end list -->

  - Formatprovider  
    Typ: [System.IFormatProvider](/dotnet/api/system.iformatprovider)  
    
    Der [IFormatProvider,](/dotnet/api/system.iformatprovider) der zum Formatieren des Werts verwendet werden soll. Oder: NULL, um die numerischen Formatinformationen aus der aktuellen Gebietsschemaeinstellung des Betriebssystems abzurufen.

#### <a name="return-value"></a>Rückgabewert

Typ: [System.String](/dotnet/api/system.string)  
Eine [Zeichenfolge,](/dotnet/api/system.string) die den Wert der aktuellen Instanz im angegebenen Format enthält.  

#### <a name="implements"></a>Implementiert

[IFormattable.ToString(String, IFormatProvider)](/dotnet/api/system.iformattable.tostring#System_IFormattable_ToString_System_String_System_IFormatProvider_)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[JET_OSSNAPID-Struktur](./jet-ossnapid-structure.md)

[JET_OSSNAPID-Member](./jet-ossnapid-members.md)

[ToString-Überladung](./jet-ossnapid.tostring-method.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
