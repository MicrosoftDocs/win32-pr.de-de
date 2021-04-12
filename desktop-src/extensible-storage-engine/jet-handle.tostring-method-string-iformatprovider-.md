---
description: 'Weitere Informationen finden Sie hier: JET_HANDLE. Methode "destring" (String, IFormatProvider)'
title: JET_HANDLE. Methode "destring" (String, IFormatProvider)
TOCTitle: ToString method (String, IFormatProvider)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_HANDLE.ToString(System.String,System.IFormatProvider)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_handle.tostring(v=EXCHG.10)
ms:contentKeyID: 39515173
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_HANDLE.ToString
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c2891e33712027c3387e2d45ff73111e7bf54126
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348809"
---
# <a name="jet_handletostring-method-string-iformatprovider"></a>JET_HANDLE. Methode "destring" (String, IFormatProvider)

Formatiert den Wert der aktuellen Instanz mit dem angegebenen Format.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Function ToString ( _
    format As String, _
    formatProvider As IFormatProvider _
) As String
'Usage
Dim instance As JET_HANDLE
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
    Typ: [System. String](/dotnet/api/system.string)  
    
    Die [Zeichenfolge](/dotnet/api/system.string) , die das zu verwendende Format angibt. -oder-NULL, um das für den Typ der [IFormattable](/dotnet/api/system.iformattable) -Implementierung definierte Standardformat zu verwenden.

<!-- end list -->

  - Format Provider  
    Typ: [System. IFormatProvider](/dotnet/api/system.iformatprovider)  
    
    Der [IFormatProvider](/dotnet/api/system.iformatprovider) , der zum Formatieren des Werts verwendet werden soll. -oder-NULL zum Abrufen der numerischen Formatinformationen aus der aktuellen Gebiets Schema Einstellung des Betriebssystems.

#### <a name="return-value"></a>Rückgabewert

Typ: [System. String](/dotnet/api/system.string)  
Eine [Zeichenfolge](/dotnet/api/system.string) , die den Wert der aktuellen Instanz im angegebenen Format enthält.  

#### <a name="implements"></a>Implementiert

[IFormattable. to String (String, IFormatProvider)](/dotnet/api/system.iformattable.tostring#System_IFormattable_ToString_System_String_System_IFormatProvider_)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[JET_HANDLE Struktur](./jet-handle-structure.md)

[Mitglieder JET_HANDLE](./jet-handle-members.md)

[Überladung von ""](./jet-handle.tostring-method.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
