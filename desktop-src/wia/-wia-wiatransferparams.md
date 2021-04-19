---
description: 'Der wiatransferparameams wird während einer Datenübertragung durch das Windows-Abbild Erfassungs Laufzeitsystem (WIA) an die iwiatransfercallback:: transfercallback-Methode an eine Anwendung übertragen.'
ms.assetid: 4f1bbacf-e9fd-4129-ab05-3edaeecfaf43
title: Wiatransferparameams-Struktur (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WiaTransferParams
api_type:
- HeaderDef
api_location:
- Wia.h
ms.openlocfilehash: 4c432cab14e08d89a49234dd7c6de059cc9d72c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348786"
---
# <a name="wiatransferparams-structure"></a><span data-ttu-id="48b4a-103">Wiatransferparameams-Struktur</span><span class="sxs-lookup"><span data-stu-id="48b4a-103">WiaTransferParams structure</span></span>

<span data-ttu-id="48b4a-104">Der **wiatransferparameams** wird während einer Datenübertragung durch das Windows-Abbild Erfassungs Laufzeitsystem (WIA) an die [**iwiatransfercallback:: transfercallback**](-wia-iwiatransfercallback-transfercallback.md) -Methode an eine Anwendung übertragen.</span><span class="sxs-lookup"><span data-stu-id="48b4a-104">The **WiaTransferParams** is transmitted to an application during a data transfer by the Windows Image Acquisition (WIA) run-time system to the [**IWiaTransferCallback::TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="48b4a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="48b4a-105">Syntax</span></span>


```C++
typedef struct _WiaTransferParams {
  LONG    lMessage;
  LONG    lPercentComplete;
  ULONG64 ulTransferredBytes;
  HRESULT hrErrorStatus;
} WiaTransferParams;
```



## <a name="members"></a><span data-ttu-id="48b4a-106">Member</span><span class="sxs-lookup"><span data-stu-id="48b4a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="48b4a-107">**lMessage**</span><span class="sxs-lookup"><span data-stu-id="48b4a-107">**lMessage**</span></span>
</dt> <dd>

<span data-ttu-id="48b4a-108">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="48b4a-108">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="48b4a-109">Gibt den Status der Datenübertragung an.</span><span class="sxs-lookup"><span data-stu-id="48b4a-109">Indicates the status of the data transfer.</span></span>

<dt>

<span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>

<span data-ttu-id="48b4a-110"><span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>**Status der WIA- \_ Übertragungs Meldung \_ \_**</span><span class="sxs-lookup"><span data-stu-id="48b4a-110"><span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>**WIA\_TRANSFER\_MSG\_STATUS**</span></span>


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>

<span data-ttu-id="48b4a-111"><span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>**\_ \_ \_ Ende \_ des Daten \_ Stroms der WIA-Übertragungs Nachricht**</span><span class="sxs-lookup"><span data-stu-id="48b4a-111"><span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>**WIA\_TRANSFER\_MSG\_END\_OF\_STREAM**</span></span>


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>

<span data-ttu-id="48b4a-112"><span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>**\_ \_ \_ Ende \_ der \_ Übertragung der WIA-Übertragungs Nachricht**</span><span class="sxs-lookup"><span data-stu-id="48b4a-112"><span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>**WIA\_TRANSFER\_MSG\_END\_OF\_TRANSFER**</span></span>


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>

<span data-ttu-id="48b4a-113"><span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>**\_ \_ \_ Geräte \_ Status der WIA-Übertragungs Meldung**</span><span class="sxs-lookup"><span data-stu-id="48b4a-113"><span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>**WIA\_TRANSFER\_MSG\_DEVICE\_STATUS**</span></span>


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>

<span data-ttu-id="48b4a-114"><span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>**Seite "WIA \_ Transfer \_ msg \_ New \_ "**</span><span class="sxs-lookup"><span data-stu-id="48b4a-114"><span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>**WIA\_TRANSFER\_MSG\_NEW\_PAGE**</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="48b4a-115">**lprozentuabgeschlossen**</span><span class="sxs-lookup"><span data-stu-id="48b4a-115">**lPercentComplete**</span></span>
</dt> <dd>

<span data-ttu-id="48b4a-116">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="48b4a-116">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="48b4a-117">Gibt den Fortschritt der Datenübertragung als Prozentsatz an.</span><span class="sxs-lookup"><span data-stu-id="48b4a-117">Indicates the progress of the data transfer as a percentage.</span></span>

</dd> <dt>

<span data-ttu-id="48b4a-118">**ultransferredbytes**</span><span class="sxs-lookup"><span data-stu-id="48b4a-118">**ulTransferredBytes**</span></span>
</dt> <dd>

<span data-ttu-id="48b4a-119">Typ: **ULONG64**</span><span class="sxs-lookup"><span data-stu-id="48b4a-119">Type: **ULONG64**</span></span>

</dd> <dd>

<span data-ttu-id="48b4a-120">Gibt die Menge der übertragenen Daten an.</span><span class="sxs-lookup"><span data-stu-id="48b4a-120">Indicates the amount of data transferred.</span></span>

</dd> <dt>

<span data-ttu-id="48b4a-121">**hrerrorstatus**</span><span class="sxs-lookup"><span data-stu-id="48b4a-121">**hrErrorStatus**</span></span>
</dt> <dd>

<span data-ttu-id="48b4a-122">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="48b4a-122">Type: **HRESULT**</span></span>

</dd> <dd>

<span data-ttu-id="48b4a-123">Der Status oder Fehlerzustand des Geräts, das vom Treiber festgelegt wird. beispielsweise "Aufwärmphase".</span><span class="sxs-lookup"><span data-stu-id="48b4a-123">The status, or error state, of the device set by the driver; for example, "warming up".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="48b4a-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48b4a-124">Requirements</span></span>



| <span data-ttu-id="48b4a-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48b4a-125">Requirement</span></span> | <span data-ttu-id="48b4a-126">Wert</span><span class="sxs-lookup"><span data-stu-id="48b4a-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="48b4a-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="48b4a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="48b4a-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48b4a-128">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="48b4a-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="48b4a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="48b4a-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="48b4a-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="48b4a-131">Header</span><span class="sxs-lookup"><span data-stu-id="48b4a-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="48b4a-132"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="48b4a-132"><dt>Wia.h</dt></span></span> </dl> |



 

 




