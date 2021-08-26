---
description: Windows Portable Geräte unterstützen die folgenden Ereigniseigenschaften.
ms.assetid: 672b75ac-cd47-4212-a505-c220ecdf98e3
title: Ereigniseigenschaften (PortableDevice.h)
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
ms.openlocfilehash: f5220b7cd3b0acfb70788a62138a7da3a4ebac008a51e90bbc93308ae2624300
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055350"
---
# <a name="event-properties"></a>Ereigniseigenschaften

Windows Portable Geräte unterstützen die folgenden Ereigniseigenschaften.



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
<td>Ein boolescher Wert, der angibt, ob das Ereignis an alle Clients übertragen wird. Clients können dieses Ereignis empfangen, indem sie ihren Rückruf bei <strong>IPortableDevice::Advise registrieren.</strong><br/></td>
</tr>
<tr class="odd">
<td><strong>WPD_EVENT_PARAMETER_CHILD_HIERARCHY_CHANGED</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>Ein boolescher Wert, der angibt, ob die untergeordnete Hierarchie für das -Objekt geändert wurde. Dieser Parameter wird verwendet, um den Aufrufer darüber zu benachrichtigen, dass einige der für das angegebene Objekt erstellten objekte hinzugefügt oder entfernt wurden. In der Regel wird die Hierarchieänderung auf geräteseitiger Seite initiiert. Clients müssen möglicherweise die unteren Ordner neu aufzählen, um ihre Ansichten auf dem neuesten Stand zu halten.<br/></td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_PARAMETER_EVENT_ID</strong></td>
<td><strong>VT_CLSID</strong></td>
<td>Ein -Wert, der ein Ereignis identifiziert.</td>
</tr>
<tr class="odd">
<td><strong>WPD_EVENT_PARAMETER_OBJECT_CREATION_COOKIE</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Das Cookie, das an einen Client übergeben wird, wenn er eine Objekterstellung durch Aufrufen der <a href="/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata"><strong>IPortableDeviceContent::CreateObjectWithPropertiesAndData-Methode anfing.</strong></a> Dieser Parameter wird der Einfachheit halber hinzugefügt, um dem Aufrufer zu helfen, ein vom Objekt hinzugefügtes Ereignis mit der Anforderung zu verknüpfen, die er zum Erstellen des Objekts gesendet hat. Der Treiber übergibt dieses Cookie als WPD_PROPERTY_OBJECT_MANAGEMENT_CONTEXT <strong>Rückgabewert</strong> zurück, wenn der <strong>WPD_COMMAND_OBJECT_MANAGEMENT_CREATE_OBJECT_WITH_PROPERTIES_AND_DATA</strong> verarbeitet wird.<br/></td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_PARAMETER_OBJECT_PARENT_PERSISTENT_UNIQUE_ID</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Ein -Wert, der das übergeordnete Objekt eindeutig identifiziert. Diese Eigenschaft ähnelt <strong>WPD_OBJECT_PARENT_ID</strong>, aber diese ID ändert sich nicht zwischen Sitzungen.</td>
</tr>
<tr class="odd">
<td><strong>WPD_EVENT_PARAMETER_OPERATION_PROGRESS</strong></td>
<td><strong>VT_UI4</strong></td>
<td>Ein -Wert, der den Status eines derzeit ausgeführten Vorgangs angibt. Der Wert dieser Eigenschaft kann zwischen 0 und 100 liegen, und 100 gibt an, dass der Vorgang abgeschlossen ist.</td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_PARAMETER_OPERATION_STATE</strong></td>
<td><strong>VT_UI4</strong></td>
<td>Ein -Wert, der den aktuellen Status des Vorgangs angibt, z. B. gestartet, ausgeführt, beendet und so weiter. Die möglichen Werte dieses Parameters sind aus der WPD_OPERATION_STATES <strong>enumeration,</strong> die in PortableDevice.h definiert ist. Mögliche Werte:<br/> <dl> <strong>WPD_OPERATION_STATE_UNSPECIFIED</strong><br />
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
<td>Ein -Wert, der das Gerät angibt, von dem das Ereignis stammt. Dies ist die Geräte- oder Dienst-ID, die vom Plug-and-Play-System (PnP) angegeben wird, und ist die gleiche Zeichenfolge, die in den <strong>Methoden IPortableDevice::Open</strong>oder <a href="/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open"><strong>IPortableDeviceService::Open</strong></a> verwendet wird.<br/></td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_PARAMETER_SERVICE_METHOD_CONTEXT</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Eine Zeichenfolge, die von einem WPD-Treiber verwendet wird, um den Vorgang einer device-service-Methode zu identifizieren. Anwendungen sollten diesen Parameter nicht direkt verwenden.</td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WPD-Eigenschaften und -Attribute**](properties-and-attributes.md)
</dt> </dl>

 

 




