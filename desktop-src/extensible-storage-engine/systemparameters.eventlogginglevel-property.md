---
description: Weitere Informationen finden Sie in der System Parameters. eventlogginglevel-Eigenschaft.
title: System Parameters. eventlogginglevel-Eigenschaft
TOCTitle: 'EventLoggingLevel property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.EventLoggingLevel
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.eventlogginglevel(v=EXCHG.10)
ms:contentKeyID: 55104119
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.EventLoggingLevel
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.set_EventLoggingLevel
- Microsoft.Isam.Esent.Interop.SystemParameters.EventLoggingLevel
- Microsoft.Isam.Esent.Interop.SystemParameters.get_EventLoggingLevel
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6e70ef2c0adff6982a34c8e11cc2140f51229299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350408"
---
# <a name="systemparameterseventlogginglevel-property"></a><span data-ttu-id="c9e0e-103">System Parameters. eventlogginglevel-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c9e0e-103">SystemParameters.EventLoggingLevel property</span></span>

<span data-ttu-id="c9e0e-104">Ruft die Detailebene von EventLog-Meldungen ab, die von der Datenbank-Engine an das Ereignisprotokoll ausgegeben werden, oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="c9e0e-104">Gets or sets the detail level of eventlog messages that are emitted to the eventlog by the database engine.</span></span> <span data-ttu-id="c9e0e-105">Höhere Zahlen führen zu ausführlicheren Ereignisprotokoll Meldungen.</span><span class="sxs-lookup"><span data-stu-id="c9e0e-105">Higher numbers will result in more detailed eventlog messages.</span></span>

<span data-ttu-id="c9e0e-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c9e0e-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c9e0e-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c9e0e-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c9e0e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9e0e-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Property EventLoggingLevel As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.EventLoggingLevel

SystemParameters.EventLoggingLevel = value
```

``` csharp
public static int EventLoggingLevel { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="c9e0e-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c9e0e-109">Property value</span></span>

<span data-ttu-id="c9e0e-110">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="c9e0e-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="c9e0e-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9e0e-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c9e0e-112">Referenz</span><span class="sxs-lookup"><span data-stu-id="c9e0e-112">Reference</span></span>

[<span data-ttu-id="c9e0e-113">SystemParameters-Klasse</span><span class="sxs-lookup"><span data-stu-id="c9e0e-113">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="c9e0e-114">SystemParameters-Member</span><span class="sxs-lookup"><span data-stu-id="c9e0e-114">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="c9e0e-115">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="c9e0e-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
