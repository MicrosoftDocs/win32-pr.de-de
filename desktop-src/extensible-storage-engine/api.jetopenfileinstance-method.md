---
description: 'Weitere Informationen finden Sie hier: API. jetoperfileinstance-Methode'
title: API. jetopdenfileinstance-Methode
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
ms.openlocfilehash: 3b58b3a426fd2eb7e33cce1f5f539418bcc993ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369850"
---
# <a name="apijetopenfileinstance-method"></a>API. jetopdenfileinstance-Methode

Öffnet eine angefügte Datenbank, datenbankpatchdatei oder Transaktionsprotokoll Datei einer aktiven Instanz zum Ausführen einer Streaming-Fuzzy-Sicherung. Die Daten aus diesen Dateien können anschließend mithilfe von jetreadfileinstance durch das zurückgegebene Handle gelesen werden. Das zurückgegebene Handle muss mithilfe von jetclosefilinput Stance geschlossen werden. Eine externe Sicherung der Instanz muss mithilfe von jetbeginexternalbackupinstance initiiert werden.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

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
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Die zu verwendende-Instanz.

<!-- end list -->

  - file  
    Typ: [System. String](/dotnet/api/system.string)  
    
    Die zu öffnende Datei.

<!-- end list -->

  - Handlebezeichner  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_HANDLE](./jet-handle-structure.md)  
    
    Gibt ein Handle für die Datei zurück.

<!-- end list -->

  - filesizelow  
    Typ: [System. Int64](/dotnet/api/system.int64)  
    
    Gibt die am wenigsten signifikanten 32 Bits der Dateigröße zurück.

<!-- end list -->

  - filesizehigh  
    Typ: [System. Int64](/dotnet/api/system.int64)  
    
    Gibt die signifikantesten 32 Bits der Dateigröße zurück.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[API-Klasse](./api-class.md)

[API-Mitglieder](./api-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
