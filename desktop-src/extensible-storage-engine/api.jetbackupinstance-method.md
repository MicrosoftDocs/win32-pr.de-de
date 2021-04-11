---
description: Weitere Informationen finden Sie in der API. jetbackupinstance-Methode.
title: API. jetbackupinstance-Methode
TOCTitle: 'JetBackupInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetBackupInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String,Microsoft.Isam.Esent.Interop.BackupGrbit,Microsoft.Isam.Esent.Interop.JET_PFNSTATUS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetbackupinstance(v=EXCHG.10)
ms:contentKeyID: 55107221
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetBackupInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetBackupInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 73c5b44f1f0b69aaed6066635ad4e82690bc3c37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128057"
---
# <a name="apijetbackupinstance-method"></a>API. jetbackupinstance-Methode

Führt eine Streamingsicherung einer Instanz, einschließlich aller angefügten Datenbanken, in ein Verzeichnis aus. Mit mehreren Sicherungsmethoden, die von der-Engine unterstützt werden, ist dies die einfachste und gekapselte Funktion.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetBackupInstance ( _
    instance As JET_INSTANCE, _
    destination As String, _
    grbit As BackupGrbit, _
    statusCallback As JET_PFNSTATUS _
)
'Usage
Dim instance As JET_INSTANCE
Dim destination As String
Dim grbit As BackupGrbit
Dim statusCallback As JET_PFNSTATUSApi.JetBackupInstance(instance, _
    destination, grbit, statusCallback)
```

``` csharp
public static void JetBackupInstance(
    JET_INSTANCE instance,
    string destination,
    BackupGrbit grbit,
    JET_PFNSTATUS statusCallback
)
```

#### <a name="parameters"></a>Parameter

  - instance  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Die Instanz, die gesichert werden soll.

<!-- end list -->

  - destination  
    Typ: [System. String](/dotnet/api/system.string)  
    
    Das Verzeichnis, in dem die Sicherung gespeichert werden soll. Wenn der Sicherungs Pfad für die Verwendung von NULL ist, schneidet die-Funktion die Protokolle ab, sofern dies möglich ist.

<!-- end list -->

  - grbit  
    Typ: [Microsoft. ISAM. ESENT. Interop. backupgrbit](./backupgrbit-enumeration.md)  
    
    Sicherungs Optionen.

<!-- end list -->

  - Status Rückruf  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)  
    
    Optionaler Status Benachrichtigungs Rückruf.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[API-Klasse](./api-class.md)

[API-Mitglieder](./api-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
