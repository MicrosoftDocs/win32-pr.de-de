---
description: 'Erfahren Sie mehr über: JET_DBID. ToString-Methode (String, IFormatProvider)'
title: JET_DBID. ToString-Methode (String, IFormatProvider)
TOCTitle: ToString method (String, IFormatProvider)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_DBID.ToString(System.String,System.IFormatProvider)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbid.tostring(v=EXCHG.10)
ms:contentKeyID: 39513106
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBID.ToString
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7b6fca1494a31bc342d4f8ad2933968c58efacc5f5e115ff10fe92a8afbabca8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017258"
---
# <a name="jet_dbidtostring-method-string-iformatprovider"></a>JET_DBID. ToString-Methode (String, IFormatProvider)

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
Dim instance As JET_DBID
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

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[JET_DBID-Struktur](./jet-dbid-structure.md)

[JET_DBID-Member](./jet-dbid-members.md)

[ToString-Überladung](./jet-dbid.tostring-method.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
