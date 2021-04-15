---
title: Initialize-Methode von inapenforcementclientconnection (napforcementclient. h)
description: Initialisiert die Client Verbindung.
ms.assetid: da72bfc3-9551-4fb0-b9a5-2931c14f618f
keywords:
- Methode "NAP initialisieren"
- Initialize-Methode NAP, inapenforcementclientconnection-Schnittstelle
- Inapenforcementclientconnection-Schnittstelle NAP, Initialize-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.Initialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b51f12025bbddb8a9e795a97f2ed443344327a17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475993"
---
# <a name="inapenforcementclientconnectioninitialize-method"></a><span data-ttu-id="3410c-106">Inapenforcementclientconnection:: Initialize-Methode</span><span class="sxs-lookup"><span data-stu-id="3410c-106">INapEnforcementClientConnection::Initialize method</span></span>

> [!Note]  
> <span data-ttu-id="3410c-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3410c-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="3410c-108">Die **inapenforcementclientconnection:: Initialize** -Methode initialisiert die Client Verbindung.</span><span class="sxs-lookup"><span data-stu-id="3410c-108">The **INapEnforcementClientConnection::Initialize** method initializes the client connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="3410c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="3410c-109">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] EnforcementEntityId id
);
```



## <a name="parameters"></a><span data-ttu-id="3410c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3410c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3410c-111">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3410c-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3410c-112">Ein Zeiger auf eine [**enforemententityid**](nap-datatypes.md) , die den Erzwingungs Client identifiziert, der die Verbindung anfordert.</span><span class="sxs-lookup"><span data-stu-id="3410c-112">A pointer to an [**EnforementEntityId**](nap-datatypes.md) that identifies the enforcement client requesting the connection.</span></span> <span data-ttu-id="3410c-113">Dieser Wert wird von NAPAgent während der Verbindungs Erstellung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3410c-113">This value is set by the NapAgent during connection creation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3410c-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3410c-114">Return value</span></span>

<span data-ttu-id="3410c-115">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3410c-115">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="3410c-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="3410c-116">Return code</span></span>                                                                                     | <span data-ttu-id="3410c-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3410c-117">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="3410c-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3410c-118"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="3410c-119">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="3410c-119">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="3410c-120"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="3410c-120"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="3410c-121">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="3410c-121">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="3410c-122"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="3410c-122"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="3410c-123">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3410c-123">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3410c-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3410c-124">Requirements</span></span>



| <span data-ttu-id="3410c-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3410c-125">Requirement</span></span> | <span data-ttu-id="3410c-126">Wert</span><span class="sxs-lookup"><span data-stu-id="3410c-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3410c-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3410c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3410c-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3410c-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3410c-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3410c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3410c-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3410c-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3410c-131">Header</span><span class="sxs-lookup"><span data-stu-id="3410c-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="3410c-132"><dt>Napforcementclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="3410c-132"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="3410c-133">IDL</span><span class="sxs-lookup"><span data-stu-id="3410c-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3410c-134"><dt>Napforcementclient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3410c-134"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="3410c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="3410c-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3410c-136"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3410c-136"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="3410c-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3410c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3410c-138">**Inapenforcementclientconnection**</span><span class="sxs-lookup"><span data-stu-id="3410c-138">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





