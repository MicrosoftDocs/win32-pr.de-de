---
description: 'Weitere Informationen finden Sie unter: Api.JetRestoreInstance-Methode'
title: Api.JetRestoreInstance-Methode
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
ms.openlocfilehash: 3fef9ca38f8e8efb86813666840f859ed10287197d5f3b6ed0bafdd434ea43dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119947770"
---
# <a name="apijetrestoreinstance-method"></a>Api.JetRestoreInstance-Methode

Stellt eine Streamingsicherung einer Instanz einschließlich aller angefügten Datenbanken wieder her und stellt sie wieder her. Sie ist für die Arbeit mit einer Sicherung konzipiert, die mit der [JetBackupInstance(JET_INSTANCE-, String-, BackupGrbit-, JET_PFNSTATUS)-Funktion](./api.jetbackupinstance-method.md) erstellt wurde. Dies ist die einfachste und am häufigsten gekapselte Wiederherstellungsfunktion.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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
    Typ: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Die zu verwendende -Instanz. Die -Instanz sollte nicht initialisiert werden. Beim Wiederherstellen der Dateien wird die -Instanz initialisiert.

<!-- end list -->

  - source  
    Typ: [System.String](/dotnet/api/system.string)  
    
    Speicherort der Sicherung. Die Sicherung sollte mit [JetBackupInstance(JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)](./api.jetbackupinstance-method.md)erstellt worden sein.

<!-- end list -->

  - destination  
    Typ: [System.String](/dotnet/api/system.string)  
    
    Name des Ordners, in den die Datenbankdateien aus dem Sicherungssatz kopiert und wiederhergestellt werden. Wenn diese Einstellung auf NULL festgelegt ist, werden die Datenbankdateien kopiert und an ihrem ursprünglichen Speicherort wiederhergestellt.

<!-- end list -->

  - statusCallback  
    Typ: [Microsoft.Isam.Esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)  
    
    Optionaler Statusbenachrichtigungsrückruf.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Verweis

[API-Klasse](./api-class.md)

[API-Member](./api-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
