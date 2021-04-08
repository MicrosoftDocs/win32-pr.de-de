---
description: Stellt die analogen Videoeingabe Parameter eines Computermonitors dar.
ms.assetid: 87d4260d-06c7-4a76-a3a1-8f6e51e23d92
title: Wmimonitoranalog gvideoinputparameams-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorAnalogVideoInputParams
- WmiMonitorAnalogVideoInputParams.Active
- WmiMonitorAnalogVideoInputParams.CompositeSyncSupported
- WmiMonitorAnalogVideoInputParams.InstanceName
- WmiMonitorAnalogVideoInputParams.SeparateSyncsSupported
- WmiMonitorAnalogVideoInputParams.SerrationOfVsyncRequired
- WmiMonitorAnalogVideoInputParams.SetupExpected
- WmiMonitorAnalogVideoInputParams.SignalLevelStandard
- WmiMonitorAnalogVideoInputParams.SyncOnGreenVideoSupported
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 900bf4353de0c81acb5aa2c69578256b0212a2c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960100"
---
# <a name="wmimonitoranalogvideoinputparams-class"></a>Wmimonitoranalog gvideoinputparameams-Klasse

Die **wmimonitoranalog** -WMI-Klasse stellt die analogen Videoeingabe Parameter eines Computermonitors dar. Die Daten in dieser Klasse entsprechen den Daten in der Videoeingabe Definition von "velectronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) Standard". Eine Instanz dieser Klasse ist nur verfügbar, wenn der Wert der **videoinputtype** -Eigenschaft der [**wmimonitorbasicdisplayparameyparameyparameyparameyparameyparameyparameyparameyparameyparamey**](wmimonitorbasicdisplayparams.md)

## <a name="syntax"></a>Syntax

``` syntax
class WmiMonitorAnalogVideoInputParams : MSMonitorClass
{
  boolean Active;
  uint8   CompositeSyncSupported;
  string  InstanceName;
  uint8   SeparateSyncsSupported;
  uint8   SerrationOfVsyncRequired;
  uint8   SetupExpected;
  uint8   SignalLevelStandard;
  uint8   SyncOnGreenVideoSupported;
};
```

## <a name="members"></a>Member

Die **wmimonitoranalog gvideoinputparameams** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **wmimonitoranalog gvideoinputparameams** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Aktiv**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den aktiven Monitor an.

</dd> <dt>

**Compositesyncsupported**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die kombinierte Synchronisierung unterstützt wird.



| Wert                                                                              | Bedeutung                                                             |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Zusammengesetzte Synchronisierung auf horizontaler Synchronisierungs Linie wird unterstützt.<br/>     |
| <dl> <dt>1 (0x1)</dt> </dl> | Zusammengesetzte Synchronisierung auf horizontaler Synchronisierungs Linie wird nicht unterstützt.<br/> |



 

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Der Name der spezifischen Monitor Instanz.

</dd> <dt>

**Separatesyncssupported**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob separate synchronisiert unterstützt werden.



| Wert                                                                              | Bedeutung                                      |
|------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Separate synchronisiert werden unterstützt.<br/>     |
| <dl> <dt>1 (0x1)</dt> </dl> | Separate synchronisiert werden nicht unterstützt.<br/> |



 

</dd> <dt>

**Serrationofvsynkrequired**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die vertikale Synchronisierungs Pulse-serration erforderlich ist.



| Wert                                                                              | Bedeutung                                                                                                             |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Wenn ein zusammengesetztes synchronisieren oder ein on-Green-on-Green-Video verwendet wird, ist die serration des vertikalen Synchronisierungs Pulse erforderlich<br/>     |
| <dl> <dt>1 (0x1)</dt> </dl> | Wenn ein zusammengesetztes synchronisieren oder ein on-Green-on-Green-Video verwendet wird, ist die serration des vertikalen Synchronisierungs Pulse nicht erforderlich.<br/> |



 

</dd> <dt>

**Setuperwartet**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob Setup erwartet wird.



| Wert                                                                              | Bedeutung                                                                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Der Monitor erwartet eine leer-zu-leer-Einrichtung oder eine socksebene gemäß dem entsprechenden Signal Stufen Standard.<br/>                      |
| <dl> <dt>1 (0x1)</dt> </dl> | Der Monitor erwartet nicht, dass ein Leerzeichen oder ein Bildschirm Bild entsprechend dem entsprechenden Signal Stufen Standard ist.<br/> |



 

</dd> <dt>

**Signallevelstandard**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Signal Level-Standard für eVC-Verbindungen (Enhanced Video Connector).



| Wert                                                                              | Bedeutung                     |
|------------------------------------------------------------------------------------|-----------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | 0,7, 0.3 \[ V\]<br/>     |
| <dl> <dt>1 (0x1)</dt> </dl> | 0.714, 0.286 \[ V\]<br/> |
| <dl> <dt>2 (0x2)</dt> </dl> | 1.0, 0,4 \[ V\]<br/>     |
| <dl> <dt>3 (0x3)</dt> </dl> | 0,7, 0,0 \[ V\]<br/>     |



 

</dd> <dt>

**SYN-greenvideosupported**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Synchronisierung bei Grün unterstützt wird



| Wert                                                                              | Bedeutung                                          |
|------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Sync on Green Video wird unterstützt.<br/>     |
| <dl> <dt>1 (0x1)</dt> </dl> | Das Synchronisieren bei einem grünen Video wird nicht unterstützt.<br/> |



 

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Namespace<br/>                | WMI-Stammdatei \\<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WMI Core. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




