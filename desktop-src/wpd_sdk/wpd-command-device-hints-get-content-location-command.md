---
description: Mit dem Befehl "WPD- \_ Befehl \_ Geräte \_ Hinweise \_ get \_ Content Location" werden \_ die Objekt-IDs von Ordnern abgerufen, die ein Objekt eines bestimmten Typs enthalten können.
ms.assetid: 85de64cc-44ee-4536-b658-49d5936351e4
title: WPD_COMMAND_DEVICE_HINTS_GET_CONTENT_LOCATION Befehl (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_DEVICE_HINTS_GET_CONTENT_LOCATION
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 22014925455979a8e84b92f1f641cd839df0b9f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368289"
---
# <a name="wpd_command_device_hints_get_content_location-command"></a>WPD- \_ Befehl \_ Geräte \_ Hinweise \_ get \_ Content Location- \_ Befehl

Mit dem Befehl " **WPD- \_ Befehl \_ Geräte \_ Hinweise \_ get \_ Content \_ Location" werden** die Objekt-IDs von Ordnern abgerufen, die ein Objekt eines bestimmten Typs enthalten können. Dieser Befehl wird für einen Client schneller bereitgestellt, um zu ermitteln, wo bestimmte Objekte von einem Gerät gespeichert werden, als durch eine Brute-Object-Enumeration.

## <a name="command-category"></a>Befehlskategorie

**WPD- \_ Kategorie \_ Geräte \_ Hinweise**

## <a name="parameters"></a>Parameter

Der Treiber erwartet die folgenden Parameter.



| Parameter                                   | VarType   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Inhaltstyp für WPD- \_ Eigenschaften \_ Geräte \_ Hinweise \_ \_ | VT \_ CLSID | Erforderlich. Der Objekttyp, für den der Aufrufer den Container finden möchte. Um beispielsweise die Ordner auf der obersten Ebene zu suchen, die zum Speichern von Bildern auf einer digitalen Kamera verwendet werden, sendet der Aufrufer das WPD- \_ \_ Inhaltstyp \_ Image. Eine Liste der Objekttypen, die von tragbaren Windows-Geräten definiert werden, finden Sie unter [Anforderungen für Objekte](requirements-for-objects.md) . |



 

## <a name="return-value"></a>Rückgabewert

Als Ergebnisse des Treibers werden erwartet:



| Ergebnis                                               | VarType     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ \_ \_ Inhalts Orte für gerätehinweise \_ für WPD-Eigenschaften** | VT \_ unbekannt | Erforderlich. Eine [**iportabledevicepropvariantcollection**](iportabledevicepropvariantcollection.md) vom Typ VT \_ LPWSTR Values, die die Objekt-IDs von Ordnern angeben, die Objekte des Typs enthalten, der durch den aufrufenden Parameter angegeben wird. Wenn keine Ordner gefunden werden, sollte dies eine leere Liste sein. Die durch das Ergebnis aufgeführten Ordner können Objekte anderer Inhaltstypen enthalten. Informationen zu Einschränkungen für Ordner finden Sie in der Eigenschaft " [Inhaltstypen für WPD- \_ Ordner \_ \_ \_ zulässig](miscellaneous-properties.md) ".<br/> |
| **WPD- \_ Eigenschaft allgemeiner \_ \_ HRESULT**                   | VT- \_ Fehler   | Erforderlich. Ein **HRESULT** , das den Erfolg oder das Fehlschlagen der Ausführung des Befehls angibt. Wenn der Aufrufer eine ungültige Anforderung sendet, sollte der Treiber **HRESULT \_ aus Win32 zurückgeben \_ (Fehler \_ nicht \_ unterstützt)** , und es ist nicht erforderlich, andere Ergebnis Werte zurückzugeben. Fehlercodes enthalten [Fehlercodes für tragbare Windows-Geräte](error-constants.md) oder andere geeignete Fehlercodes.                                                                                                                                                                            |
| **WPD- \_ Eigenschaft allgemeiner \_ \_ Treiber \_ Fehler \_ Code**       | VT \_ UI4     | Dies ist optional. Ein Treiber spezifischer Fehlercode. Dies wird in der Regel nur für Treiber Tests verwendet, oder wenn der Treiber, das Gerät und der Client verbunden sind.                                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="calling-methods"></a>Aufrufen von Methoden

Kann nur direkt mit [**iportabledevice:: Send Command**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)aufgerufen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



 

 




