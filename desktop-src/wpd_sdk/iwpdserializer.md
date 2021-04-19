---
description: 'Die iwpdserializer-Schnittstelle wird vom Gerätetreiber zum Serialisieren von iportabledevicevalues-Schnittstellen zu und aus den Rohdaten Puffern verwendet, die für die Kommunikation mit der Anwendung verwendet werden. Anwendungen müssen diese Schnittstelle nicht verwenden, da die Daten beim Aufrufen von iportabledevice:: sendCommand automatisch serialisiert und deserialisiert werden. Rufen Sie CoCreateInstance auf, und übergeben Sie IID iwpdserializer, um diese Schnittstelle abzurufen. \_'
ms.assetid: 837bd850-6e27-4f8e-a612-d16f61b92b1d
title: Iwpdserializer-Schnittstelle (portabledevicetypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: dde4bfeea596ccc2691323d484f5583d55ade621
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373873"
---
# <a name="iwpdserializer-interface"></a><span data-ttu-id="19d4e-103">Iwpdserializer-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="19d4e-103">IWpdSerializer interface</span></span>

<span data-ttu-id="19d4e-104">Die **iwpdserializer** -Schnittstelle wird vom Gerätetreiber zum Serialisieren von [**iportabledevicevalues**](iportabledevicevalues.md) -Schnittstellen zu und aus den Rohdaten Puffern verwendet, die für die Kommunikation mit der Anwendung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="19d4e-104">The **IWpdSerializer** interface is used by the device driver to serialize [**IPortableDeviceValues**](iportabledevicevalues.md) interfaces to and from the raw data buffers used to communicate with the application.</span></span>

<span data-ttu-id="19d4e-105">Anwendungen müssen diese Schnittstelle nicht verwenden, da die Daten beim Aufrufen von [**iportabledevice:: Send Command**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)automatisch serialisiert und deserialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="19d4e-105">Applications do not need to use this interface, because the data is serialized and deserialized automatically when calling [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).</span></span>

<span data-ttu-id="19d4e-106">Um diese Schnittstelle zu erhalten, müssen Sie **cokreateinstance** aufrufen und **IID \_ iwpdserializer** übergeben.</span><span class="sxs-lookup"><span data-stu-id="19d4e-106">To get this interface, call **CoCreateInstance** and pass in **IID\_IWpdSerializer**.</span></span>

## <a name="members"></a><span data-ttu-id="19d4e-107">Member</span><span class="sxs-lookup"><span data-stu-id="19d4e-107">Members</span></span>

<span data-ttu-id="19d4e-108">Die **iwpdserializer** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="19d4e-108">The **IWpdSerializer** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="19d4e-109">**Iwpdserializer** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="19d4e-109">**IWpdSerializer** also has these types of members:</span></span>

-   [<span data-ttu-id="19d4e-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="19d4e-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="19d4e-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="19d4e-111">Methods</span></span>

<span data-ttu-id="19d4e-112">Die **iwpdserializer** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="19d4e-112">The **IWpdSerializer** interface has these methods.</span></span>



| <span data-ttu-id="19d4e-113">Methode</span><span class="sxs-lookup"><span data-stu-id="19d4e-113">Method</span></span>                                                                                          | <span data-ttu-id="19d4e-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="19d4e-114">Description</span></span>                                                                                                      |
|:------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="19d4e-115">**Getbufferfromiportabledecoevalues**</span><span class="sxs-lookup"><span data-stu-id="19d4e-115">**GetBufferFromIPortableDeviceValues**</span></span>](iwpdserializer-getbufferfromiportabledevicevalues.md) | <span data-ttu-id="19d4e-116">Serialisiert eine übermittelte **iportabledevicevalues** -Schnittstelle zu einem zugeordneten Bytearray.</span><span class="sxs-lookup"><span data-stu-id="19d4e-116">Serializes a submitted **IPortableDeviceValues** interface to an allocated byte array.</span></span><br/>                |
| [<span data-ttu-id="19d4e-117">**Getiportableendvicevaluesfrombuffer**</span><span class="sxs-lookup"><span data-stu-id="19d4e-117">**GetIPortableDeviceValuesFromBuffer**</span></span>](iwpdserializer-getiportabledevicevaluesfrombuffer.md) | <span data-ttu-id="19d4e-118">Deserialisiert ein Bytearray in eine **iportabledevicevalues** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="19d4e-118">Deserializes a byte array to an **IPortableDeviceValues** interface.</span></span><br/>                                  |
| [<span data-ttu-id="19d4e-119">**Getserializedsize**</span><span class="sxs-lookup"><span data-stu-id="19d4e-119">**GetSerializedSize**</span></span>](iwpdserializer-getserializedsize.md)                                   | <span data-ttu-id="19d4e-120">Berechnet die Puffergröße, die zum Speichern einer serialisierten **iportabledevicevalues** -Schnittstelle erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="19d4e-120">Calculates the buffer size that is required to hold a serialized **IPortableDeviceValues** interface.</span></span><br/> |
| [<span data-ttu-id="19d4e-121">**"Schreibportabledebug"**</span><span class="sxs-lookup"><span data-stu-id="19d4e-121">**WriteIPortableDeviceValuesToBuffer**</span></span>](iwpdserializer-writeiportabledevicevaluestobuffer.md) | <span data-ttu-id="19d4e-122">Serialisiert eine **iportabledevicevalues** -Schnittstelle zu einem vom Aufrufer zugeordneten Bytearray.</span><span class="sxs-lookup"><span data-stu-id="19d4e-122">Serializes an **IPortableDeviceValues** interface to a caller-allocated byte array.</span></span><br/>                   |



 

## <a name="requirements"></a><span data-ttu-id="19d4e-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19d4e-123">Requirements</span></span>



| <span data-ttu-id="19d4e-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="19d4e-124">Requirement</span></span> | <span data-ttu-id="19d4e-125">Wert</span><span class="sxs-lookup"><span data-stu-id="19d4e-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19d4e-126">Header</span><span class="sxs-lookup"><span data-stu-id="19d4e-126">Header</span></span><br/>  | <dl> <span data-ttu-id="19d4e-127"><dt>Portablede vicetypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="19d4e-127"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="19d4e-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="19d4e-128">Library</span></span><br/> | <dl> <span data-ttu-id="19d4e-129"><dt>Portabledeviceguids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="19d4e-129"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19d4e-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19d4e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19d4e-131">**Treiber Schnittstellen**</span><span class="sxs-lookup"><span data-stu-id="19d4e-131">**Driver Interfaces**</span></span>](driver-interfaces.md)
</dt> </dl>

 

