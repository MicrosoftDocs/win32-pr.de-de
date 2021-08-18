---
description: 'Weitere Informationen finden Sie unter: Api.JetGetTruncateLogInfoInstance-Methode'
title: Api.JetGetTruncateLogInfoInstance-Methode
TOCTitle: 'JetGetTruncateLogInfoInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTruncateLogInfoInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String@,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettruncateloginfoinstance(v=EXCHG.10)
ms:contentKeyID: 55100743
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetTruncateLogInfoInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTruncateLogInfoInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1a0e96bd52b7a6ac196289d554c7376790ceb544823235caf5fd99e4fd5da5e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978230"
---
# <a name="apijetgettruncateloginfoinstance-method"></a>Api.JetGetTruncateLogInfoInstance-Methode

Wird während einer Sicherung verwendet, die von [JetBeginExternalBackupInstance(JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md) initiiert wurde, um eine Instanz nach den Namen der Transaktionsprotokolldateien abfragt, die nach erfolgreichem Abschluss der Sicherung sicher gelöscht werden können.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetGetTruncateLogInfoInstance ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef files As String, _
    maxChars As Integer, _
    <OutAttribute> ByRef actualChars As Integer _
)
'Usage
Dim instance As JET_INSTANCE
Dim files As String
Dim maxChars As Integer
Dim actualChars As IntegerApi.JetGetTruncateLogInfoInstance(instance, _
    files, maxChars, actualChars)
```

``` csharp
public static void JetGetTruncateLogInfoInstance(
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
    
    Gibt eine Liste der auf NULL beendeten Zeichenfolgen zurück, die den Satz von Datenbankprotokolldateien beschreiben, die nach Abschluss der Sicherung sicher gelöscht werden können. Die Liste der in diesem Puffer zurückgegebenen Zeichenfolgen hat das gleiche Format wie eine mehrzeichenfolge, die von der Registrierung verwendet wird. Jede auf NULL endende Zeichenfolge wird nacheinander zurückgegeben, gefolgt von einem abschließenden NULL-Abschlusszeichen.

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

#### <a name="reference"></a>Verweis

[API-Klasse](./api-class.md)

[API-Member](./api-members.md)

[Microsoft.Isam.Esent.Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
