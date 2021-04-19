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
# <a name="event-properties"></a>Ereigniseigenschaften

Tragbare Windows-Geräte unterstützen die folgenden Ereignis Eigenschaften.



<table>
<thead>
<tr class="header">
<th>Eigenschaft</th>
<th>VarType</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>WPD_EVENT_OPTION_IS_AUTOPLAY_EVENT</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>Für die zukünftige Verwendung reserviert.</td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_OPTION_IS_BROADCAST_EVENT</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>Ein boolescher Wert, der angibt, ob das Ereignis an alle Clients übertragen wird. Clients können dieses Ereignis empfangen, indem Sie Ihren Rückruf bei <strong>iportabledevice:: Rat</strong>registrieren.<br/></td>
</tr>
<tr class="odd">
<td><strong>WPD_EVENT_PARAMETER_CHILD_HIERARCHY_CHANGED</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>Ein boolescher Wert, der angibt, ob sich die untergeordnete Hierarchie für das-Objekt geändert hat. Dieser Parameter wird verwendet, um den Aufrufer darüber zu benachrichtigen, dass einige untergeordnete Elemente für das angegebene Objekt hinzugefügt oder entfernt wurden. In der Regel wird die Hierarchie Änderung auf der Geräteseite initiiert. Clients müssen die untergeordneten Elemente dieses Ordners möglicherweise erneut aufzählen, um ihre Ansichten auf dem neuesten Stand zu halten.<br/></td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_PARAMETER_EVENT_ID</strong></td>
<td><strong>VT_CLSID</strong></td>
<td>Ein-Wert, der ein Ereignis bezeichnet.</td>
</tr>
<tr class="odd">
<td><strong>WPD_EVENT_PARAMETER_OBJECT_CREATION_COOKIE</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Das Cookie, das an einen Client zurückgegeben wird, wenn es durch Aufrufen der <a href="/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata"><strong>iportabledevicecontent:: createobjectwithpropertiesanddata</strong></a> -Methode eine Objekt Erstellung anfordert. Dieser Parameter wird hinzugefügt, um dem Aufrufer dabei zu helfen, ein Objekt hinzugefügtes Ereignis mit der Anforderung zu verknüpfen, die zum Erstellen des Objekts gesendet wurde. Der Treiber übergibt dieses Cookie zurück als <strong>WPD_PROPERTY_OBJECT_MANAGEMENT_CONTEXT</strong> Rückgabewert, wenn der <strong>WPD_COMMAND_OBJECT_MANAGEMENT_CREATE_OBJECT_WITH_PROPERTIES_AND_DATA</strong> Befehl verarbeitet wird.<br/></td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_PARAMETER_OBJECT_PARENT_PERSISTENT_UNIQUE_ID</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Ein Wert, der das übergeordnete Objekt eindeutig identifiziert. Diese Eigenschaft ähnelt <strong>WPD_OBJECT_PARENT_ID</strong>, aber diese ID ändert sich nicht zwischen den Sitzungen.</td>
</tr>
<tr class="odd">
<td><strong>WPD_EVENT_PARAMETER_OPERATION_PROGRESS</strong></td>
<td><strong>VT_UI4</strong></td>
<td>Ein-Wert, der den Status eines aktuell ausgeführten Vorgangs angibt. Der Wert dieser Eigenschaft kann zwischen 0 und 100 liegen, wobei 100 angibt, dass der Vorgang beendet ist.</td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_PARAMETER_OPERATION_STATE</strong></td>
<td><strong>VT_UI4</strong></td>
<td>Ein-Wert, der den aktuellen Zustand des Vorgangs angibt, z. b. "gestartet", "wird ausgeführt", "beendet" usw. Die möglichen Werte dieses Parameters stammen aus der in portabledevice. h definierten <strong>WPD_OPERATION_STATES</strong> Enumeration. Dabei sind folgende Werte möglich:<br/> <dl> <strong>WPD_OPERATION_STATE_UNSPECIFIED</strong><br />
<strong>WPD_OPERATION_STATE_STARTED</strong><br />
<strong>WPD_OPERATION_STATE_RUNNING</strong><br />
<strong>WPD_OPERATION_STATE_PAUSED</strong><br />
<strong>WPD_OPERATION_STATE_CANCELLED</strong><br />
<strong>WPD_OPERATION_STATE_FINISHED</strong><br />
<strong>WPD_OPERATION_STATE_ABORTED</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td><strong>WPD_EVENT_PARAMETER_PNP_DEVICE_ID</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Ein-Wert, der das Gerät angibt, von dem das Ereignis stammt. Dies ist das Gerät oder der Dienst Bezeichner, das vom PNP-System (Plug-and-Play) angegeben wird, und ist dieselbe Zeichenfolge, die in der <strong>iportabledevice:: Open</strong>-Methode oder der <a href="/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open"><strong>iportabledeviceservice:: Open</strong></a> -Methode verwendet wird.<br/></td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_PARAMETER_SERVICE_METHOD_CONTEXT</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Eine Zeichenfolge, die von einem WPD-Treiber verwendet wird, um den Betrieb einer Geräte Dienst Methode zu identifizieren. Anwendungen sollten diesen Parameter nicht direkt verwenden.</td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WPD-Eigenschaften und-Attribute**](properties-and-attributes.md)
</dt> </dl>

 

 




