---
description: Weitere Informationen finden Sie unter Api.JetCompact-Methode.
title: Api.JetCompact-Methode
TOCTitle: 'JetCompact method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCompact(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_PFNSTATUS,Microsoft.Isam.Esent.Interop.JET_CONVERT,Microsoft.Isam.Esent.Interop.CompactGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcompact(v=EXCHG.10)
ms:contentKeyID: 55100666
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCompact
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCompact
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8aecd3ec6120a93edb19b06d1f86c9573c1404f8dc1feb95c1acfec2d0077bcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118983460"
---
# <a name="apijetcompact-method"></a>Api.JetCompact-Methode

Erstellt eine Kopie einer vorhandenen Datenbank. Die Kopie wird für die Verwendung in einen optimalen Zustand komprimiert. Die Daten in den kopierten Daten werden entsprechend den Measures gepackt, die für die Indizes bei der Indexerstellung ausgewählt wurden. Auf diese Weise können komprimierte Daten so dichte wie möglich gespeichert werden. Alternativ können komprimierte Daten Speicherplatz für nachfolgende Datensatzvergrößerungen oder Indexeinfügungen reservieren.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetCompact ( _
    sesid As JET_SESID, _
    sourceDatabase As String, _
    destinationDatabase As String, _
    statusCallback As JET_PFNSTATUS, _
    ignored As JET_CONVERT, _
    grbit As CompactGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim sourceDatabase As String
Dim destinationDatabase As String
Dim statusCallback As JET_PFNSTATUS
Dim ignored As JET_CONVERT
Dim grbit As CompactGrbitApi.JetCompact(sesid, sourceDatabase, _
    destinationDatabase, statusCallback, _
    ignored, grbit)
```

``` csharp
public static void JetCompact(
    JET_SESID sesid,
    string sourceDatabase,
    string destinationDatabase,
    JET_PFNSTATUS statusCallback,
    JET_CONVERT ignored,
    CompactGrbit grbit
)
```

#### <a name="parameters"></a>Parameter

  - sesid  
    Typ: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die Sitzung, die für den Aufruf verwendet werden soll.

<!-- end list -->

  - sourceDatabase  
    Typ: [System.String](/dotnet/api/system.string)  
    
    Die Quelldatenbank, die komprimiert wird.

<!-- end list -->

  - destinationDatabase  
    Typ: [System.String](/dotnet/api/system.string)  
    
    Der Name, der für die komprimierte Datenbank verwendet werden soll.

<!-- end list -->

  - statusCallback  
    Typ: [Microsoft.Isam.Esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)  
    
    Eine Rückruffunktion, die regelmäßig über den Datenbank-Compact-Vorgang aufgerufen werden kann, um den Fortschritt zu melden.

<!-- end list -->

  - wird ignoriert.  
    Typ: [Microsoft.Isam.Esent.Interop.JET_CONVERT](./jet-convert-class.md)  
    
    Dieser Parameter wird ignoriert und sollte NULL sein.

<!-- end list -->

  - grbit  
    Typ: [Microsoft.Isam.Esent.Interop.CompactGrbit](./compactgrbit-enumeration.md)  
    
    Kompakte Optionen.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[API-Klasse](./api-class.md)

[API-Member](./api-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
