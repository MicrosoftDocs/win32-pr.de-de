---
description: 'Weitere Informationen finden Sie unter: Api.JetOpenFileInstance-Methode'
title: Api.JetOpenFileInstance-Methode
TOCTitle: 'JetOpenFileInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenFileInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String,Microsoft.Isam.Esent.Interop.JET_HANDLE@,System.Int64@,System.Int64@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopenfileinstance(v=EXCHG.10)
ms:contentKeyID: 55100767
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenFileInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenFileInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1dc526cb9d70b86faa54c476cb1d2fa85a93ec032b2fcc5a3d1755779108a8cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118084959"
---
# <a name="apijetopenfileinstance-method"></a>Api.JetOpenFileInstance-Methode

Öffnet eine angefügte Datenbank, eine Datenbankpatchdatei oder eine Transaktionsprotokolldatei einer aktiven Instanz, um eine Streaming-Fuzzysicherung durchführen zu können. Die Daten aus diesen Dateien können anschließend mit JetReadFileInstance über das zurückgegebene Handle gelesen werden. Das zurückgegebene Handle muss mit JetCloseFileInstance geschlossen werden. Eine externe Sicherung der Instanz muss zuvor mit JetBeginExternalBackupInstance initiiert worden sein.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetOpenFileInstance ( _
    instance As JET_INSTANCE, _
    file As String, _
    <OutAttribute> ByRef handle As JET_HANDLE, _
    <OutAttribute> ByRef fileSizeLow As Long, _
    <OutAttribute> ByRef fileSizeHigh As Long _
)
'Usage
Dim instance As JET_INSTANCE
Dim file As String
Dim handle As JET_HANDLE
Dim fileSizeLow As Long
Dim fileSizeHigh As LongApi.JetOpenFileInstance(instance, _
    file, handle, fileSizeLow, fileSizeHigh)
```

``` csharp
public static void JetOpenFileInstance(
    JET_INSTANCE instance,
    string file,
    out JET_HANDLE handle,
    out long fileSizeLow,
    out long fileSizeHigh
)
```

#### <a name="parameters"></a>Parameter

  - instance  
    Typ: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Die zu verwendende -Instanz.

<!-- end list -->

  - file  
    Typ: [System.String](/dotnet/api/system.string)  
    
    Die zu öffnende Datei.

<!-- end list -->

  - Handlebezeichner  
    Typ: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)  
    
    Gibt ein Handle für die Datei zurück.

<!-- end list -->

  - fileSizeLow  
    Typ: [System.Int64](/dotnet/api/system.int64)  
    
    Gibt die am wenigsten signifikanten 32 Bits der Dateigröße zurück.

<!-- end list -->

  - fileSizeHigh  
    Typ: [System.Int64](/dotnet/api/system.int64)  
    
    Gibt die signifikantesten 32 Bits der Dateigröße zurück.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[API-Klasse](./api-class.md)

[API-Member](./api-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
