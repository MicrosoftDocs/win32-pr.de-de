---
description: 'Weitere Informationen finden Sie unter: Api.JetGetAttachInfoInstance-Methode'
title: Api.JetGetAttachInfoInstance-Methode
TOCTitle: 'JetGetAttachInfoInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetAttachInfoInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String@,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetattachinfoinstance(v=EXCHG.10)
ms:contentKeyID: 55100704
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetAttachInfoInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetAttachInfoInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 29796919302b19b708878feb31e1fd53151700694a67bd1f6943bfa9d82d419c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118272456"
---
# <a name="apijetgetattachinfoinstance-method"></a>Api.JetGetAttachInfoInstance-Methode

Wird während einer Sicherung verwendet, die von [JetBeginExternalBackupInstance(JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md) initiiert wird, um eine Instanz nach den Namen von Datenbankdateien abfragt, die Teil des Sicherungsdateisets werden sollen. Es werden nur Datenbanken berücksichtigt, die derzeit mit [JetAttachDatabase(JET_SESID, String, AttachDatabaseGrbit)](./api.jetattachdatabase-method.md) an die Instanz angefügt sind. Diese Dateien können anschließend mit [JetOpenFileInstance(JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md) geöffnet und mit [JetReadFileInstance(JET_INSTANCE, JET_HANDLE, \[ \] , Int32, Int32)](./api.jetreadfileinstance-method.md)gelesen werden.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetGetAttachInfoInstance ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef files As String, _
    maxChars As Integer, _
    <OutAttribute> ByRef actualChars As Integer _
)
'Usage
Dim instance As JET_INSTANCE
Dim files As String
Dim maxChars As Integer
Dim actualChars As IntegerApi.JetGetAttachInfoInstance(instance, _
    files, maxChars, actualChars)
```

``` csharp
public static void JetGetAttachInfoInstance(
    JET_INSTANCE instance,
    out string files,
    int maxChars,
    out int actualChars
)
```

#### <a name="parameters"></a>Parameter

  - instance  
    Typ: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Die -Instanz, für die die Informationen erhalten werden.

<!-- end list -->

  - files  
    Typ: [System.String](/dotnet/api/system.string)  
    
    Gibt eine Liste der auf NULL beendeten Zeichenfolgen zurück, die den Satz von Datenbankdateien beschreiben, die Teil des Sicherungsdateisets sein sollen. Die Liste der in diesem Puffer zurückgegebenen Zeichenfolgen hat das gleiche Format wie eine von der Registrierung verwendete Mehrfachzeichenfolge. Jede auf NULL endende Zeichenfolge wird nacheinander zurückgegeben, gefolgt von einem abschließenden NULL-Abschlusszeichen.

<!-- end list -->

  - maxChars  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Maximale Anzahl der abzurufenden Zeichen.

<!-- end list -->

  - actualChars  
    Typ: [System.Int32](/dotnet/api/system.int32)  
    
    Tatsächliche Größe der Dateiliste. Wenn dies größer als maxChars ist, wurde die Liste abgeschnitten.

## <a name="remarks"></a>Hinweise

Beachten Sie, dass diese API keinen Fehler oder eine Warnung zurück gibt, wenn der Ausgabepuffer zu klein ist, um die vollständige Liste der Dateien zu akzeptieren, die Teil des Sicherungsdateisets sein sollten.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[API-Klasse](./api-class.md)

[API-Member](./api-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
