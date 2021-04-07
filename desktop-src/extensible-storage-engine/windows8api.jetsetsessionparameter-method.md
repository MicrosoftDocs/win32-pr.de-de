---
description: 'Weitere Informationen finden Sie hier: Windows8Api. jetabzessionparameter-Methode'
title: Windows8Api. jetsezessionparameter-Methode (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'JetSetSessionParameter method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetSetSessionParameter(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam,System.Byte[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetsetsessionparameter(v=EXCHG.10)
ms:contentKeyID: 55104461
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetSetSessionParameter
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetSetSessionParameter
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b73331c765e1f8026b39c28dde5268417601663c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863299"
---
# <a name="windows8apijetsetsessionparameter-method"></a><span data-ttu-id="219ea-103">Windows8Api. jetabzessionparameter-Methode</span><span class="sxs-lookup"><span data-stu-id="219ea-103">Windows8Api.JetSetSessionParameter method</span></span>

<span data-ttu-id="219ea-104">Legt einen Parameter für den bereitgestellten Sitzungszustand fest, der für die Lebensdauer dieser Sitzung oder bis zur zurück Setzung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="219ea-104">Sets a parameter on the provided session state, used for the lifetime of this session or until reset.</span></span>

<span data-ttu-id="219ea-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="219ea-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="219ea-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="219ea-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="219ea-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="219ea-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetSessionParameter ( _
    sesid As JET_SESID, _
    sesparamid As JET_sesparam, _
    data As Byte(), _
    dataSize As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim sesparamid As JET_sesparam
Dim data As Byte()
Dim dataSize As IntegerWindows8Api.JetSetSessionParameter(sesid, _
    sesparamid, data, dataSize)
```

``` csharp
public static void JetSetSessionParameter(
    JET_SESID sesid,
    JET_sesparam sesparamid,
    byte[] data,
    int dataSize
)
```

#### <a name="parameters"></a><span data-ttu-id="219ea-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="219ea-108">Parameters</span></span>

  - <span data-ttu-id="219ea-109">-sid</span><span class="sxs-lookup"><span data-stu-id="219ea-109">sesid</span></span>  
    <span data-ttu-id="219ea-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="219ea-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="219ea-111">Die Sitzung, für die der Parameter festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="219ea-111">The session to set the parameter on.</span></span>

<!-- end list -->

  - <span data-ttu-id="219ea-112">sesparamid</span><span class="sxs-lookup"><span data-stu-id="219ea-112">sesparamid</span></span>  
    <span data-ttu-id="219ea-113">Typ: [Microsoft.ISAM.ESENT.Interop.Windows8.JET_sesparam](./jet-sesparam-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="219ea-113">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam](./jet-sesparam-enumeration.md)</span></span>  
    
    <span data-ttu-id="219ea-114">Die ID des festzulegenden Sitzungs Parameters.</span><span class="sxs-lookup"><span data-stu-id="219ea-114">The ID of the session parameter to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="219ea-115">Daten</span><span class="sxs-lookup"><span data-stu-id="219ea-115">data</span></span>  
    <span data-ttu-id="219ea-116">Sorte \[\]</span><span class="sxs-lookup"><span data-stu-id="219ea-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="219ea-117">Die in diesem Sitzungs Parameter festzulegenden Daten.</span><span class="sxs-lookup"><span data-stu-id="219ea-117">Data to set in this session parameter.</span></span>

<!-- end list -->

  - <span data-ttu-id="219ea-118">dataSize</span><span class="sxs-lookup"><span data-stu-id="219ea-118">dataSize</span></span>  
    <span data-ttu-id="219ea-119">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="219ea-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="219ea-120">Größe der bereitgestellten Daten.</span><span class="sxs-lookup"><span data-stu-id="219ea-120">Size of the data provided.</span></span>

## <a name="see-also"></a><span data-ttu-id="219ea-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="219ea-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="219ea-122">Referenz</span><span class="sxs-lookup"><span data-stu-id="219ea-122">Reference</span></span>

[<span data-ttu-id="219ea-123">Windows8Api-Klasse</span><span class="sxs-lookup"><span data-stu-id="219ea-123">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="219ea-124">Windows8Api-Member</span><span class="sxs-lookup"><span data-stu-id="219ea-124">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="219ea-125">Microsoft. ISAM. ESENT. Interop. Windows8-Namespace</span><span class="sxs-lookup"><span data-stu-id="219ea-125">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
