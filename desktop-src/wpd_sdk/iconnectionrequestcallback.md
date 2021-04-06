---
description: Definiert eine einzelne Rückruf Methode.
ms.assetid: 579f7a29-cd98-4d97-9f8e-9b786897df1c
title: Iconnectionrequestcallback-Schnittstelle (devpkey. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IConnectionRequestCallback
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: aca827de068ce221f013f03b35f88fd76a030dd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960848"
---
# <a name="iconnectionrequestcallback-interface"></a><span data-ttu-id="d5b78-103">Iconnectionrequestcallback-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d5b78-103">IConnectionRequestCallback interface</span></span>

<span data-ttu-id="d5b78-104">Die **iconnectionrequestcallback** -Schnittstelle definiert eine einzelne Rückruf Methode.</span><span class="sxs-lookup"><span data-stu-id="d5b78-104">The **IConnectionRequestCallback** interface defines a single callback method.</span></span> <span data-ttu-id="d5b78-105">Eine Windows Portable Devices (WPD)-Anwendung implementiert diese optionale Component Object Model (com)-Schnittstelle zum Empfangen von Benachrichtigungen zu abgeschlossenen Anforderungen und zum Abbrechen ausstehender Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="d5b78-105">A Windows Portable Devices (WPD) application implements this optional Component Object Model (COM) interface to receive notifications about completed requests and to cancel pending requests.</span></span> <span data-ttu-id="d5b78-106">Die Anforderungen werden mithilfe der [**iportabledeviceconnector:: Connect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) -Methode und der [**iportabledeviceconnector::D isconnect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) -Methode gesendet.</span><span class="sxs-lookup"><span data-stu-id="d5b78-106">The requests are sent using the [**IPortableDeviceConnector::Connect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-connect) and [**IPortableDeviceConnector::Disconnect**](/windows/desktop/api/portabledeviceconnectapi/nf-portabledeviceconnectapi-iportabledeviceconnector-disconnect) methods.</span></span>

## <a name="members"></a><span data-ttu-id="d5b78-107">Member</span><span class="sxs-lookup"><span data-stu-id="d5b78-107">Members</span></span>

<span data-ttu-id="d5b78-108">Die **iconnectionrequestcallback** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d5b78-108">The **IConnectionRequestCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d5b78-109">**Iconnectionrequestcallback** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d5b78-109">**IConnectionRequestCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="d5b78-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="d5b78-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d5b78-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="d5b78-111">Methods</span></span>

<span data-ttu-id="d5b78-112">Die **iconnectionrequestcallback** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="d5b78-112">The **IConnectionRequestCallback** interface has these methods.</span></span>



| <span data-ttu-id="d5b78-113">Methode</span><span class="sxs-lookup"><span data-stu-id="d5b78-113">Method</span></span>                                                      | <span data-ttu-id="d5b78-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d5b78-114">Description</span></span>                                                                           |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="d5b78-115">**OnComplete**</span><span class="sxs-lookup"><span data-stu-id="d5b78-115">**OnComplete**</span></span>](iconnectionrequestcallback-oncomplete.md) | <span data-ttu-id="d5b78-116">Benachrichtigt eine Anwendung, dass eine zuvor geplante Anforderung abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="d5b78-116">Notifies an application that a previously scheduled request has completed.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d5b78-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d5b78-117">Requirements</span></span>



| <span data-ttu-id="d5b78-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d5b78-118">Requirement</span></span> | <span data-ttu-id="d5b78-119">Wert</span><span class="sxs-lookup"><span data-stu-id="d5b78-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5b78-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d5b78-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d5b78-121">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d5b78-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="d5b78-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d5b78-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d5b78-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d5b78-123">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="d5b78-124">Header</span><span class="sxs-lookup"><span data-stu-id="d5b78-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5b78-125"><dt>Devpkey. h; </dt> <dt>Portablede viceconnectapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5b78-125"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="d5b78-126">IDL</span><span class="sxs-lookup"><span data-stu-id="d5b78-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d5b78-127"><dt>Portablede viceconnectapi. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d5b78-127"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="d5b78-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d5b78-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="d5b78-129"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5b78-129"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



 

