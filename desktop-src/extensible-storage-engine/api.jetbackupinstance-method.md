---
description: 'Weitere Informationen finden Sie unter: Api.JetBackupInstance-Methode'
title: Api.JetBackupInstance-Methode
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
ms.openlocfilehash: 4a4b9ef9fbedce13b9c68940fc45204a35c1113e9551034fa57ed6948f4fa5e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118983650"
---
# <a name="apijetbackupinstance-method"></a>Api.JetBackupInstance-Methode

Führt eine Streamingsicherung einer Instanz einschließlich aller angefügten Datenbanken in einem Verzeichnis aus. Da die Engine mehrere Sicherungsmethoden unterstützt, ist dies die einfachste und am häufigsten gekapselte Funktion.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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
    Typ: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Die zu sichernde Instanz.

<!-- end list -->

  - destination  
    Typ: [System.String](/dotnet/api/system.string)  
    
    Das Verzeichnis, in dem die Sicherung gespeichert werden soll. Wenn der Sicherungspfad null ist, um die Funktion zu verwenden, werden die Protokolle nach Möglichkeit abgeschnitten.

<!-- end list -->

  - grbit  
    Typ: [Microsoft.Isam.Esent.Interop.BackupGrbit](./backupgrbit-enumeration.md)  
    
    Sicherungsoptionen.

<!-- end list -->

  - statusCallback  
    Typ: [Microsoft.Isam.Esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)  
    
    Optionaler Statusbenachrichtigungsrückruf.

## <a name="see-also"></a>Weitere Informationen

#### <a name="reference"></a>Verweis

[API-Klasse](./api-class.md)

[API-Member](./api-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
