---
title: Inapserverinfo getnapserverinfo-Methode (napservermanagement. h)
description: Ruft Informationen zum NAP-Server ab.
ms.assetid: 02f7ce40-3443-4263-86b2-4276cbc7b694
keywords:
- Getnapserverinfo-Methode NAP
- Getnapserverinfo-Methode NAP, inapserverinfo-Schnittstelle
- Inapserverinfo-Schnittstelle NAP, getnapserverinfo-Methode
topic_type:
- apiref
api_name:
- INapServerInfo.GetNapServerInfo
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b182b9e1a5c8d7974128b062fd284c5af3f060f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743888"
---
# <a name="inapserverinfogetnapserverinfo-method"></a><span data-ttu-id="9d71a-106">Inapserverinfo:: getnapserverinfo-Methode</span><span class="sxs-lookup"><span data-stu-id="9d71a-106">INapServerInfo::GetNapServerInfo method</span></span>

> [!Note]  
> <span data-ttu-id="9d71a-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9d71a-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="9d71a-108">Mit der Methode **inapserverinfo:: getnapserverinfo** werden Informationen zum NAP-Server abgerufen.</span><span class="sxs-lookup"><span data-stu-id="9d71a-108">The **INapServerInfo::GetNapServerInfo** method retrieves information about the NAP server.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d71a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d71a-109">Syntax</span></span>


```C++
HRESULT GetNapServerInfo(
  [out] CountedString **serverName,
  [out] CountedString **serverDescription,
  [out] CountedString **protocolVersion
);
```



## <a name="parameters"></a><span data-ttu-id="9d71a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d71a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d71a-111">*Servername* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9d71a-111">*serverName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d71a-112">Ein Zeiger auf einen Zeiger auf eine [**zählstring**](/windows/win32/api/naptypes/ns-naptypes-countedstring) -Struktur, die den Servernamen enthält.</span><span class="sxs-lookup"><span data-stu-id="9d71a-112">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the server name.</span></span>

</dd> <dt>

<span data-ttu-id="9d71a-113">*Server Beschreibung* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9d71a-113">*serverDescription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d71a-114">Ein Zeiger auf einen Zeiger auf eine [**zählstring**](/windows/win32/api/naptypes/ns-naptypes-countedstring) -Struktur, die die Server Beschreibung enthält.</span><span class="sxs-lookup"><span data-stu-id="9d71a-114">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the server description.</span></span>

</dd> <dt>

<span data-ttu-id="9d71a-115">*ProtocolVersion* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9d71a-115">*protocolVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d71a-116">Ein Zeiger auf einen Zeiger auf eine [**zählstring**](/windows/win32/api/naptypes/ns-naptypes-countedstring) -Struktur, die die Protokollversion enthält.</span><span class="sxs-lookup"><span data-stu-id="9d71a-116">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the protocol version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d71a-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9d71a-117">Return value</span></span>

<span data-ttu-id="9d71a-118">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9d71a-118">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="9d71a-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9d71a-119">Return code</span></span>                                                                                     | <span data-ttu-id="9d71a-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9d71a-120">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="9d71a-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9d71a-121"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="9d71a-122">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="9d71a-122">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="9d71a-123"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="9d71a-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="9d71a-124">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="9d71a-124">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="9d71a-125"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="9d71a-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="9d71a-126">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9d71a-126">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9d71a-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9d71a-127">Requirements</span></span>



| <span data-ttu-id="9d71a-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d71a-128">Requirement</span></span> | <span data-ttu-id="9d71a-129">Wert</span><span class="sxs-lookup"><span data-stu-id="9d71a-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d71a-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9d71a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9d71a-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9d71a-131">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="9d71a-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9d71a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9d71a-133">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d71a-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9d71a-134">Header</span><span class="sxs-lookup"><span data-stu-id="9d71a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d71a-135"><dt>Napservermanagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d71a-135"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="9d71a-136">IDL</span><span class="sxs-lookup"><span data-stu-id="9d71a-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9d71a-137"><dt>Napservermanagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9d71a-137"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="9d71a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="9d71a-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d71a-139"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d71a-139"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="9d71a-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d71a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d71a-141">**Inapserverinfo**</span><span class="sxs-lookup"><span data-stu-id="9d71a-141">**INapServerInfo**</span></span>](inapserverinfo.md)
</dt> <dt>

[<span data-ttu-id="9d71a-142">**"Zählzeichen Folge"**</span><span class="sxs-lookup"><span data-stu-id="9d71a-142">**CountedString**</span></span>](/windows/win32/api/naptypes/ns-naptypes-countedstring)
</dt> </dl>

 

 





