---
description: Weitere Informationen finden Sie in der Eigenschaft instanceparameters. cleanupmismatchedlogfiles.
title: Instanceparameters. cleanupmismatchedlogfiles (Eigenschaft)
TOCTitle: 'CleanupMismatchedLogFiles property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.CleanupMismatchedLogFiles
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.cleanupmismatchedlogfiles(v=EXCHG.10)
ms:contentKeyID: 55103296
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.CleanupMismatchedLogFiles
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_CleanupMismatchedLogFiles
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_CleanupMismatchedLogFiles
- Microsoft.Isam.Esent.Interop.InstanceParameters.CleanupMismatchedLogFiles
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0e80bb8877335e26cb233a09b2fa3ec3a6f12615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130557"
---
# <a name="instanceparameterscleanupmismatchedlogfiles-property"></a>Instanceparameters. cleanupmismatchedlogfiles (Eigenschaft)

Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob jetinit fehlschlägt, wenn die Datenbank-Engine für die Verwendung von Transaktionsprotokoll Dateien auf dem Datenträger konfiguriert ist, die eine andere Größe als die konfigurierte Normalerweise stellt [jetinit (JET_INSTANCE)](./api.jetinit-method.md) die Datenbanken erfolgreich wieder her, schlägt jedoch mit [logfilesizemismatchdatabaseskonsistente](./jet-err-enumeration.md) fehl, um anzugeben, dass die Protokolldatei Größe falsch konfiguriert ist. Wenn dieser Parameter jedoch auf true festgelegt ist, löscht die Datenbank-Engine automatisch alle alten Protokolldateien und startet mithilfe der konfigurierten Protokolldatei Größe einen neuen Satz von Transaktionsprotokoll Dateien. Dieser Parameter ist hilfreich, wenn die Anwendung die Größe der Transaktionsprotokoll Datei transparent ändern möchte, aber trotzdem in Aktualisierungs-und Wiederherstellungs Szenarien transparent funktioniert.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property CleanupMismatchedLogFiles As Boolean
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Boolean

value = instance.CleanupMismatchedLogFiles

instance.CleanupMismatchedLogFiles = value
```

``` csharp
public bool CleanupMismatchedLogFiles { get; set; }
```

#### <a name="property-value"></a>Eigenschaftswert

Typ: [System. Boolean](/dotnet/api/system.boolean)  

## <a name="see-also"></a>Siehe auch

#### <a name="reference"></a>Referenz

[Instanceparameters-Klasse](./instanceparameters-class.md)

[Instanceparameters-Elemente](./instanceparameters-members.md)

[Microsoft. ISAM. ESENT. Interop-Namespace](./microsoft.isam.esent.interop-namespace.md)
