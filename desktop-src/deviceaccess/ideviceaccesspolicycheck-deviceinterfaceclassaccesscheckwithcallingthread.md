---
title: Ideviceaccesspolicycheck deviceinterfaceclassaccesscheckwithcallingthread-Methode
description: Diese API bestimmt, ob das Token für den aktuellen Kontext Zugriff auf die angegebene Geräteschnittstellen Klasse hat. IID 7d276ff2-ce90-4275-a2a8-9a48b10d3e0b.
ms.assetid: D7BFE1F3-4876-4BAB-A32D-46DB533140BB
keywords:
- Deviceingeterfaceclassaccesscheckwithcallingthread-Methode Geräte Zugriffs Broker-API
- Deviceinterfaceclassaccesscheckwithcallingthread-Methode Geräte Zugriffs Broker-API, ideviceaccesspolicycheck-Schnittstelle
- Ideviceaccesspolicycheck Interface Geräte Zugriffs Broker-API, deviceinterfaceclassaccesscheckwithcallingthread-Methode
topic_type:
- apiref
api_name:
- IDeviceAccessPolicyCheck.DeviceInterfaceClassAccessCheckWithCallingThread
api_type:
- COM
ms.topic: article
ms.date: 02/11/2020
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 44eb44a83175cf8f735abfeb8cfec4de83f46bd2
ms.sourcegitcommit: 01a4383738056cf3de4f45f36d98ef73d4dc694d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "106337205"
---
# <a name="ideviceaccesspolicycheckdeviceinterfaceclassaccesscheckwithcallingthread-method"></a><span data-ttu-id="60a73-107">Ideviceaccesspolicycheck::D eviceinterfaceclassaccesscheckwithcallingthread-Methode</span><span class="sxs-lookup"><span data-stu-id="60a73-107">IDeviceAccessPolicyCheck::DeviceInterfaceClassAccessCheckWithCallingThread method</span></span>

> [!Important]  
> <span data-ttu-id="60a73-108">Diese Schnittstellen werden nicht unterstützt und sollten nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60a73-108">These interfaces are not supported and should not be used.</span></span> <span data-ttu-id="60a73-109">Verwenden Sie stattdessen die APIs in der [C++-Programmier Referenz für die Geräte Zugriffs-API](device-access-api-c---programming-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="60a73-109">Use the APIs in the [Device Access API C++ Programming Reference](device-access-api-c---programming-reference.md) instead.</span></span>

<span data-ttu-id="60a73-110">Diese API bestimmt, ob das Token für den aktuellen Kontext Zugriff auf die angegebene Geräteschnittstellen Klasse hat.</span><span class="sxs-lookup"><span data-stu-id="60a73-110">This API will determine if the token for the current context has access to the device interface class specified.</span></span> <span data-ttu-id="60a73-111">IID = 7d276ff2-ce90-4275-a2a8-9a48b10d3e0b.</span><span class="sxs-lookup"><span data-stu-id="60a73-111">IID = 7D276FF2-CE90-4275-A2A8-9A48B10D3E0B.</span></span>

## <a name="syntax"></a><span data-ttu-id="60a73-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="60a73-112">Syntax</span></span>

```C++
HRESULT DeviceInterfaceClassAccessCheckWithCallingThread(
  [in] PCWSTR pszDeviceInterfaceClassGuid,
  [in] DWORD  dwClientThreadId
);
```

## <a name="parameters"></a><span data-ttu-id="60a73-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="60a73-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60a73-114">*pszbeviceingeterfakeclassguid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="60a73-114">*pszDeviceInterfaceClassGuid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60a73-115">Die Geräteschnittstellen Klassen-GUID, für die der Zugriff geprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="60a73-115">Device interface class GUID for which access should be checked.</span></span>

</dd> <dt>

<span data-ttu-id="60a73-116">*dwclientthreadid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="60a73-116">*dwClientThreadId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60a73-117">Clientthread-ID, bei der ggf. eine zugeordnete Benutzeroberfläche angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="60a73-117">Client thread ID where any associated UI should be shown if necessary.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60a73-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="60a73-118">Return value</span></span>

<span data-ttu-id="60a73-119">Wenn diese Funktion erfolgreich ausgeführt wird, wird S_OK zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="60a73-119">If this function succeeds, it returns S_OK.</span></span> <span data-ttu-id="60a73-120">Andernfalls wird ein HRESULT-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="60a73-120">Otherwise, it returns an HRESULT error code.</span></span>
