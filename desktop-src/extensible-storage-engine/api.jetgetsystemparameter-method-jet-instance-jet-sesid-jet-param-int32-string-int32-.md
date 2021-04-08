---
description: 'Weitere Informationen finden Sie unter: API. jetgetsystemparameter-Methode (JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)'
title: API. jetgetsystemparameter-Methode (JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)
TOCTitle: JetGetSystemParameter method (JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetSystemParameter(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_param,System.Int32@,System.String@,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetsystemparameter(v=EXCHG.10)
ms:contentKeyID: 55100727
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetSystemParameter
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 840c17ef1d74b57b4bee75b9efafe5a314f09a57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862228"
---
# <a name="apijetgetsystemparameter-method-jet_instance-jet_sesid-jet_param-int32-string-int32"></a><span data-ttu-id="2e0ee-103">API. jetgetsystemparameter-Methode (JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-103">Api.JetGetSystemParameter method (JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)</span></span>

<span data-ttu-id="2e0ee-104">Ruft Daten Bank Konfigurationsoptionen ab.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-104">Gets database configuration options.</span></span>

<span data-ttu-id="2e0ee-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2e0ee-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2e0ee-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e0ee-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetGetSystemParameter ( _
    instance As JET_INSTANCE, _
    sesid As JET_SESID, _
    paramid As JET_param, _
    ByRef paramValue As Integer, _
    <OutAttribute> ByRef paramString As String, _
    maxParam As Integer _
) As JET_wrn
'Usage
Dim instance As JET_INSTANCE
Dim sesid As JET_SESID
Dim paramid As JET_param
Dim paramValue As Integer
Dim paramString As String
Dim maxParam As Integer
Dim returnValue As JET_wrn

returnValue = Api.JetGetSystemParameter(instance, _
    sesid, paramid, paramValue, paramString, _
    maxParam)
```

``` csharp
public static JET_wrn JetGetSystemParameter(
    JET_INSTANCE instance,
    JET_SESID sesid,
    JET_param paramid,
    ref int paramValue,
    out string paramString,
    int maxParam
)
```

#### <a name="parameters"></a><span data-ttu-id="2e0ee-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e0ee-108">Parameters</span></span>

  - <span data-ttu-id="2e0ee-109">instance</span><span class="sxs-lookup"><span data-stu-id="2e0ee-109">instance</span></span>  
    <span data-ttu-id="2e0ee-110">Typ: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="2e0ee-111">Die-Instanz, aus der die Optionen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-111">The instance to retrieve the options from.</span></span>

<!-- end list -->

  - <span data-ttu-id="2e0ee-112">-sid</span><span class="sxs-lookup"><span data-stu-id="2e0ee-112">sesid</span></span>  
    <span data-ttu-id="2e0ee-113">Typ: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="2e0ee-114">Die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="2e0ee-115">paramid</span><span class="sxs-lookup"><span data-stu-id="2e0ee-115">paramid</span></span>  
    <span data-ttu-id="2e0ee-116">Typ: [Microsoft.ISAM.ESENT.Interop.JET_param](./jet-param-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-116">Type: [Microsoft.Isam.Esent.Interop.JET_param](./jet-param-enumeration.md)</span></span>  
    
    <span data-ttu-id="2e0ee-117">Der zu Get-Parameter.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-117">The parameter to get.</span></span>

<!-- end list -->

  - <span data-ttu-id="2e0ee-118">angegebene paramValue</span><span class="sxs-lookup"><span data-stu-id="2e0ee-118">paramValue</span></span>  
    <span data-ttu-id="2e0ee-119">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="2e0ee-120">Gibt den Wert des-Parameters zurück, wenn der Wert eine ganze Zahl ist.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-120">Returns the value of the parameter, if the value is an integer.</span></span>

<!-- end list -->

  - <span data-ttu-id="2e0ee-121">paramString</span><span class="sxs-lookup"><span data-stu-id="2e0ee-121">paramString</span></span>  
    <span data-ttu-id="2e0ee-122">Typ: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-122">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="2e0ee-123">Gibt den Wert des-Parameters zurück, wenn der Wert eine Zeichenfolge ist.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-123">Returns the value of the parameter, if the value is a string.</span></span>

<!-- end list -->

  - <span data-ttu-id="2e0ee-124">maxparam</span><span class="sxs-lookup"><span data-stu-id="2e0ee-124">maxParam</span></span>  
    <span data-ttu-id="2e0ee-125">Typ: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="2e0ee-126">Die maximale Größe der Parameter Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-126">The maximum size of the parameter string.</span></span>

#### <a name="return-value"></a><span data-ttu-id="2e0ee-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2e0ee-127">Return value</span></span>

<span data-ttu-id="2e0ee-128">Typ: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="2e0ee-128">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="2e0ee-129">Ein ESENT-Warnungs Code.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-129">An ESENT warning code.</span></span>  

## <a name="remarks"></a><span data-ttu-id="2e0ee-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e0ee-130">Remarks</span></span>

<span data-ttu-id="2e0ee-131">[Errorto String](./jet-param-enumeration.md) übergibt die Fehlernummer im paramValue, weshalb es sich um einen ref-Parameter und nicht um einen out-Parameter handelt.</span><span class="sxs-lookup"><span data-stu-id="2e0ee-131">[ErrorToString](./jet-param-enumeration.md) passes in the error number in the paramValue, which is why it is a ref parameter and not an out parameter.</span></span>

## <a name="see-also"></a><span data-ttu-id="2e0ee-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e0ee-132">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2e0ee-133">Referenz</span><span class="sxs-lookup"><span data-stu-id="2e0ee-133">Reference</span></span>

[<span data-ttu-id="2e0ee-134">API-Klasse</span><span class="sxs-lookup"><span data-stu-id="2e0ee-134">Api class</span></span>](./api-class.md)

[<span data-ttu-id="2e0ee-135">API-Mitglieder</span><span class="sxs-lookup"><span data-stu-id="2e0ee-135">Api members</span></span>](./api-members.md)

[<span data-ttu-id="2e0ee-136">Jetgetsystemparameter-Überladung</span><span class="sxs-lookup"><span data-stu-id="2e0ee-136">JetGetSystemParameter overload</span></span>](./api.jetgetsystemparameter-method.md)

[<span data-ttu-id="2e0ee-137">Microsoft. ISAM. ESENT. Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="2e0ee-137">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
