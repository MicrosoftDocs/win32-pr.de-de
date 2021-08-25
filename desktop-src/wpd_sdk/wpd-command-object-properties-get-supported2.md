---
description: Ruft die eigenschaften ab, die von einem -Objekt unterstützt werden.
ms.assetid: 842bd4d6-0824-4597-bb5d-9ef8769055fb
title: WPD_COMMAND_OBJECT_PROPERTIES_GET_SUPPORTED Befehl (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_OBJECT_PROPERTIES_GET_SUPPORTED
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 5020494658f380abc465a9059544131174edc8c417f69f6322636e6c9d4170d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119703980"
---
# <a name="wpd_command_object_properties_get_supported-command"></a>WPD \_ COMMAND \_ OBJECT \_ PROPERTIES \_ GET \_ SUPPORTED Command

Mit **dem Befehl WPD COMMAND OBJECT \_ PROPERTIES GET \_ \_ \_ \_ SUPPORTED** werden die eigenschaften abgerufen, die von einem -Objekt unterstützt werden.

## <a name="command-category"></a>Befehlskategorie

**WPD \_ CATEGORY \_ OBJECT \_ PROPERTIES**

## <a name="parameters"></a>Parameter

Der Treiber erwartet den folgenden Parameter.



| Parameter                                         | VarType        | Beschreibung                                                            |
|---------------------------------------------------|----------------|------------------------------------------------------------------------|
| **WPD \_ PROPERTY \_ OBJECT \_ PROPERTIES \_ OBJECT \_ ID** | **VT \_ LPWSTR** | Erforderlich. Die ID des Objekts, das die angeforderten Eigenschaften enthält. |



 

## <a name="return-value"></a>Rückgabewert

Als Ergebnisse des Treibers werden erwartet:



| Ergebnis                                                | VarType         | Beschreibung                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_EIGENSCHAFTENEIGENSCHAFTEN-SCHLÜSSEL \_ DES WPD-EIGENSCHAFTENOBJEKTS \_ \_ \_** | **VT \_ UNKNOWN** | Erforderlich. Eine [**IPortableDeviceKeyCollection-Schnittstelle,**](iportabledevicekeycollection.md) die alle unterstützten Eigenschaften angibt.                                                                                                                                                                                                            |
| **\_WPD-EIGENSCHAFT \_ COMMON \_ HRESULT**                    | **\_VT-FEHLER**   | Erforderlich. Ein **HRESULT-Wert,** der den Gesamterfolg oder -fehler angibt. Mögliche Ergebniswerte sind Windows [Fehlercodes für portable Geräte.](error-constants.md) Wenn der Aufrufer eine ungültige Anforderung vorgibt, sollte der Treiber **HRESULT \_ FROM \_ WIN32 (ERROR \_ NOT \_ SUPPORTED)** zurückgeben, andernfalls muss kein anderer Ergebniswert zurückgegeben werden. |
| **\_WPD-EIGENSCHAFT \_ COMMON DRIVER \_ ERROR \_ \_ CODE**        | **VT \_ UI4**     | Optional. Ein treiberspezifischer Fehlercode. Dies wird in der Regel nur für Treibertests verwendet, oder wenn Treiber, Gerät und Client zusammen entworfen werden.                                                                                                                                                                                                |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Befehle**](commands.md)
</dt> </dl>

 

 




