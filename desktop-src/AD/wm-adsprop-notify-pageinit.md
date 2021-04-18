---
title: WM_ADSPROP_NOTIFY_PAGEINIT Meldung (adsprop. h)
description: Eine Active Directory Eigenschaften Blatt Erweiterung ruft adspropgetinitinfo auf, um Daten über das Verzeichnis Objekt zu erhalten, für das die Eigenschaften Blatt Erweiterung gilt.
ms.assetid: 473c5a75-d0d9-4d12-b855-63683e8cdf3f
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_NOTIFY_PAGEINIT Meldung Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_PAGEINIT
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2718ee30cdbecec7c4e0954636aa14c75f13027
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517600"
---
# <a name="wm_adsprop_notify_pageinit-message"></a><span data-ttu-id="99130-104">WM \_ adsprop \_ benachrichtigt \_ pageInit-Nachricht</span><span class="sxs-lookup"><span data-stu-id="99130-104">WM\_ADSPROP\_NOTIFY\_PAGEINIT message</span></span>

<span data-ttu-id="99130-105">Eine Active Directory Eigenschaften Blatt Erweiterung ruft [**adspropgetinitinfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) auf, um Daten über das Verzeichnis Objekt zu erhalten, für das die Eigenschaften Blatt Erweiterung gilt.</span><span class="sxs-lookup"><span data-stu-id="99130-105">An Active Directory property sheet extension calls the [**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) to obtain data about regarding the directory object that the property sheet extension applies to.</span></span> <span data-ttu-id="99130-106">Die **adspropgetinitinfo** -Funktion sendet die " **WM \_ adsprop \_ Notify \_ pageInit** "-Nachricht an das Benachrichtigungs Objekt, um dieses Ergebnis zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="99130-106">The **ADsPropGetInitInfo** function sends the **WM\_ADSPROP\_NOTIFY\_PAGEINIT** message to the notification object to achieve this result.</span></span>


```C++
WM_ADSPROP_NOTIFY_PAGEINIT

    WPARAM wParam
    LPARAM pADsPropInitParams
    
```



## <a name="parameters"></a><span data-ttu-id="99130-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="99130-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99130-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="99130-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="99130-109">Handle des Benachrichtigungs Objekts.</span><span class="sxs-lookup"><span data-stu-id="99130-109">Handle of the notification object.</span></span> <span data-ttu-id="99130-110">Dies ist der *hnotifyobject* -Parameter, der durch einen Aufrufen von [**adspropkreatenotifyobj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="99130-110">This is the *hNotifyObject* parameter obtained by a call to [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> <dt>

<span data-ttu-id="99130-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="99130-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="99130-112">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="99130-112">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="99130-113">*padspropinitparametriams*</span><span class="sxs-lookup"><span data-stu-id="99130-113">*pADsPropInitParams*</span></span> 
</dt> <dd>

<span data-ttu-id="99130-114">Ein Zeiger auf eine [**adspropinitparameams**](/windows/desktop/api/Adsprop/ns-adsprop-adspropinitparams) -Struktur, die die Verzeichnis Objektinformationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="99130-114">Pointer to an [**ADSPROPINITPARAMS**](/windows/desktop/api/Adsprop/ns-adsprop-adspropinitparams) structure that receives the directory object information.</span></span> <span data-ttu-id="99130-115">Dies ist der an [**adspropkreatenotifyobj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)übergebenen *pinitparameams* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="99130-115">This is the *pInitParams* parameter passed to [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99130-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="99130-116">Return value</span></span>

<span data-ttu-id="99130-117">Diese Nachricht weist keinen Rückgabewert auf.</span><span class="sxs-lookup"><span data-stu-id="99130-117">This message has no return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="99130-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="99130-118">Requirements</span></span>



| <span data-ttu-id="99130-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="99130-119">Requirement</span></span> | <span data-ttu-id="99130-120">Wert</span><span class="sxs-lookup"><span data-stu-id="99130-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="99130-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="99130-121">Minimum supported client</span></span><br/> | <span data-ttu-id="99130-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="99130-122">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="99130-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="99130-123">Minimum supported server</span></span><br/> | <span data-ttu-id="99130-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="99130-124">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="99130-125">Header</span><span class="sxs-lookup"><span data-stu-id="99130-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="99130-126"><dt>Adsprop. h</dt></span><span class="sxs-lookup"><span data-stu-id="99130-126"><dt>Adsprop.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99130-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99130-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99130-128">Nachrichten in Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="99130-128">Messages in Active Directory Domain Services</span></span>](messages-in-active-directory-domain-services.md)
</dt> <dt>

[<span data-ttu-id="99130-129">**Adspropgetinitinfo**</span><span class="sxs-lookup"><span data-stu-id="99130-129">**ADsPropGetInitInfo**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo)
</dt> <dt>

[<span data-ttu-id="99130-130">**Adspropinitparameams**</span><span class="sxs-lookup"><span data-stu-id="99130-130">**ADSPROPINITPARAMS**</span></span>](/windows/desktop/api/Adsprop/ns-adsprop-adspropinitparams)
</dt> </dl>

 

 





