---
description: Weitere Informationen finden Sie in der API. jetrestorerstance-Methode.
title: API. jetrestoreingestance-Methode
TOCTitle: 'JetRestoreInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRestoreInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_PFNSTATUS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetrestoreinstance(v=EXCHG.10)
ms:contentKeyID: 55100787
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRestoreInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRestoreInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3e2c2976eb8bf661dc53bdc86723bb21309ab973
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346706"
---
# <a name="apijetrestoreinstance-method"></a>API. jetrestoreingestance-Methode

Stellt eine Streamingsicherung einer Instanz, einschließlich aller angefügten Datenbanken, wieder her. Es ist für die Arbeit mit einer Sicherung konzipiert, die mit der [jetbackupinstance (JET_INSTANCE, String, backupgrbit JET_PFNSTATUS)](./api.jetbackupinstance-method.md) -Funktion erstellt wurde. Dies ist die einfachste und gekapselte Restore-Funktion.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetRestoreInstance ( _
    instance As JET_INSTANCE, _
    source As String, _
    destination As String, _
    statusCallback As JET_PFNSTATUS _
)
'Usage
Dim instance As JET_INSTANCE
Dim source As String
Dim destination As String
Dim statusCallback As JET_PFNSTATUSApi.JetRestoreInstance(instance, _
    source, destination, statusCallback)
```

``` csharp
public static void JetRestoreInstance(
    JET_INSTANCE instance,
    string source,
    string destination,
    JET_PFNSTATUS statusCallback
)
```

#### <a name="parameters"></a>Parameter

  - instance  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Die zu verwendende-Instanz. Die Instanz sollte nicht initialisiert werden. Durch das Wiederherstellen der Dateien wird die Instanz initialisiert.

<!-- end list -->

  - source  
    Typ: [System. String](/dotnet/api/system.string)  
    
    Speicherort der Sicherung. Die Sicherung sollte mit [jetbackupinstance (JET_INSTANCE, String, backupgrbit JET_PFNSTATUS)](./api.jetbackupinstance-method.md)erstellt worden sein.

<!-- end list -->

  - destination  
    Typ: [System. String](/dotnet/api/system.string)  
    
    Der Name des Ordners, in den die Datenbankdateien aus dem Sicherungs Satz kopiert und wieder hergestellt werden. Wenn dieser Wert auf NULL festgelegt ist, werden die Datenbankdateien kopiert und an Ihrem ursprünglichen Speicherort wieder hergestellt.

<!-- end list -->

  - Status Rückruf  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)  
    
    Optionaler Status Benachrichtigungs Rückruf.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[API-Klasse](./api-class.md)

[API-Mitglieder](./api-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
