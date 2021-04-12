---
title: Idevicebroker opendevicefrominterfacepath-Methode
description: Versucht, eine Geräteschnittstellen Instanz im Namen eines Clients zu öffnen. IID 8604b268-34a6-4b1a-a59b-cdbd8379bd98.
ms.assetid: 5ADDB994-3AAB-49B2-8B83-F71883AFD854
keywords:
- Opendevicefrominterfacepath-Methode Geräte Zugriffs Broker-API
- Opendevicefrominterfacepath-Methode Geräte Zugriffs Broker-API, idevicebroker-Schnittstelle
- Idevicebroker-Schnittstelle Geräte Zugriffs Broker-API, opendevicefrominterfacepath-Methode
topic_type:
- apiref
api_name:
- IDeviceBroker.OpenDeviceFromInterfacePath
api_type:
- COM
ms.topic: article
ms.date: 02/11/2020
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5363600455ee1ba5c1c86cb12690afd242f68118
ms.sourcegitcommit: 01a4383738056cf3de4f45f36d98ef73d4dc694d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "104389818"
---
# <a name="idevicebrokeropendevicefrominterfacepath-method"></a><span data-ttu-id="ba0ef-107">Idevicebroker:: opendevicefrominterfacepath-Methode</span><span class="sxs-lookup"><span data-stu-id="ba0ef-107">IDeviceBroker::OpenDeviceFromInterfacePath method</span></span>

> [!Important]  
> <span data-ttu-id="ba0ef-108">Diese Schnittstellen werden nicht unterstützt und sollten nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ba0ef-108">These interfaces are not supported and should not be used.</span></span> <span data-ttu-id="ba0ef-109">Verwenden Sie stattdessen die APIs in der [C++-Programmier Referenz für die Geräte Zugriffs-API](device-access-api-c---programming-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="ba0ef-109">Use the APIs in the [Device Access API C++ Programming Reference](device-access-api-c---programming-reference.md) instead.</span></span>

<span data-ttu-id="ba0ef-110">Versucht, eine Geräteschnittstellen Instanz im Namen eines Clients zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ba0ef-110">Attempts to open a device interface instance on behalf of a client.</span></span> <span data-ttu-id="ba0ef-111">IID = 8604b268-34a6-4b1a-a59b-cdbd8379bd98.</span><span class="sxs-lookup"><span data-stu-id="ba0ef-111">IID = 8604b268-34A6-4b1A-A59F-CDBD8379FD98.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba0ef-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba0ef-112">Syntax</span></span>

```C++
HRESULT OpenDeviceFromInterfacePath(
  [in]  PCWSTR pszDeviceInterfacePath,
  [in]  DWORD  desiredAccess,
  [in]  DWORD  shareMode,
  [in]  DWORD  flagsAndAttributes,
  [out] Handle *phDevice
);
```

## <a name="parameters"></a><span data-ttu-id="ba0ef-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba0ef-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba0ef-114">*pszde viceinterfacepath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ba0ef-114">*pszDeviceInterfacePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba0ef-115">Zu öffnende Geräteschnittstellen Instanz.</span><span class="sxs-lookup"><span data-stu-id="ba0ef-115">Device interface instance to open.</span></span>

</dd> <dt>

<span data-ttu-id="ba0ef-116">*desiredAccess* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ba0ef-116">*desiredAccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba0ef-117">Gewünschter Zugriff zum Öffnen an</span><span class="sxs-lookup"><span data-stu-id="ba0ef-117">Desired access to be passed to open.</span></span>

</dd> <dt>

<span data-ttu-id="ba0ef-118">*share Mode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ba0ef-118">*shareMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba0ef-119">Der Freigabe Modus, der an "Öffnen" weitergegeben werden</span><span class="sxs-lookup"><span data-stu-id="ba0ef-119">Share mode to be passed to open.</span></span>

</dd> <dt>

<span data-ttu-id="ba0ef-120">*flagsandattribute* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ba0ef-120">*flagsAndAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba0ef-121">Flags und Attribute, die an Open übermittelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ba0ef-121">Flags and attributes to be passed to open.</span></span>

</dd> <dt>

<span data-ttu-id="ba0ef-122">*\* phdevice* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ba0ef-122">*\*phDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba0ef-123">Resultierende Handle, wenn das Öffnen erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="ba0ef-123">Resulting handle if open was successful.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba0ef-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ba0ef-124">Return value</span></span>

<span data-ttu-id="ba0ef-125">Wenn diese Funktion erfolgreich ausgeführt wird, wird S_OK zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ba0ef-125">If this function succeeds, it returns S_OK.</span></span> <span data-ttu-id="ba0ef-126">Andernfalls wird ein HRESULT-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ba0ef-126">Otherwise, it returns an HRESULT error code.</span></span>
