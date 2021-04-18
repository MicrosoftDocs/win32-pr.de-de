---
description: Ruft die Eigenschaften ab, die von einem-Objekt unterstützt werden.
ms.assetid: 842bd4d6-0824-4597-bb5d-9ef8769055fb
title: WPD_COMMAND_OBJECT_PROPERTIES_GET_SUPPORTED Befehl (portabledevice. h)
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
ms.openlocfilehash: bd816e1dc4ce9c3cbb1fb3c0b118004983baea54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354687"
---
# <a name="wpd_command_object_properties_get_supported-command"></a>WPD- \_ Befehls \_ Objekt \_ Eigenschaften \_ Get supported- \_ Befehl

Der Befehl " **\_ \_ \_ \_ get \_ supported" (WPD Command Object Properties** ) Ruft die von einem Objekt unterstützten Eigenschaften ab.

## <a name="command-category"></a>Befehls Kategorie

**\_ \_ Objekt \_ Eigenschaften der WPD-Kategorie**

## <a name="parameters"></a>Parameter

Der Treiber erwartet den folgenden Parameter.



| Parameter                                         | VarType        | BESCHREIBUNG                                                            |
|---------------------------------------------------|----------------|------------------------------------------------------------------------|
| **Objekt-ID der WPD- \_ \_ \_ Eigenschaften \_ \_ Objekte** | **VT \_ LPWSTR** | Erforderlich. Die ID des-Objekts, das die angeforderten Eigenschaften enthält. |



 

## <a name="return-value"></a>Rückgabewert

Als Ergebnisse des Treibers werden erwartet:



| Ergebnis                                                | VarType         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Eigenschaften Schlüssel für WPD- \_ Eigenschafts \_ Objekt \_ Eigenschaften \_ \_** | **VT \_ unbekannt** | Erforderlich. Eine [**iportabledevicekeycollection**](iportabledevicekeycollection.md) -Schnittstelle, die alle unterstützten Eigenschaften angibt.                                                                                                                                                                                                            |
| **WPD- \_ Eigenschaft allgemeiner \_ \_ HRESULT**                    | **VT- \_ Fehler**   | Erforderlich. Ein **HRESULT** -Wert, der den Gesamterfolg oder Misserfolg angibt. Mögliche Ergebnis Werte sind [Fehlercodes für tragbare Windows-Geräte](error-constants.md). Wenn der Aufrufer eine ungültige Anforderung sendet, sollte der Treiber **HRESULT \_ aus Win32 zurückgeben \_ (Fehler \_ nicht \_ unterstützt)** . andernfalls ist es nicht erforderlich, einen anderen Ergebniswert zurückzugeben. |
| **WPD- \_ Eigenschaft allgemeiner \_ \_ Treiber \_ Fehler \_ Code**        | **VT \_ UI4**     | Dies ist optional. Ein Treiber spezifischer Fehlercode. Dies wird in der Regel nur für Treiber Tests oder für den Treiber, das Gerät und den Client verwendet.                                                                                                                                                                                                |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Befehle**](commands.md)
</dt> </dl>

 

 




