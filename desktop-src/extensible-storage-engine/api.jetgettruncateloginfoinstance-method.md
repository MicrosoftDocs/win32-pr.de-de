---
description: Weitere Informationen finden Sie in der API. jetgettruneureloginfoinstance-Methode.
title: API. jetgettruneureloginfoinstance-Methode
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
ms.openlocfilehash: fc54d12796a724b382343c4a3514f03102df305f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218471"
---
# <a name="apijetgettruncateloginfoinstance-method"></a>API. jetgettruneureloginfoinstance-Methode

Wird bei einer von [jetbeginexternalbackupinstance initiierten Sicherung (JET_INSTANCE beginexternalbackupgrbit)](./api.jetbeginexternalbackupinstance-method.md) verwendet, um eine Instanz nach den Namen der Transaktionsprotokoll Dateien abzufragen, die nach erfolgreichem Abschluss der Sicherung sicher gelöscht werden können.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

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
    Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Die-Instanz, für die die Informationen zu erhalten sind.

<!-- end list -->

  - files  
    Typ: [System. String](/dotnet/api/system.string)  
    
    Gibt eine Liste von null-terminierten Zeichen folgen zurück, die den Satz von Daten Bank Protokolldateien beschreiben, die nach Abschluss der Sicherung sicher gelöscht werden können. Die Liste der in diesem Puffer zurückgegebenen Zeichen folgen weist das gleiche Format auf wie eine von der Registrierung verwendete Multizeichenfolge. Jede NULL terminierte Zeichenfolge wird nacheinander zurückgegeben, gefolgt von einem abschließenden NULL-Terminator.

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
