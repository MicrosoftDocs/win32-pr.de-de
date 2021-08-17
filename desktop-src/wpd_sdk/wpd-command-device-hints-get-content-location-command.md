---
description: Der Befehl WPD \_ COMMAND \_ DEVICE \_ HINTS GET CONTENT LOCATION ruft \_ \_ die \_ Objekt-IDs von Ordnern ab, die ein Objekt eines angegebenen Typs enthalten können.
ms.assetid: 85de64cc-44ee-4536-b658-49d5936351e4
title: WPD_COMMAND_DEVICE_HINTS_GET_CONTENT_LOCATION-Befehl (PortableDevice.h)
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
ms.openlocfilehash: 7e893df2a67aebcbd271d6df201e7e199b3c3326371e918b02b5c574ebba5763
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118026813"
---
# <a name="wpd_command_device_hints_get_content_location-command"></a>WPD \_ COMMAND \_ DEVICE \_ HINTS \_ GET \_ CONTENT \_ LOCATION Command

Der Befehl **WPD \_ COMMAND DEVICE \_ \_ HINTS GET CONTENT \_ \_ \_ LOCATION** ruft die Objekt-IDs von Ordnern ab, die ein Objekt eines angegebenen Typs enthalten können. Dieser Befehl wird für einen Client schneller bereitgestellt, um zu ermitteln, wo ein Gerät bestimmte Objekte speichert, als durch brute-Objektenumeration.

## <a name="command-category"></a>Befehlskategorie

**GERÄTEHINWEISE \_ DER WPD-KATEGORIE \_ \_**

## <a name="parameters"></a>Parameter

Der Treiber erwartet die folgenden Parameter.



| Parameter                                   | VarType   | Beschreibung                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ \_ WPD-EIGENSCHAFTENGERÄTEHINWEISE \_ \_ INHALTSTYP | VT \_ CLSID | Erforderlich. Der Objekttyp, für den der Aufrufer den Container suchen möchte. Um beispielsweise die Ordner der obersten Ebene zu finden, die zum Speichern von Bildern auf einer Digitalkamera verwendet werden, sendet der Aufrufer WPD \_ CONTENT \_ TYPE \_ IMAGE. Eine Liste der Objekttypen, die von Windows Portable Devices definiert werden, finden Sie unter [Anforderungen für](requirements-for-objects.md) Objekte. |



 

## <a name="return-value"></a>Rückgabewert

Als Ergebnisse des Treibers werden erwartet:



| Ergebnis                                               | VarType     | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_WPD-EIGENSCHAFTENGERÄTEHINWEISE \_ \_ ZU \_ \_ INHALTSSPEICHERORTEN** | VT \_ UNKNOWN | Erforderlich. Eine [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) vom Typ VT \_ LPWSTR-Werte, die die Objekt-IDs von Ordnern angeben, die Objekte des vom aufrufenden Parameter angegebenen Typs enthalten. Wenn keine Ordner gefunden werden, sollte dies eine leere Liste sein. Die durch das Ergebnis angegebenen Ordner dürfen Objekte anderer Inhaltstypen enthalten oder nicht. Informationen zu Ordnereinschränkungen finden Sie in der [WPD \_ FOLDER CONTENT \_ TYPES \_ \_ ALLOWED-Eigenschaft.](miscellaneous-properties.md)<br/> |
| **\_WPD-EIGENSCHAFT \_ COMMON \_ HRESULT**                   | \_VT-FEHLER   | Erforderlich. Ein **HRESULT,** das den Erfolg oder Fehler bei der Verarbeitung des Befehls angibt. Wenn der Aufrufer eine ungültige Anforderung stellt, sollte der Treiber **HRESULT \_ FROM \_ WIN32(ERROR \_ NOT \_ SUPPORTED)** zurückgeben und muss keine anderen Ergebniswerte zurückgeben. Fehlercodes umfassen [Windows Fehlercodes für portable Geräte](error-constants.md) oder andere geeignete Fehlercodes.                                                                                                                                                                            |
| **ALLGEMEINER \_ \_ \_ \_ TREIBERFEHLERCODE \_ FÜR WPD-EIGENSCHAFTEN**       | VT \_ UI4     | Optional. Ein treiberspezifischer Fehlercode. Dies wird in der Regel nur für Treibertests verwendet, oder wenn Treiber, Gerät und Client alle zusammen entworfen wurden.                                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="calling-methods"></a>Aufrufen von Methoden

Kann nur direkt mit [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)aufgerufen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



 

 




