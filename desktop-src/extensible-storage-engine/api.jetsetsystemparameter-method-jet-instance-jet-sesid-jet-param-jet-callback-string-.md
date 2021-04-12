---
description: 'Weitere Informationen finden Sie unter: API. jetsetsystemparameter-Methode (JET_INSTANCE, JET_SESID, JET_param, JET_CALLBACK, Zeichenfolge)'
title: API. jetsetsystemparameter-Methode (JET_INSTANCE, JET_SESID, JET_param, JET_CALLBACK, Zeichenfolge)
TOCTitle: JetSetSystemParameter method (JET_INSTANCE, JET_SESID, JET_param, JET_CALLBACK, String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetSystemParameter(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_param,Microsoft.Isam.Esent.Interop.JET_CALLBACK,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetsystemparameter(v=EXCHG.10)
ms:contentKeyID: 55100819
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetSystemParameter
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2d8d9d65af803a011c0a6a79fdaec2fb0a44755b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218810"
---
# <a name="apijetsetsystemparameter-method-jet_instance-jet_sesid-jet_param-jet_callback-string"></a><span data-ttu-id="020f4-103">API. jetsetsystemparameter-Methode (JET_INSTANCE, JET_SESID, JET_param, JET_CALLBACK, Zeichenfolge)</span><span class="sxs-lookup"><span data-stu-id="020f4-103">Api.JetSetSystemParameter method (JET_INSTANCE, JET_SESID, JET_param, JET_CALLBACK, String)</span></span>

<span data-ttu-id="020f4-104">Legt Daten Bank Konfigurationsoptionen fest.</span><span class="sxs-lookup"><span data-stu-id="020f4-104">Sets database configuration options.</span></span>

<span data-ttu-id="020f4-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="020f4-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="020f4-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="020f4-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="020f4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="020f4-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetSetSystemParameter ( _
    instance As JET_INSTANCE, _
    sesid As JET_SESID, _
    paramid As JET_param, _
    paramValue As JET_CALLBACK, _
    paramString As String _
) As JET_wrn
'Usage
Dim instance As JET_INSTANCE
Dim sesid As JET_SESID
Dim paramid As JET_param
Dim paramValue As JET_CALLBACK
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
    JET_CALLBACK paramValue,
    string paramString
)
```

#### <a name="parameters"></a><span data-ttu-id="020f4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="020f4-108">Parameters</span></span>

  - <span data-ttu-id="020f4-109">instance</span><span class="sxs-lookup"><span data-stu-id="020f4-109">instance</span></span>  
    <span data-ttu-id="020f4-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="020f4-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="020f4-111">Die Instanz, für die die Option festgelegt werden soll, oder [null](./jet-instance.nil-property.md) , um die Option für alle Instanzen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="020f4-111">The instance to set the option on or [Nil](./jet-instance.nil-property.md) to set the option on all instances.</span></span>

<!-- end list -->

  - <span data-ttu-id="020f4-112">-sid</span><span class="sxs-lookup"><span data-stu-id="020f4-112">sesid</span></span>  
    <span data-ttu-id="020f4-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="020f4-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="020f4-114">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="020f4-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="020f4-115">paramid</span><span class="sxs-lookup"><span data-stu-id="020f4-115">paramid</span></span>  
    <span data-ttu-id="020f4-116">Typ: [Microsoft.ISAM.ESENT.Interop.JET_param](./jet-param-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="020f4-116">Type: [Microsoft.Isam.Esent.Interop.JET_param](./jet-param-enumeration.md)</span></span>  
    
    <span data-ttu-id="020f4-117">Der festzulegende Parameter.</span><span class="sxs-lookup"><span data-stu-id="020f4-117">The parameter to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="020f4-118">angegebene paramValue</span><span class="sxs-lookup"><span data-stu-id="020f4-118">paramValue</span></span>  
    <span data-ttu-id="020f4-119">Typ: [Microsoft.ISAM.ESENT.Interop.JET_CALLBACK](./jet-callback-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="020f4-119">Type: [Microsoft.Isam.Esent.Interop.JET_CALLBACK](./jet-callback-delegate.md)</span></span>  
    
    <span data-ttu-id="020f4-120">Der Wert des festzulegenden Parameters, wenn der Parameter ein JET_CALLBACK ist.</span><span class="sxs-lookup"><span data-stu-id="020f4-120">The value of the parameter to set, if the parameter is a JET_CALLBACK.</span></span>

<!-- end list -->

  - <span data-ttu-id="020f4-121">paramString</span><span class="sxs-lookup"><span data-stu-id="020f4-121">paramString</span></span>  
    <span data-ttu-id="020f4-122">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="020f4-122">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="020f4-123">Der Wert des festzulegenden Parameters, wenn der Parameter vom Typ String ist.</span><span class="sxs-lookup"><span data-stu-id="020f4-123">The value of the parameter to set, if the parameter is a string type.</span></span>

#### <a name="return-value"></a><span data-ttu-id="020f4-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="020f4-124">Return value</span></span>

<span data-ttu-id="020f4-125">Typ: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="020f4-125">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="020f4-126">Ein ESENT-Warnungs Code.</span><span class="sxs-lookup"><span data-stu-id="020f4-126">An ESENT warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="020f4-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="020f4-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="020f4-128">Referenz</span><span class="sxs-lookup"><span data-stu-id="020f4-128">Reference</span></span>

[<span data-ttu-id="020f4-129">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="020f4-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="020f4-130">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="020f4-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="020f4-131">Jetsetsystemparameter-Überladung</span><span class="sxs-lookup"><span data-stu-id="020f4-131">JetSetSystemParameter overload</span></span>](./api.jetsetsystemparameter-method.md)

[<span data-ttu-id="020f4-132">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="020f4-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
