---
description: Weitere Informationen finden Sie in der API. jetcompact-Methode.
title: API. jetcompact-Methode
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
ms.openlocfilehash: 74d714a1b0fa8d53743945afb3a35cc2015df293
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958810"
---
# <a name="apijetcompact-method"></a>API. jetcompact-Methode

Erstellt eine Kopie einer vorhandenen Datenbank. Die Kopie wird zu einem für die Verwendung optimalen Zustand komprimiert. Die Daten in den kopierten Daten werden entsprechend den Measures verpackt, die bei der Indexerstellung für die Indizes ausgewählt wurden. Auf diese Weise können komprimierte Daten so dicht wie möglich gespeichert werden. Alternativ können durch komprimierte Datenspeicher Platz für nachfolgende Daten Satz Vergrößerung oder Index Einfügungen reserviert werden.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

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

  - -sid  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Die für den-Befehl zu verwendende Sitzung.

<!-- end list -->

  - sourceDatabase  
    Typ: [System. String](/dotnet/api/system.string)  
    
    Die Quelldatenbank, die komprimiert wird.

<!-- end list -->

  - destinationDatabase  
    Typ: [System. String](/dotnet/api/system.string)  
    
    Der Name, der für die komprimierte Datenbank verwendet werden soll.

<!-- end list -->

  - Status Rückruf  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)  
    
    Eine Rückruffunktion, die regelmäßig über den Daten Bank Compact-Vorgang aufgerufen werden kann, um den Status zu melden.

<!-- end list -->

  - wird ignoriert.  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_CONVERT](./jet-convert-class.md)  
    
    Dieser Parameter wird ignoriert und sollte NULL sein.

<!-- end list -->

  - grbit  
    Typ: [Microsoft. ISAM. ESENT. Interop. compactgrbit](./compactgrbit-enumeration.md)  
    
    Compact-Optionen.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[API-Klasse](./api-class.md)

[API-Mitglieder](./api-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
