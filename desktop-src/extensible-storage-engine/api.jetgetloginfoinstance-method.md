---
description: Weitere Informationen finden Sie in der API. jetgetloginfoinstance-Methode.
title: API. jetgetloginfoinstance-Methode
TOCTitle: 'JetGetLogInfoInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetLogInfoInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String@,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetloginfoinstance(v=EXCHG.10)
ms:contentKeyID: 55100726
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetLogInfoInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetLogInfoInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 85e252b74c47d3274fc83af59e3fb571906219fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344418"
---
# <a name="apijetgetloginfoinstance-method"></a>API. jetgetloginfoinstance-Methode

Wird bei einer von [jetbeginexternalbackupinstance initiierten Sicherung (JET_INSTANCE, beginexternalbackupgrbit)](./api.jetbeginexternalbackupinstance-method.md) verwendet, um eine Instanz für die Namen von datenbankpatchdateien und Protokolldateien abzufragen, die Teil der Sicherungsdatei Gruppe werden sollen. Diese Dateien können anschließend mit [jetopenfileinstance (JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md) geöffnet und mit [jetreadfileinstance (JET_INSTANCE, JET_HANDLE, \[ \] , Int32, Int32)](./api.jetreadfileinstance-method.md)gelesen werden.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Shared Sub JetGetLogInfoInstance ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef files As String, _
    maxChars As Integer, _
    <OutAttribute> ByRef actualChars As Integer _
)
'Usage
Dim instance As JET_INSTANCE
Dim files As String
Dim maxChars As Integer
Dim actualChars As IntegerApi.JetGetLogInfoInstance(instance, _
    files, maxChars, actualChars)
```

``` csharp
public static void JetGetLogInfoInstance(
    JET_INSTANCE instance,
    out string files,
    int maxChars,
    out int actualChars
)
```

#### <a name="parameters"></a>Parameter

  - instance  
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Die-Instanz, für die die Informationen zu erhalten sind.

<!-- end list -->

  - files  
    Typ: [System. String](/dotnet/api/system.string)  
    
    Gibt eine Liste von null-terminierten Zeichen folgen zurück, die den Satz von datenbankpatchdateien und Protokolldateien beschreiben, die Teil des Sicherungsdatei Satzes sein sollen. Die Liste der in diesem Puffer zurückgegebenen Zeichen folgen weist das gleiche Format auf wie eine von der Registrierung verwendete Multizeichenfolge. Jede NULL terminierte Zeichenfolge wird nacheinander zurückgegeben, gefolgt von einem abschließenden NULL-Terminator.

<!-- end list -->

  - maxChars  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Maximale Anzahl der abzurufenden Zeichen.

<!-- end list -->

  - actualchars  
    Typ: [System. Int32](/dotnet/api/system.int32)  
    
    Die tatsächliche Größe der Datei Liste. Wenn dieser Wert größer als maxChars ist, wurde die Liste abgeschnitten.

## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass diese API keinen Fehler oder keine Warnung zurückgibt, wenn der Ausgabepuffer zu klein ist, um die vollständige Liste der Dateien zu akzeptieren, die Bestandteil des Sicherungsdatei Satzes sein sollten.

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[API-Klasse](./api-class.md)

[API-Mitglieder](./api-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
