---
title: Iconnectionbrokerclient-Schnittstelle (cbclient. h)
description: Stellt die Methoden bereit, die zum Verwenden des Remotedesktopverbindung Broker-Clients erforderlich sind.
ms.assetid: AFFE0157-DEF5-480D-8CE0-D89E9EF70EAF
ms.tgt_platform: multiple
keywords:
- Iconnectionbrokerclient-Schnittstelle Remotedesktopdienste
- Iconnectionbrokerclient-Schnittstelle Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IConnectionBrokerClient
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a062059f7aa1f16e32514b3bacbfb31dc0a350f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478891"
---
# <a name="iconnectionbrokerclient-interface"></a><span data-ttu-id="4cd2d-105">Iconnectionbrokerclient-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="4cd2d-105">IConnectionBrokerClient interface</span></span>

<span data-ttu-id="4cd2d-106">Stellt die Methoden bereit, die zum Verwenden des Remotedesktopverbindung Broker-Clients erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="4cd2d-106">Provides the methods needed to use the Remote Desktop Connection Broker client.</span></span>

<span data-ttu-id="4cd2d-107">Diese Schnittstelle wird vom System implementiert.</span><span class="sxs-lookup"><span data-stu-id="4cd2d-107">This interface is implemented by the system.</span></span> <span data-ttu-id="4cd2d-108">Verwenden Sie die [**cbkreateclientinstance**](cbcreateclientinstance.md) -Funktion, um eine Instanz dieser Schnittstelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4cd2d-108">To obtain an instance of this interface, use the [**CBCreateClientInstance**](cbcreateclientinstance.md) function.</span></span>

## <a name="members"></a><span data-ttu-id="4cd2d-109">Member</span><span class="sxs-lookup"><span data-stu-id="4cd2d-109">Members</span></span>

<span data-ttu-id="4cd2d-110">Die **iconnectionbrokerclient** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="4cd2d-110">The **IConnectionBrokerClient** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4cd2d-111">**Iconnectionbrokerclient** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4cd2d-111">**IConnectionBrokerClient** also has these types of members:</span></span>

-   [<span data-ttu-id="4cd2d-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="4cd2d-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4cd2d-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="4cd2d-113">Methods</span></span>

<span data-ttu-id="4cd2d-114">Die **iconnectionbrokerclient** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="4cd2d-114">The **IConnectionBrokerClient** interface has these methods.</span></span>



| <span data-ttu-id="4cd2d-115">Methode</span><span class="sxs-lookup"><span data-stu-id="4cd2d-115">Method</span></span>                                                         | <span data-ttu-id="4cd2d-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4cd2d-116">Description</span></span>                                                                                          |
|:---------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4cd2d-117">**Gettargetinfo**</span><span class="sxs-lookup"><span data-stu-id="4cd2d-117">**GetTargetInfo**</span></span>](iconnectionbrokerclient-gettargetinfo.md) | <span data-ttu-id="4cd2d-118">Fordert Informationen über den Zielcomputer an, an den die Verbindung umgeleitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4cd2d-118">Requests information about the target computer where the connection should be redirected.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4cd2d-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4cd2d-119">Requirements</span></span>



| <span data-ttu-id="4cd2d-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4cd2d-120">Requirement</span></span> | <span data-ttu-id="4cd2d-121">Wert</span><span class="sxs-lookup"><span data-stu-id="4cd2d-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cd2d-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4cd2d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4cd2d-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4cd2d-123">Windows 8</span></span><br/>                                                                       |
| <span data-ttu-id="4cd2d-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4cd2d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4cd2d-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4cd2d-125">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="4cd2d-126">Header</span><span class="sxs-lookup"><span data-stu-id="4cd2d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cd2d-127"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cd2d-127"><dt>Cbclient.h</dt></span></span> </dl>      |
| <span data-ttu-id="4cd2d-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4cd2d-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="4cd2d-129"><dt>Cbclient. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4cd2d-129"><dt>Cbclient.lib</dt></span></span> </dl>    |
| <span data-ttu-id="4cd2d-130">DLL</span><span class="sxs-lookup"><span data-stu-id="4cd2d-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4cd2d-131"><dt>Cbclient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4cd2d-131"><dt>Cbclient.dll</dt></span></span> </dl>    |
| <span data-ttu-id="4cd2d-132">IID</span><span class="sxs-lookup"><span data-stu-id="4cd2d-132">IID</span></span><br/>                      | <span data-ttu-id="4cd2d-133">IID \_ iconnectionbrokerclient ist als D6818DF2-8338-4EB7-AD77-DE210817987C definiert.</span><span class="sxs-lookup"><span data-stu-id="4cd2d-133">IID\_IConnectionBrokerClient is defined as D6818DF2-8338-4EB7-AD77-DE210817987C</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4cd2d-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4cd2d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cd2d-135">**Cbkreateclientinstance**</span><span class="sxs-lookup"><span data-stu-id="4cd2d-135">**CBCreateClientInstance**</span></span>](cbcreateclientinstance.md)
</dt> </dl>

 

