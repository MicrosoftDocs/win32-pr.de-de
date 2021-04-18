---
description: 'Weitere Informationen finden Sie hier: Server2003Param. Alternative datasedatabaserecoverypath-Feld'
title: Server2003Param. alternativen datasedatabaserecoverypath-Feld (Microsoft. ISAM. ESENT. Interop. Server2003)
TOCTitle: AlternateDatabaseRecoveryPath field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Server2003.Server2003Param.AlternateDatabaseRecoveryPath
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003param.alternatedatabaserecoverypath(v=EXCHG.10)
ms:contentKeyID: 55104217
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Param.AlternateDatabaseRecoveryPath
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Param.AlternateDatabaseRecoveryPath
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 770ac27596b4385d0012cb65847754b4deb7e9fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343360"
---
# <a name="server2003paramalternatedatabaserecoverypath-field"></a><span data-ttu-id="fcb92-103">Server2003Param. Alternative datasedatabaserecoverypath-Feld</span><span class="sxs-lookup"><span data-stu-id="fcb92-103">Server2003Param.AlternateDatabaseRecoveryPath field</span></span>

<span data-ttu-id="fcb92-104">Der vollständige Pfad zu jeder Datenbank wird zur Laufzeit in den Transaktions Protokollen beibehalten.</span><span class="sxs-lookup"><span data-stu-id="fcb92-104">The full path to each database is persisted in the transaction logs at run time.</span></span> <span data-ttu-id="fcb92-105">Normalerweise müssen diese Datenbanken am ursprünglichen Speicherort verbleiben, damit die Transaktions Wiedergabe ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="fcb92-105">Ordinarily, these databases must remain at the original location for transaction replay to function correctly.</span></span> <span data-ttu-id="fcb92-106">Dieser Parameter kann verwendet werden, um die Wiederherstellung von abstürzen oder einen Wiederherstellungs Vorgang zum Suchen nach den Datenbanken zu erzwingen, auf die im Transaktionsprotokoll im angegebenen Ordner verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="fcb92-106">This parameter can be used to force crash recovery or a restore operation to look for the databases referenced in the transaction log in the specified folder.</span></span>

<span data-ttu-id="fcb92-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fcb92-107">**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span></span>  
<span data-ttu-id="fcb92-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="fcb92-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fcb92-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="fcb92-109">Syntax</span></span>

``` vb
'Declaration
Public Const AlternateDatabaseRecoveryPath As JET_param
'Usage
Dim value As JET_param

value = Server2003Param.AlternateDatabaseRecoveryPath
```

``` csharp
public const JET_param AlternateDatabaseRecoveryPath
```

## <a name="see-also"></a><span data-ttu-id="fcb92-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fcb92-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fcb92-111">Referenz</span><span class="sxs-lookup"><span data-stu-id="fcb92-111">Reference</span></span>

[<span data-ttu-id="fcb92-112">Server2003Param-Klasse</span><span class="sxs-lookup"><span data-stu-id="fcb92-112">Server2003Param class</span></span>](./server2003param-class.md)

[<span data-ttu-id="fcb92-113">Server2003Param-Member</span><span class="sxs-lookup"><span data-stu-id="fcb92-113">Server2003Param members</span></span>](./server2003param-members.md)

[<span data-ttu-id="fcb92-114">Microsoft. ISAM. ESENT. Interop. Server2003-Namespace</span><span class="sxs-lookup"><span data-stu-id="fcb92-114">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
