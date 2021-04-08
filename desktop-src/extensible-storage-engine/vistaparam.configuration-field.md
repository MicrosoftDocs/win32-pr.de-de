---
description: 'Weitere Informationen finden Sie hier: VistaParam.Configurationsfeld'
title: VistaParam.Configurationsfeld (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: Configuration field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Vista.VistaParam.Configuration
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaparam.configuration(v=EXCHG.10)
ms:contentKeyID: 55104229
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.Configuration
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.Configuration
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b330afb7158c616ba7bb9683a7bbe226d8d63542
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749696"
---
# <a name="vistaparamconfiguration-field"></a><span data-ttu-id="f6814-103">VistaParam.Configurationsfeld</span><span class="sxs-lookup"><span data-stu-id="f6814-103">VistaParam.Configuration field</span></span>

<span data-ttu-id="f6814-104">Dieser Parameter macht mehrere Sätze von Standardwerten für den gesamten Satz von Systemparametern verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f6814-104">This parameter exposes multiple sets of default values for the entire set of system parameters.</span></span> <span data-ttu-id="f6814-105">Wenn dieser Parameter auf eine bestimmte Konfiguration festgelegt ist, werden alle Systemparameter Werte auf ihre Standardwerte für diese Konfiguration zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="f6814-105">When this parameter is set to a specific configuration, all system parameter values are reset to their default values for that configuration.</span></span> <span data-ttu-id="f6814-106">Wenn die Konfiguration für eine bestimmte Instanz festgelegt ist, werden die globalen Systemparameter nicht auf ihre Standardwerte zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="f6814-106">If the configuration is set for a specific instance then global system parameters will not be reset to their default values.</span></span> <span data-ttu-id="f6814-107">Kleine Konfiguration (0): die Datenbank-Engine ist für die Speichernutzung optimiert.</span><span class="sxs-lookup"><span data-stu-id="f6814-107">Small Configuration (0): The database engine is optimized for memory use.</span></span> <span data-ttu-id="f6814-108">Legacy Konfiguration (1): die Datenbank-Engine verfügt über die herkömmlichen Standardeinstellungen.</span><span class="sxs-lookup"><span data-stu-id="f6814-108">Legacy Configuration (1): The database engine has its traditional defaults.</span></span>

<span data-ttu-id="f6814-109">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f6814-109">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="f6814-110">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f6814-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f6814-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6814-111">Syntax</span></span>

``` vb
'Declaration
Public Const Configuration As JET_param
'Usage
Dim value As JET_param

value = VistaParam.Configuration
```

``` csharp
public const JET_param Configuration
```

## <a name="see-also"></a><span data-ttu-id="f6814-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6814-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f6814-113">Referenz</span><span class="sxs-lookup"><span data-stu-id="f6814-113">Reference</span></span>

[<span data-ttu-id="f6814-114">Vistaparam-Klasse</span><span class="sxs-lookup"><span data-stu-id="f6814-114">VistaParam class</span></span>](./vistaparam-class.md)

[<span data-ttu-id="f6814-115">Vistaparam-Member</span><span class="sxs-lookup"><span data-stu-id="f6814-115">VistaParam members</span></span>](./vistaparam-members.md)

[<span data-ttu-id="f6814-116">Microsoft. ISAM. ESENT. Interop. Vista-Namespace</span><span class="sxs-lookup"><span data-stu-id="f6814-116">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
