---
description: Erstellt einen Enumerator mit Eigenschafts Informationen für jedes verfügbare Windows-Abbild Erfassungsgerät (WIA) 2,0.
ms.assetid: e37b73d5-5192-46e4-bb1c-bd1ef41f1d6c
title: 'IWiaDevMgr2:: enumdevicumfo-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.EnumDeviceInfo
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: bd9e9281b625f4cec5377537d82a304045b95a3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752840"
---
# <a name="iwiadevmgr2enumdeviceinfo-method"></a><span data-ttu-id="35c5f-103">IWiaDevMgr2:: enumdevicumfo-Methode</span><span class="sxs-lookup"><span data-stu-id="35c5f-103">IWiaDevMgr2::EnumDeviceInfo method</span></span>

<span data-ttu-id="35c5f-104">Erstellt einen Enumerator mit Eigenschafts Informationen für jedes verfügbare Windows-Abbild Erfassungsgerät (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="35c5f-104">Creates an enumerator of property information for each available Windows Image Acquisition (WIA) 2.0 device.</span></span>

## <a name="syntax"></a><span data-ttu-id="35c5f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="35c5f-105">Syntax</span></span>


```C++
HRESULT EnumDeviceInfo(
  [in]          LONG              lFlags,
  [out, retval] IEnumWIA_DEV_INFO **ppIEnum
);
```



## <a name="parameters"></a><span data-ttu-id="35c5f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="35c5f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35c5f-107">*lFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35c5f-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35c5f-108">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="35c5f-108">Type: **LONG**</span></span>

<span data-ttu-id="35c5f-109">Gibt den Typ der aufzuzählenden WIA 2,0-Geräte an.</span><span class="sxs-lookup"><span data-stu-id="35c5f-109">Specifies the type of WIA 2.0 devices to enumerate.</span></span>

<dt>

<span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>

<span data-ttu-id="35c5f-110"><span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>**WIA-Aufzählung ( \_ \_ \_ lokal)**</span><span class="sxs-lookup"><span data-stu-id="35c5f-110"><span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>**WIA\_DEVINFO\_ENUM\_LOCAL**</span></span>


</dt> <dd>

<span data-ttu-id="35c5f-111">Nur lokal verbundene aktive Überprüfungs Geräte werden aufgezählt.</span><span class="sxs-lookup"><span data-stu-id="35c5f-111">Only locally connected active scanner devices are enumerated.</span></span>

</dd> <dt>

<span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>

<span data-ttu-id="35c5f-112"><span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>**WIA-Aufzählung \_ \_ \_ alle**</span><span class="sxs-lookup"><span data-stu-id="35c5f-112"><span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>**WIA\_DEVINFO\_ENUM\_ALL**</span></span>


</dt> <dd>

<span data-ttu-id="35c5f-113">Alle Geräte werden sowohl lokal als auch Remote aufgelistet, einschließlich inaktiver (nicht verbundener) Geräte und Legacy-Geräte mit nur-STI-Geräten.</span><span class="sxs-lookup"><span data-stu-id="35c5f-113">All devices are enumerated, both locally and remote, including inactive (disconnected) devices and legacy STI-only devices.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="35c5f-114">*ppiumum* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="35c5f-114">*ppIEnum* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="35c5f-115">Typ: **[ **ienumwia \_ dev \_ Info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)\*\***</span><span class="sxs-lookup"><span data-stu-id="35c5f-115">Type: **[**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)\*\***</span></span>

<span data-ttu-id="35c5f-116">Empfängt die Adresse eines Zeigers auf die [**ienumwia \_ dev \_ Info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="35c5f-116">Receives the address of a pointer to the [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35c5f-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="35c5f-117">Return value</span></span>

<span data-ttu-id="35c5f-118">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="35c5f-118">Type: **HRESULT**</span></span>

<span data-ttu-id="35c5f-119">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="35c5f-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="35c5f-120">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="35c5f-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="35c5f-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="35c5f-121">Remarks</span></span>

<span data-ttu-id="35c5f-122">Die **IWiaDevMgr2:: enumdeviceinfo** -Methode erstellt ein Enumeratorobjekt, das die [**ienumwia \_ dev \_ Info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) -Schnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="35c5f-122">The **IWiaDevMgr2::EnumDeviceInfo** method creates an enumerator object that supports the [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) interface.</span></span> <span data-ttu-id="35c5f-123">Die-Methode speichert einen Zeiger auf die **ienumwia \_ dev \_ Info** -Schnittstelle im Parameter *ppienumum*.</span><span class="sxs-lookup"><span data-stu-id="35c5f-123">The method stores a pointer to the **IEnumWIA\_DEV\_INFO** interface in the parameter *ppIEnum*.</span></span> <span data-ttu-id="35c5f-124">Anwendungen können den **ienumwia \_ dev \_ Info** -Schnittstellen Zeiger verwenden, um die Eigenschaften jedes WIA 2,0-Geräts aufzulisten, das mit dem Computer des Benutzers verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="35c5f-124">Applications can use the **IEnumWIA\_DEV\_INFO** interface pointer to enumerate the properties of each WIA 2.0 device attached to the user's computer.</span></span>

<span data-ttu-id="35c5f-125">Anwendungen müssen die [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode für die Schnittstellen Zeiger aufrufen, die Sie über den *ppienum* -Parameter empfangen.</span><span class="sxs-lookup"><span data-stu-id="35c5f-125">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIEnum* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="35c5f-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="35c5f-126">Requirements</span></span>



| <span data-ttu-id="35c5f-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="35c5f-127">Requirement</span></span> | <span data-ttu-id="35c5f-128">Wert</span><span class="sxs-lookup"><span data-stu-id="35c5f-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="35c5f-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="35c5f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="35c5f-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="35c5f-130">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="35c5f-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="35c5f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="35c5f-132">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="35c5f-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="35c5f-133">Header</span><span class="sxs-lookup"><span data-stu-id="35c5f-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="35c5f-134"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="35c5f-134"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="35c5f-135">IDL</span><span class="sxs-lookup"><span data-stu-id="35c5f-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="35c5f-136"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="35c5f-136"><dt>Wia.idl</dt></span></span> </dl> |



 

 
