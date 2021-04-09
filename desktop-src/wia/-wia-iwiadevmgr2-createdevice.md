---
description: Erstellt eine hierarchische Struktur von IWiaItem2-Objekten für ein Windows-Abbild Erfassungsgerät (WIA) 2,0.
ms.assetid: df7f3cc2-da0a-4238-b280-89c72107753c
title: 'IWiaDevMgr2:: kreatedevice-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.CreateDevice
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: a548a0ef43c2621b77c4ed10acde393af21d596d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865252"
---
# <a name="iwiadevmgr2createdevice-method"></a><span data-ttu-id="13417-103">IWiaDevMgr2:: kreatedevice-Methode</span><span class="sxs-lookup"><span data-stu-id="13417-103">IWiaDevMgr2::CreateDevice method</span></span>

<span data-ttu-id="13417-104">Erstellt eine hierarchische Struktur von [**IWiaItem2**](-wia-iwiaitem2.md) -Objekten für ein Windows-Abbild Erfassungsgerät (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="13417-104">Creates a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects for a Windows Image Acquisition (WIA) 2.0 device.</span></span>

## <a name="syntax"></a><span data-ttu-id="13417-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="13417-105">Syntax</span></span>


```C++
HRESULT CreateDevice(
  [in]  LONG      lFlags,
  [in]  BSTR      bstrDeviceID,
  [out] IWiaItem2 **ppWiaItem2Root
);
```



## <a name="parameters"></a><span data-ttu-id="13417-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="13417-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13417-107">*lFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13417-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13417-108">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="13417-108">Type: **LONG**</span></span>

<span data-ttu-id="13417-109">Derzeit nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="13417-109">Currently unused.</span></span> <span data-ttu-id="13417-110">Sollte auf Null festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="13417-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="13417-111">*bstraude viceid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13417-111">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13417-112">Typ: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="13417-112">Type: **BSTR**</span></span>

<span data-ttu-id="13417-113">Gibt den eindeutigen Bezeichner des WIA 2,0-Geräts an.</span><span class="sxs-lookup"><span data-stu-id="13417-113">Specifies the unique identifier of the WIA 2.0 device.</span></span>

</dd> <dt>

<span data-ttu-id="13417-114">*ppWiaItem2Root* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="13417-114">*ppWiaItem2Root* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13417-115">Typ: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="13417-115">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="13417-116">Empfängt die Adresse eines Zeigers auf die [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstelle des Stamm Elements in der hierarchischen Struktur für das WIA 2,0-Gerät.</span><span class="sxs-lookup"><span data-stu-id="13417-116">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the root item in the hierarchical tree for the WIA 2.0 device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13417-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="13417-117">Return value</span></span>

<span data-ttu-id="13417-118">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="13417-118">Type: **HRESULT**</span></span>

<span data-ttu-id="13417-119">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="13417-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="13417-120">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="13417-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="13417-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="13417-121">Remarks</span></span>

<span data-ttu-id="13417-122">Anwendungen verwenden die **IWiaDevMgr2:: kreatedevice** -Methode, um ein Geräte Objekt für die WIA 2,0-Geräte zu erstellen, die durch den bstrindeviceid-Parameter angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="13417-122">Applications use the **IWiaDevMgr2::CreateDevice** method to create a device object for the WIA 2.0 devices specified by the bstrDeviceID parameter.</span></span> <span data-ttu-id="13417-123">Wenn der Wert zurückgegeben wird, speichert die **IWiaDevMgr2:: kreatedevice** -Methode eine Adresse eines Zeigers im Parameter *ppWiaItem2Root*, der auf das Stamm Element der [**IWiaItem2**](-wia-iwiaitem2.md) -Objekte zeigt, die von **IWiaDevMgr2:: kreatedevice** erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="13417-123">When it returns, the **IWiaDevMgr2::CreateDevice** method stores an address of a pointer in the parameter *ppWiaItem2Root*, which points to the root item of the tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects created by **IWiaDevMgr2::CreateDevice**.</span></span> <span data-ttu-id="13417-124">Anwendungen können diese Objektstruktur verwenden, um Daten aus dem WIA 2,0-Gerät zu steuern und abzurufen.</span><span class="sxs-lookup"><span data-stu-id="13417-124">Applications can use this tree of objects to control and retrieve data from the WIA 2.0 device.</span></span>

<span data-ttu-id="13417-125">Anwendungen müssen die [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode für die Zeiger aufrufen, die Sie über den *ppWiaItem2Root* -Parameter empfangen.</span><span class="sxs-lookup"><span data-stu-id="13417-125">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the pointers they receive through the *ppWiaItem2Root* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="13417-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13417-126">Requirements</span></span>



| <span data-ttu-id="13417-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="13417-127">Requirement</span></span> | <span data-ttu-id="13417-128">Wert</span><span class="sxs-lookup"><span data-stu-id="13417-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="13417-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="13417-129">Minimum supported client</span></span><br/> | <span data-ttu-id="13417-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="13417-130">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="13417-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="13417-131">Minimum supported server</span></span><br/> | <span data-ttu-id="13417-132">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="13417-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="13417-133">Header</span><span class="sxs-lookup"><span data-stu-id="13417-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="13417-134"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="13417-134"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="13417-135">IDL</span><span class="sxs-lookup"><span data-stu-id="13417-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="13417-136"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="13417-136"><dt>Wia.idl</dt></span></span> </dl> |



 

 
