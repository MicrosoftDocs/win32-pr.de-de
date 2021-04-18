---
description: 'Weitere Informationen finden Sie unter: instanceparameters. datasedatabaserecoverydirectory-Eigenschaft'
title: Instanceparameters. datasedatabaserecoverydirectory (Eigenschaft)
TOCTitle: 'AlternateDatabaseRecoveryDirectory property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.AlternateDatabaseRecoveryDirectory
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.alternatedatabaserecoverydirectory(v=EXCHG.10)
ms:contentKeyID: 55107440
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.AlternateDatabaseRecoveryDirectory
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.AlternateDatabaseRecoveryDirectory
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_AlternateDatabaseRecoveryDirectory
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_AlternateDatabaseRecoveryDirectory
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 70e08c65027806990ab511ef8561b41551f0ac2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354543"
---
# <a name="instanceparametersalternatedatabaserecoverydirectory-property"></a><span data-ttu-id="cd08b-103">Instanceparameters. datasedatabaserecoverydirectory (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="cd08b-103">InstanceParameters.AlternateDatabaseRecoveryDirectory property</span></span>

<span data-ttu-id="cd08b-104">Ruft den relativen oder absoluten Dateisystempfad des Ordners ab, in dem die Absturz Wiederherstellung oder ein Wiederherstellungs Vorgang die Datenbanken finden kann, auf die im Transaktionsprotokoll im angegebenen Ordner verwiesen wird, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="cd08b-104">Gets or sets the relative or absolute file system path of the a folder where crash recovery or a restore operation can find the databases referenced in the transaction log in the specified folder.</span></span>

<span data-ttu-id="cd08b-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cd08b-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="cd08b-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="cd08b-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cd08b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd08b-107">Syntax</span></span>

``` vb
'Declaration
Public Property AlternateDatabaseRecoveryDirectory As String
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As String

value = instance.AlternateDatabaseRecoveryDirectory

instance.AlternateDatabaseRecoveryDirectory = value
```

``` csharp
public string AlternateDatabaseRecoveryDirectory { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="cd08b-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="cd08b-108">Property value</span></span>

<span data-ttu-id="cd08b-109">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="cd08b-109">Type: [System.String](/dotnet/api/system.string)</span></span>  

## <a name="remarks"></a><span data-ttu-id="cd08b-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cd08b-110">Remarks</span></span>

<span data-ttu-id="cd08b-111">Dieser Parameter wird unter Windows XP ignoriert.</span><span class="sxs-lookup"><span data-stu-id="cd08b-111">This parameter is ignored on Windows XP.</span></span>

## <a name="see-also"></a><span data-ttu-id="cd08b-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd08b-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cd08b-113">Referenz</span><span class="sxs-lookup"><span data-stu-id="cd08b-113">Reference</span></span>

[<span data-ttu-id="cd08b-114">Instanceparameters-Klasse</span><span class="sxs-lookup"><span data-stu-id="cd08b-114">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="cd08b-115">Instanceparameters-Elemente</span><span class="sxs-lookup"><span data-stu-id="cd08b-115">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="cd08b-116">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="cd08b-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
