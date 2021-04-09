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
# <a name="instanceparameterscleanupmismatchedlogfiles-property"></a><span data-ttu-id="5a549-103">Instanceparameters. cleanupmismatchedlogfiles (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5a549-103">InstanceParameters.CleanupMismatchedLogFiles property</span></span>

<span data-ttu-id="5a549-104">Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob jetinit fehlschlägt, wenn die Datenbank-Engine für die Verwendung von Transaktionsprotokoll Dateien auf dem Datenträger konfiguriert ist, die eine andere Größe als die konfigurierte</span><span class="sxs-lookup"><span data-stu-id="5a549-104">Gets or sets a value indicating whether JetInit fails when the database engine is configured to start using transaction log files on disk that are of a different size than what is configured.</span></span> <span data-ttu-id="5a549-105">Normalerweise stellt [jetinit (JET_INSTANCE)](./api.jetinit-method.md) die Datenbanken erfolgreich wieder her, schlägt jedoch mit [logfilesizemismatchdatabaseskonsistente](./jet-err-enumeration.md) fehl, um anzugeben, dass die Protokolldatei Größe falsch konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="5a549-105">Normally, [JetInit(JET_INSTANCE)](./api.jetinit-method.md) will successfully recover the databases but will fail with [LogFileSizeMismatchDatabasesConsistent](./jet-err-enumeration.md) to indicate that the log file size is misconfigured.</span></span> <span data-ttu-id="5a549-106">Wenn dieser Parameter jedoch auf true festgelegt ist, löscht die Datenbank-Engine automatisch alle alten Protokolldateien und startet mithilfe der konfigurierten Protokolldatei Größe einen neuen Satz von Transaktionsprotokoll Dateien.</span><span class="sxs-lookup"><span data-stu-id="5a549-106">However, when this parameter is set to true then the database engine will silently delete all the old log files, start a new set of transaction log files using the configured log file size.</span></span> <span data-ttu-id="5a549-107">Dieser Parameter ist hilfreich, wenn die Anwendung die Größe der Transaktionsprotokoll Datei transparent ändern möchte, aber trotzdem in Aktualisierungs-und Wiederherstellungs Szenarien transparent funktioniert.</span><span class="sxs-lookup"><span data-stu-id="5a549-107">This parameter is useful when the application wishes to transparently change its transaction log file size yet still work transparently in upgrade and restore scenarios.</span></span>

<span data-ttu-id="5a549-108">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5a549-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5a549-109">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5a549-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5a549-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a549-110">Syntax</span></span>

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

#### <a name="property-value"></a><span data-ttu-id="5a549-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="5a549-111">Property value</span></span>

<span data-ttu-id="5a549-112">Typ: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="5a549-112">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  

## <a name="see-also"></a><span data-ttu-id="5a549-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a549-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5a549-114">Referenz</span><span class="sxs-lookup"><span data-stu-id="5a549-114">Reference</span></span>

[<span data-ttu-id="5a549-115">Instanceparameters-Klasse</span><span class="sxs-lookup"><span data-stu-id="5a549-115">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="5a549-116">Instanceparameters-Elemente</span><span class="sxs-lookup"><span data-stu-id="5a549-116">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="5a549-117">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="5a549-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
