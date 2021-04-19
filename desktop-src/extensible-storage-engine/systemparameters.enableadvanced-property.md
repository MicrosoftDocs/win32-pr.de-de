---
description: Weitere Informationen finden Sie in der System Parameters. enableadvanced-Eigenschaft.
title: System Parameters. enableadvanced (Eigenschaft)
TOCTitle: 'EnableAdvanced property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.EnableAdvanced
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.enableadvanced(v=EXCHG.10)
ms:contentKeyID: 55104116
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.EnableAdvanced
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.set_EnableAdvanced
- Microsoft.Isam.Esent.Interop.SystemParameters.get_EnableAdvanced
- Microsoft.Isam.Esent.Interop.SystemParameters.EnableAdvanced
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e311685bf5ef436be11d4593523aceee73b955b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362667"
---
# <a name="systemparametersenableadvanced-property"></a><span data-ttu-id="e717e-103">System Parameters. enableadvanced (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e717e-103">SystemParameters.EnableAdvanced property</span></span>

<span data-ttu-id="e717e-104">Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob die Datenbank-Engine Änderungen an einer Teilmenge der Systemparameter akzeptiert oder ablehnt.</span><span class="sxs-lookup"><span data-stu-id="e717e-104">Gets or sets a value indicating whether the database engine accepts or rejects changes to a subset of the system parameters.</span></span> <span data-ttu-id="e717e-105">Dieser Parameter wird zusammen mit der [Konfiguration](./systemparameters.configuration-property.md) verwendet, um zu verhindern, dass einige Systemparameter aus den Standardeinstellungen der ausgewählten Konfiguration entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="e717e-105">This parameter is used in conjunction with [Configuration](./systemparameters.configuration-property.md) to prevent some system parameters from being set away from the selected configuration's defaults.</span></span> <span data-ttu-id="e717e-106">Unterstützt unter Windows Vista und up.</span><span class="sxs-lookup"><span data-stu-id="e717e-106">Supported on Windows Vista and up.</span></span> <span data-ttu-id="e717e-107">Wird unter Windows XP und Windows Server 2003 ignoriert.</span><span class="sxs-lookup"><span data-stu-id="e717e-107">Ignored on Windows XP and Windows Server 2003.</span></span>

<span data-ttu-id="e717e-108">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e717e-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e717e-109">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e717e-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e717e-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="e717e-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Property EnableAdvanced As Boolean
    Get
    Set
'Usage
Dim value As Boolean

value = SystemParameters.EnableAdvanced

SystemParameters.EnableAdvanced = value
```

``` csharp
public static bool EnableAdvanced { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="e717e-111">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e717e-111">Property value</span></span>

<span data-ttu-id="e717e-112">Typ: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="e717e-112">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  

## <a name="see-also"></a><span data-ttu-id="e717e-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e717e-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e717e-114">Referenz</span><span class="sxs-lookup"><span data-stu-id="e717e-114">Reference</span></span>

[<span data-ttu-id="e717e-115">SystemParameters-Klasse</span><span class="sxs-lookup"><span data-stu-id="e717e-115">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="e717e-116">SystemParameters-Member</span><span class="sxs-lookup"><span data-stu-id="e717e-116">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="e717e-117">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="e717e-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
