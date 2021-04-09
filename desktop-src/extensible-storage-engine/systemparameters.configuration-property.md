---
description: 'Weitere Informationen über: SystemParameters.Configurations-Eigenschaft'
title: SystemParameters.Configurationseigenschaft
TOCTitle: 'Configuration property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.Configuration
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.configuration(v=EXCHG.10)
ms:contentKeyID: 55104117
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.Configuration
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.Configuration
- Microsoft.Isam.Esent.Interop.SystemParameters.set_Configuration
- Microsoft.Isam.Esent.Interop.SystemParameters.get_Configuration
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5eaa387f63df1dd91641ff38f2a6f6450629fe99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865603"
---
# <a name="systemparametersconfiguration-property"></a><span data-ttu-id="16665-103">SystemParameters.Configurationseigenschaft</span><span class="sxs-lookup"><span data-stu-id="16665-103">SystemParameters.Configuration property</span></span>

<span data-ttu-id="16665-104">Ruft einen Wert ab, der die Standardwerte für den gesamten Satz von Systemparametern angibt, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="16665-104">Gets or sets a value specifying the default values for the entire set of system parameters.</span></span> <span data-ttu-id="16665-105">Wenn dieser Parameter auf eine bestimmte Konfiguration festgelegt ist, werden alle Systemparameter Werte auf ihre Standardwerte für diese Konfiguration zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="16665-105">When this parameter is set to a specific configuration, all system parameter values are reset to their default values for that configuration.</span></span> <span data-ttu-id="16665-106">Wenn die Konfiguration für eine bestimmte Instanz festgelegt ist, werden die globalen Systemparameter nicht auf ihre Standardwerte zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="16665-106">If the configuration is set for a specific instance then global system parameters will not be reset to their default values.</span></span> <span data-ttu-id="16665-107">Kleine Konfiguration (0): die Datenbank-Engine ist für die Speichernutzung optimiert.</span><span class="sxs-lookup"><span data-stu-id="16665-107">Small Configuration (0): The database engine is optimized for memory use.</span></span> <span data-ttu-id="16665-108">Legacy Konfiguration (1): die Datenbank-Engine verfügt über die herkömmlichen Standardeinstellungen.</span><span class="sxs-lookup"><span data-stu-id="16665-108">Legacy Configuration (1): The database engine has its traditional defaults.</span></span> <span data-ttu-id="16665-109">Unterstützt unter Windows Vista und up.</span><span class="sxs-lookup"><span data-stu-id="16665-109">Supported on Windows Vista and up.</span></span> <span data-ttu-id="16665-110">Wird unter Windows XP und Windows Server 2003 ignoriert.</span><span class="sxs-lookup"><span data-stu-id="16665-110">Ignored on Windows XP and Windows Server 2003.</span></span>

<span data-ttu-id="16665-111">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="16665-111">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="16665-112">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="16665-112">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="16665-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="16665-113">Syntax</span></span>

``` vb
'Declaration
Public Shared Property Configuration As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.Configuration

SystemParameters.Configuration = value
```

``` csharp
public static int Configuration { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="16665-114">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="16665-114">Property value</span></span>

<span data-ttu-id="16665-115">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="16665-115">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="16665-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16665-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="16665-117">Referenz</span><span class="sxs-lookup"><span data-stu-id="16665-117">Reference</span></span>

[<span data-ttu-id="16665-118">SystemParameters-Klasse</span><span class="sxs-lookup"><span data-stu-id="16665-118">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="16665-119">SystemParameters-Member</span><span class="sxs-lookup"><span data-stu-id="16665-119">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="16665-120">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="16665-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
