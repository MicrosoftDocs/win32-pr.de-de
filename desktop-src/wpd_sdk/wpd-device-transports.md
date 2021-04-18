---
description: Der \_ Enumerationstyp der WPD-Geräte \_ Transporte gibt die Vererbungs Beziehung für einen Dienst an. Diese Enumeration wird von der WPD- \_ Geräte \_ Transport Eigenschaft verwendet.
ms.assetid: a9d48034-3588-4e48-a03a-91cbe679cbc9
title: WPD_DEVICE_TRANSPORTS-Enumeration (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_DEVICE_TRANSPORTS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 574c6b0b00980d110f2374e7426dd101c9122854
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358205"
---
# <a name="wpd_device_transports-enumeration"></a><span data-ttu-id="88952-104">WPD- \_ Geräte \_ Transport-Enumeration</span><span class="sxs-lookup"><span data-stu-id="88952-104">WPD\_DEVICE\_TRANSPORTS enumeration</span></span>

<span data-ttu-id="88952-105">Der Enumerationstyp der [**WPD- \_ Geräte \_ Transporte**](/windows/desktop/wpd_sdk/wpd-device-transports) gibt die Vererbungs Beziehung für einen Dienst an.</span><span class="sxs-lookup"><span data-stu-id="88952-105">The [**WPD\_DEVICE\_TRANSPORTS**](/windows/desktop/wpd_sdk/wpd-device-transports) enumeration type specifies the inheritance relationship for a service.</span></span> <span data-ttu-id="88952-106">Diese Enumeration wird von der **WPD- \_ Geräte \_ Transport** Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="88952-106">This enumeration is used by the **WPD\_DEVICE\_TRANSPORT** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="88952-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="88952-107">Syntax</span></span>


```C++
typedef enum tagWPD_DEVICE_TRANSPORTS { 
  WPD_DEVICE_TRANSPORT_UNSPECIFIED  = 0,
  WPD_DEVICE_TRANSPORT_USB          = 1,
  WPD_DEVICE_TRANSPORT_IP           = 2,
  WPD_DEVICE_TRANSPORT_BLUETOOTH    = 3
} WPD_DEVICE_TRANSPORTS;
```



## <a name="constants"></a><span data-ttu-id="88952-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="88952-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="88952-109"><span id="WPD_DEVICE_TRANSPORT_UNSPECIFIED"></span><span id="wpd_device_transport_unspecified"></span>**der WPD- \_ Geräte \_ Transport ist \_ nicht angegeben.**</span><span class="sxs-lookup"><span data-stu-id="88952-109"><span id="WPD_DEVICE_TRANSPORT_UNSPECIFIED"></span><span id="wpd_device_transport_unspecified"></span>**WPD\_DEVICE\_TRANSPORT\_UNSPECIFIED**</span></span>
</dt> <dd>

<span data-ttu-id="88952-110">Der Transporttyp wurde nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="88952-110">The transport type was not specified.</span></span>

</dd> <dt>

<span data-ttu-id="88952-111"><span id="WPD_DEVICE_TRANSPORT_USB"></span><span id="wpd_device_transport_usb"></span>**WPD \_ \_ -Geräte Transport \_ -USB**</span><span class="sxs-lookup"><span data-stu-id="88952-111"><span id="WPD_DEVICE_TRANSPORT_USB"></span><span id="wpd_device_transport_usb"></span>**WPD\_DEVICE\_TRANSPORT\_USB**</span></span>
</dt> <dd>

<span data-ttu-id="88952-112">Das Gerät ist über USB verbunden.</span><span class="sxs-lookup"><span data-stu-id="88952-112">The device is connected through USB.</span></span>

</dd> <dt>

<span data-ttu-id="88952-113"><span id="WPD_DEVICE_TRANSPORT_IP"></span><span id="wpd_device_transport_ip"></span>**WPD \_ \_ -Geräte Transport \_ -IP**</span><span class="sxs-lookup"><span data-stu-id="88952-113"><span id="WPD_DEVICE_TRANSPORT_IP"></span><span id="wpd_device_transport_ip"></span>**WPD\_DEVICE\_TRANSPORT\_IP**</span></span>
</dt> <dd>

<span data-ttu-id="88952-114">Das Gerät ist über das Internet Protokoll (IP) verbunden.</span><span class="sxs-lookup"><span data-stu-id="88952-114">The device is connected through Internet Protocol (IP).</span></span>

</dd> <dt>

<span data-ttu-id="88952-115"><span id="WPD_DEVICE_TRANSPORT_BLUETOOTH"></span><span id="wpd_device_transport_bluetooth"></span>**WPD- \_ Geräte \_ Transport \_ Bluetooth**</span><span class="sxs-lookup"><span data-stu-id="88952-115"><span id="WPD_DEVICE_TRANSPORT_BLUETOOTH"></span><span id="wpd_device_transport_bluetooth"></span>**WPD\_DEVICE\_TRANSPORT\_BLUETOOTH**</span></span>
</dt> <dd>

<span data-ttu-id="88952-116">Das Gerät ist über Bluetooth verbunden.</span><span class="sxs-lookup"><span data-stu-id="88952-116">The device is connected through Bluetooth.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="88952-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88952-117">Requirements</span></span>



| <span data-ttu-id="88952-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="88952-118">Requirement</span></span> | <span data-ttu-id="88952-119">Wert</span><span class="sxs-lookup"><span data-stu-id="88952-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="88952-120">Header</span><span class="sxs-lookup"><span data-stu-id="88952-120">Header</span></span><br/> | <dl> <span data-ttu-id="88952-121"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="88952-121"><dt>PortableDevice.h</dt></span></span> </dl> |



 

