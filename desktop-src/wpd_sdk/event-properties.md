---
description: Tragbare Windows-Geräte unterstützen die folgenden Ereignis Eigenschaften.
ms.assetid: 672b75ac-cd47-4212-a505-c220ecdf98e3
title: Ereignis Eigenschaften (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Event
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 54c7aefeaf1170b7a8b8e3e79a62288f2d14dad2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367207"
---
# <a name="event-properties"></a><span data-ttu-id="3a931-103">Ereigniseigenschaften</span><span class="sxs-lookup"><span data-stu-id="3a931-103">Event Properties</span></span>

<span data-ttu-id="3a931-104">Tragbare Windows-Geräte unterstützen die folgenden Ereignis Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3a931-104">Windows Portable Devices supports the following event properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="3a931-105">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3a931-105">Property</span></span></th>
<th><span data-ttu-id="3a931-106">VarType</span><span class="sxs-lookup"><span data-stu-id="3a931-106">VarType</span></span></th>
<th><span data-ttu-id="3a931-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3a931-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3a931-108"><strong>WPD_EVENT_OPTION_IS_AUTOPLAY_EVENT</strong></span><span class="sxs-lookup"><span data-stu-id="3a931-108"><strong>WPD_EVENT_OPTION_IS_AUTOPLAY_EVENT</strong></span></span></td>
<td><span data-ttu-id="3a931-109"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="3a931-109"><strong>VT_BOOL</strong></span></span></td>
<td><span data-ttu-id="3a931-110">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="3a931-110">Reserved for future use.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a931-111"><strong>WPD_EVENT_OPTION_IS_BROADCAST_EVENT</strong></span><span class="sxs-lookup"><span data-stu-id="3a931-111"><strong>WPD_EVENT_OPTION_IS_BROADCAST_EVENT</strong></span></span></td>
<td><span data-ttu-id="3a931-112"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="3a931-112"><strong>VT_BOOL</strong></span></span></td>
<td><span data-ttu-id="3a931-113">Ein boolescher Wert, der angibt, ob das Ereignis an alle Clients übertragen wird. Clients können dieses Ereignis empfangen, indem Sie Ihren Rückruf bei <strong>iportabledevice:: Rat</strong>registrieren.</span><span class="sxs-lookup"><span data-stu-id="3a931-113">A Boolean value that specifies whether the event is broadcast to all clients.Clients can receive this event by registering their callback with <strong>IPortableDevice::Advise</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3a931-114"><strong>WPD_EVENT_PARAMETER_CHILD_HIERARCHY_CHANGED</strong></span><span class="sxs-lookup"><span data-stu-id="3a931-114"><strong>WPD_EVENT_PARAMETER_CHILD_HIERARCHY_CHANGED</strong></span></span></td>
<td><span data-ttu-id="3a931-115"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="3a931-115"><strong>VT_BOOL</strong></span></span></td>
<td><span data-ttu-id="3a931-116">Ein boolescher Wert, der angibt, ob sich die untergeordnete Hierarchie für das-Objekt geändert hat. Dieser Parameter wird verwendet, um den Aufrufer darüber zu benachrichtigen, dass einige untergeordnete Elemente für das angegebene Objekt hinzugefügt oder entfernt wurden.</span><span class="sxs-lookup"><span data-stu-id="3a931-116">A Boolean value that specifies whether the child hierarchy for the object has changed.This parameter is used to notify the caller that some children for the specified object have been added or removed.</span></span> <span data-ttu-id="3a931-117">In der Regel wird die Hierarchie Änderung auf der Geräteseite initiiert.</span><span class="sxs-lookup"><span data-stu-id="3a931-117">Typically the hierarchy change is initiated on the device side.</span></span> <span data-ttu-id="3a931-118">Clients müssen die untergeordneten Elemente dieses Ordners möglicherweise erneut aufzählen, um ihre Ansichten auf dem neuesten Stand zu halten.</span><span class="sxs-lookup"><span data-stu-id="3a931-118">Clients may have to re-enumerate this folder's children to keep their views up to date.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a931-119"><strong>WPD_EVENT_PARAMETER_EVENT_ID</strong></span><span class="sxs-lookup"><span data-stu-id="3a931-119"><strong>WPD_EVENT_PARAMETER_EVENT_ID</strong></span></span></td>
<td><span data-ttu-id="3a931-120"><strong>VT_CLSID</strong></span><span class="sxs-lookup"><span data-stu-id="3a931-120"><strong>VT_CLSID</strong></span></span></td>
<td><span data-ttu-id="3a931-121">Ein-Wert, der ein Ereignis bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="3a931-121">A value that identifies an event.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3a931-122"><strong>WPD_EVENT_PARAMETER_OBJECT_CREATION_COOKIE</strong></span><span class="sxs-lookup"><span data-stu-id="3a931-122"><strong>WPD_EVENT_PARAMETER_OBJECT_CREATION_COOKIE</strong></span></span></td>
<td><span data-ttu-id="3a931-123"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="3a931-123"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="3a931-124">Das Cookie, das an einen Client zurückgegeben wird, wenn es durch Aufrufen der <a href="/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata"><strong>iportabledevicecontent:: createobjectwithpropertiesanddata</strong></a> -Methode eine Objekt Erstellung anfordert. Dieser Parameter wird hinzugefügt, um dem Aufrufer dabei zu helfen, ein Objekt hinzugefügtes Ereignis mit der Anforderung zu verknüpfen, die zum Erstellen des Objekts gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="3a931-124">The cookie handed back to a client when it requests an object creation by calling the <a href="/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata"><strong>IPortableDeviceContent::CreateObjectWithPropertiesAndData</strong></a> method.This parameter is added as a convenience to help the caller tie an object-added event to the request it sent to create the object.</span></span> <span data-ttu-id="3a931-125">Der Treiber übergibt dieses Cookie zurück als <strong>WPD_PROPERTY_OBJECT_MANAGEMENT_CONTEXT</strong> Rückgabewert, wenn der <strong>WPD_COMMAND_OBJECT_MANAGEMENT_CREATE_OBJECT_WITH_PROPERTIES_AND_DATA</strong> Befehl verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="3a931-125">The driver hands this cookie back as the <strong>WPD_PROPERTY_OBJECT_MANAGEMENT_CONTEXT</strong> return value when processing the <strong>WPD_COMMAND_OBJECT_MANAGEMENT_CREATE_OBJECT_WITH_PROPERTIES_AND_DATA</strong> command.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a931-126"><strong>WPD_EVENT_PARAMETER_OBJECT_PARENT_PERSISTENT_UNIQUE_ID</strong></span><span class="sxs-lookup"><span data-stu-id="3a931-126"><strong>WPD_EVENT_PARAMETER_OBJECT_PARENT_PERSISTENT_UNIQUE_ID</strong></span></span></td>
<td><span data-ttu-id="3a931-127"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="3a931-127"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="3a931-128">Ein Wert, der das übergeordnete Objekt eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="3a931-128">A value that uniquely identifies the parent object.</span></span> <span data-ttu-id="3a931-129">Diese Eigenschaft ähnelt <strong>WPD_OBJECT_PARENT_ID</strong>, aber diese ID ändert sich nicht zwischen den Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="3a931-129">This property is similar to <strong>WPD_OBJECT_PARENT_ID</strong>, but this ID does not change between sessions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3a931-130"><strong>WPD_EVENT_PARAMETER_OPERATION_PROGRESS</strong></span><span class="sxs-lookup"><span data-stu-id="3a931-130"><strong>WPD_EVENT_PARAMETER_OPERATION_PROGRESS</strong></span></span></td>
<td><span data-ttu-id="3a931-131"><strong>VT_UI4</strong></span><span class="sxs-lookup"><span data-stu-id="3a931-131"><strong>VT_UI4</strong></span></span></td>
<td><span data-ttu-id="3a931-132">Ein-Wert, der den Status eines aktuell ausgeführten Vorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="3a931-132">A value that specifies the progress of a currently executing operation.</span></span> <span data-ttu-id="3a931-133">Der Wert dieser Eigenschaft kann zwischen 0 und 100 liegen, wobei 100 angibt, dass der Vorgang beendet ist.</span><span class="sxs-lookup"><span data-stu-id="3a931-133">The value of this property can range from 0 to 100, with 100 indicating that the operation is complete.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a931-134"><strong>WPD_EVENT_PARAMETER_OPERATION_STATE</strong></span><span class="sxs-lookup"><span data-stu-id="3a931-134"><strong>WPD_EVENT_PARAMETER_OPERATION_STATE</strong></span></span></td>
<td><span data-ttu-id="3a931-135"><strong>VT_UI4</strong></span><span class="sxs-lookup"><span data-stu-id="3a931-135"><strong>VT_UI4</strong></span></span></td>
<td><span data-ttu-id="3a931-136">Ein-Wert, der den aktuellen Zustand des Vorgangs angibt, z. b. "gestartet", "wird ausgeführt", "beendet" usw. Die möglichen Werte dieses Parameters stammen aus der in portabledevice. h definierten <strong>WPD_OPERATION_STATES</strong> Enumeration.</span><span class="sxs-lookup"><span data-stu-id="3a931-136">A value that indicates the current state of the operation, for example, started, running, stopped, and so on.This parameter's possible values are from the <strong>WPD_OPERATION_STATES</strong> enumeration defined in PortableDevice.h.</span></span> <span data-ttu-id="3a931-137">Dabei sind folgende Werte möglich:</span><span class="sxs-lookup"><span data-stu-id="3a931-137">Possible values are:</span></span><br/> <dl> <span data-ttu-id="3a931-138"><strong>WPD_OPERATION_STATE_UNSPECIFIED</strong></span><span class="sxs-lookup"><span data-stu-id="3a931-138"><strong>WPD_OPERATION_STATE_UNSPECIFIED</strong></span></span><br /><span data-ttu-id="3a931-139">
<strong>WPD_OPERATION_STATE_STARTED</strong></span><span class="sxs-lookup"><span data-stu-id="3a931-139">
<strong>WPD_OPERATION_STATE_STARTED</strong></span></span><br /><span data-ttu-id="3a931-140">
<strong>WPD_OPERATION_STATE_RUNNING</strong></span><span class="sxs-lookup"><span data-stu-id="3a931-140">
<strong>WPD_OPERATION_STATE_RUNNING</strong></span></span><br /><span data-ttu-id="3a931-141">
<strong>WPD_OPERATION_STATE_PAUSED</strong></span><span class="sxs-lookup"><span data-stu-id="3a931-141">
<strong>WPD_OPERATION_STATE_PAUSED</strong></span></span><br /><span data-ttu-id="3a931-142">
<strong>WPD_OPERATION_STATE_CANCELLED</strong></span><span class="sxs-lookup"><span data-stu-id="3a931-142">
<strong>WPD_OPERATION_STATE_CANCELLED</strong></span></span><br /><span data-ttu-id="3a931-143">
<strong>WPD_OPERATION_STATE_FINISHED</strong></span><span class="sxs-lookup"><span data-stu-id="3a931-143">
<strong>WPD_OPERATION_STATE_FINISHED</strong></span></span><br /><span data-ttu-id="3a931-144">
<strong>WPD_OPERATION_STATE_ABORTED</strong></span><span class="sxs-lookup"><span data-stu-id="3a931-144">
<strong>WPD_OPERATION_STATE_ABORTED</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3a931-145"><strong>WPD_EVENT_PARAMETER_PNP_DEVICE_ID</strong></span><span class="sxs-lookup"><span data-stu-id="3a931-145"><strong>WPD_EVENT_PARAMETER_PNP_DEVICE_ID</strong></span></span></td>
<td><span data-ttu-id="3a931-146"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="3a931-146"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="3a931-147">Ein-Wert, der das Gerät angibt, von dem das Ereignis stammt. Dies ist das Gerät oder der Dienst Bezeichner, das vom PNP-System (Plug-and-Play) angegeben wird, und ist dieselbe Zeichenfolge, die in der <strong>iportabledevice:: Open</strong>-Methode oder der <a href="/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open"><strong>iportabledeviceservice:: Open</strong></a> -Methode verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3a931-147">A value that specifies the device that originated the event.This is the device or service identifier given by the Plug-and-Play (PnP) system, and is the same string used in the <strong>IPortableDevice::Open</strong>or <a href="/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open"><strong>IPortableDeviceService::Open</strong></a> methods.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3a931-148"><strong>WPD_EVENT_PARAMETER_SERVICE_METHOD_CONTEXT</strong></span><span class="sxs-lookup"><span data-stu-id="3a931-148"><strong>WPD_EVENT_PARAMETER_SERVICE_METHOD_CONTEXT</strong></span></span></td>
<td><span data-ttu-id="3a931-149"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="3a931-149"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="3a931-150">Eine Zeichenfolge, die von einem WPD-Treiber verwendet wird, um den Betrieb einer Geräte Dienst Methode zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="3a931-150">A string that is used by a WPD driver to identify the operation of a device-service method.</span></span> <span data-ttu-id="3a931-151">Anwendungen sollten diesen Parameter nicht direkt verwenden.</span><span class="sxs-lookup"><span data-stu-id="3a931-151">Applications should not use this parameter directly.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="3a931-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3a931-152">Requirements</span></span>



| <span data-ttu-id="3a931-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3a931-153">Requirement</span></span> | <span data-ttu-id="3a931-154">Wert</span><span class="sxs-lookup"><span data-stu-id="3a931-154">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a931-155">Header</span><span class="sxs-lookup"><span data-stu-id="3a931-155">Header</span></span><br/> | <dl> <span data-ttu-id="3a931-156"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a931-156"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a931-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a931-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a931-158">**WPD-Eigenschaften und-Attribute**</span><span class="sxs-lookup"><span data-stu-id="3a931-158">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




