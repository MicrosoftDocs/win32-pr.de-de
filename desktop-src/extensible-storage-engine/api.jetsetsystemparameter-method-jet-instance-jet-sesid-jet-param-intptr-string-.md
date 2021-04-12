---
description: 'Weitere Informationen finden Sie unter: API. jetsetsystemparameter-Methode (JET_INSTANCE, JET_SESID, JET_param, IntPtr, String)'
title: API. jetsetsystemparameter-Methode (JET_INSTANCE, JET_SESID, JET_param, IntPtr, String)
TOCTitle: JetSetSystemParameter method (JET_INSTANCE, JET_SESID, JET_param, IntPtr, String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetSystemParameter(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_param,System.IntPtr,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetsystemparameter(v=EXCHG.10)
ms:contentKeyID: 55100822
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetSystemParameter
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 72a92ea3d6b6d4b828e409cd08b896f54c4aa053
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217280"
---
# <a name="apijetsetsystemparameter-method-jet_instance-jet_sesid-jet_param-intptr-string"></a><span data-ttu-id="480ca-103">API. jetsetsystemparameter-Methode (JET_INSTANCE, JET_SESID, JET_param, IntPtr, String)</span><span class="sxs-lookup"><span data-stu-id="480ca-103">Api.JetSetSystemParameter method (JET_INSTANCE, JET_SESID, JET_param, IntPtr, String)</span></span>

<span data-ttu-id="480ca-104">Legt Daten Bank Konfigurationsoptionen fest.</span><span class="sxs-lookup"><span data-stu-id="480ca-104">Sets database configuration options.</span></span>

<span data-ttu-id="480ca-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="480ca-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="480ca-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="480ca-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="480ca-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="480ca-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetSetSystemParameter ( _
    instance As JET_INSTANCE, _
    sesid As JET_SESID, _
    paramid As JET_param, _
    paramValue As IntPtr, _
    paramString As String _
) As JET_wrn
'Usage
Dim instance As JET_INSTANCE
Dim sesid As JET_SESID
Dim paramid As JET_param
Dim paramValue As IntPtr
Dim paramString As String
Dim returnValue As JET_wrn

returnValue = Api.JetSetSystemParameter(instance, _
    sesid, paramid, paramValue, paramString)
```

``` csharp
public static JET_wrn JetSetSystemParameter(
    JET_INSTANCE instance,
    JET_SESID sesid,
    JET_param paramid,
    IntPtr paramValue,
    string paramString
)
```

#### <a name="parameters"></a><span data-ttu-id="480ca-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="480ca-108">Parameters</span></span>

  - <span data-ttu-id="480ca-109">instance</span><span class="sxs-lookup"><span data-stu-id="480ca-109">instance</span></span>  
    <span data-ttu-id="480ca-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="480ca-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="480ca-111">Die Instanz, für die die Option festgelegt werden soll, oder [null](./jet-instance.nil-property.md) , um die Option für alle Instanzen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="480ca-111">The instance to set the option on or [Nil](./jet-instance.nil-property.md) to set the option on all instances.</span></span>

<!-- end list -->

  - <span data-ttu-id="480ca-112">-sid</span><span class="sxs-lookup"><span data-stu-id="480ca-112">sesid</span></span>  
    <span data-ttu-id="480ca-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="480ca-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="480ca-114">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="480ca-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="480ca-115">paramid</span><span class="sxs-lookup"><span data-stu-id="480ca-115">paramid</span></span>  
    <span data-ttu-id="480ca-116">Typ: [Microsoft.ISAM.ESENT.Interop.JET_param](./jet-param-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="480ca-116">Type: [Microsoft.Isam.Esent.Interop.JET_param](./jet-param-enumeration.md)</span></span>  
    
    <span data-ttu-id="480ca-117">Der festzulegende Parameter.</span><span class="sxs-lookup"><span data-stu-id="480ca-117">The parameter to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="480ca-118">angegebene paramValue</span><span class="sxs-lookup"><span data-stu-id="480ca-118">paramValue</span></span>  
    <span data-ttu-id="480ca-119">Typ: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="480ca-119">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="480ca-120">Der Wert des festzulegenden Parameters, wenn der Parameter ein ganzzahliger Typ ist.</span><span class="sxs-lookup"><span data-stu-id="480ca-120">The value of the parameter to set, if the parameter is an integer type.</span></span>

<!-- end list -->

  - <span data-ttu-id="480ca-121">paramString</span><span class="sxs-lookup"><span data-stu-id="480ca-121">paramString</span></span>  
    <span data-ttu-id="480ca-122">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="480ca-122">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="480ca-123">Der Wert des festzulegenden Parameters, wenn der Parameter vom Typ String ist.</span><span class="sxs-lookup"><span data-stu-id="480ca-123">The value of the parameter to set, if the parameter is a string type.</span></span>

#### <a name="return-value"></a><span data-ttu-id="480ca-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="480ca-124">Return value</span></span>

<span data-ttu-id="480ca-125">Typ: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="480ca-125">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="480ca-126">Ein ESENT-Warnungs Code.</span><span class="sxs-lookup"><span data-stu-id="480ca-126">An ESENT warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="480ca-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="480ca-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="480ca-128">Referenz</span><span class="sxs-lookup"><span data-stu-id="480ca-128">Reference</span></span>

[<span data-ttu-id="480ca-129">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="480ca-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="480ca-130">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="480ca-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="480ca-131">Jetsetsystemparameter-Überladung</span><span class="sxs-lookup"><span data-stu-id="480ca-131">JetSetSystemParameter overload</span></span>](./api.jetsetsystemparameter-method.md)

[<span data-ttu-id="480ca-132">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="480ca-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
