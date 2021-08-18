---
description: 'Weitere Informationen finden Sie unter: JET_LS. ToString-Methode (String, IFormatProvider)'
title: JET_LS. ToString-Methode (String, IFormatProvider)
TOCTitle: ToString method (String, IFormatProvider)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LS.ToString(System.String,System.IFormatProvider)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_ls.tostring(v=EXCHG.10)
ms:contentKeyID: 39512228
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_LS.ToString
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1011f8433b98925d8c3c08112dd1c4d0c5e6c2f3672b66ece5d6f11070f3d549
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119401330"
---
# <a name="jet_lstostring-method-string-iformatprovider"></a>JET_LS. ToString-Methode (String, IFormatProvider)

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
Dim instance As JET_LS
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
    
    Die [Zeichenfolge,](/dotnet/api/system.string) die das zu verwendende Format angibt. Oder: NULL, um das für den Typ der [IFormattable-Implementierung](/dotnet/api/system.iformattable) definierte Standardformat zu verwenden.

<!-- end list -->

  - Formatprovider  
    Typ: [System.IFormatProvider](/dotnet/api/system.iformatprovider)  
    
    Der [IFormatProvider, der](/dotnet/api/system.iformatprovider) zum Formatieren des Werts verwendet werden soll. Oder: NULL, um die numerischen Formatinformationen aus der aktuellen Locale-Einstellung des Betriebssystems zu erhalten.

#### <a name="return-value"></a>Rückgabewert

Typ: [System.String](/dotnet/api/system.string)  
Eine [Zeichenfolge,](/dotnet/api/system.string) die den Wert der aktuellen Instanz im angegebenen Format enthält.  

#### <a name="implements"></a>Implementiert

[IFormattable.ToString(String, IFormatProvider)](/dotnet/api/system.iformattable.tostring#System_IFormattable_ToString_System_String_System_IFormatProvider_)  

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[JET_LS-Struktur](./jet-ls-structure.md)

[JET_LS Member](./jet-ls-members.md)

[ToString-Überladung](./jet-ls.tostring-method2.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
