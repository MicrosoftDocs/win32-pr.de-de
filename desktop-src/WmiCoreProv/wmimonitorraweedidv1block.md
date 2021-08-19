---
description: Stellt die Rohdaten aus einer E-EDID-Struktur (Enhanced Extended Display Identification Data) der Video Electronics Standard Association (VESA) dar.
ms.assetid: a51b73bb-a5f7-4e01-9c88-780105e9952b
title: WmiMonitorRawEEdidV1Block-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorRawEEdidV1Block
- WmiMonitorRawEEdidV1Block.Active
- WmiMonitorRawEEdidV1Block.InstanceName
- WmiMonitorRawEEdidV1Block.Id
- WmiMonitorRawEEdidV1Block.Type
- WmiMonitorRawEEdidV1Block.Content
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 72b82f2c6eb967f39823d5b56174bb82e7503ee56f676ffb49b65822ec435936
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118821145"
---
# <a name="wmimonitorraweedidv1block-class"></a>WmiMonitorRawEEdidV1Block-Klasse

Die WMI-Klasse **"WmiMonitorRawEEdidV1Block"** stellt die Rohdaten aus einer E-EDID-Struktur (Enhanced Extended Display Identification Data) der Video Electronics Standard Association (VESA) dar. Diese 128-Byte-Datenstruktur enthält Informationen, die die optimale Konfiguration für eine Anzeige beschreiben.

## <a name="syntax"></a>Syntax

``` syntax
class WmiMonitorRawEEdidV1Block : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
  uint8   Id;
  uint8   Type;
  uint8   Content[];
};
```

## <a name="members"></a>Member

Die **WmiMonitorRawEEdidV1Block-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **WmiMonitorRawEEdidV1Block-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Aktiv**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den aktiven Monitor an.

</dd> <dt>

**Inhalt**
</dt> <dd> <dl> <dt>

Datentyp: **uint8-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

128 Bytearray, das den unformatierten Blockinhalt enthält.

</dd> <dt>

**Id**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Identität des Datenblocks.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Name der spezifischen Überwachungsinstanz.

</dd> <dt>

**Typ**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Typ des Datenblocks. In der folgenden Tabelle sind mögliche Werte aufgeführt, die zurückgegeben werden können.



| Wert                                                                                 | Bedeutung                    |
|---------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0 (0x0)</dt> </dl>    | Uninitialized<br/>   |
| <dl> <dt>1 (0x1)</dt> </dl>    | EDID-Basisblock<br/> |
| <dl> <dt>2 (0x2)</dt> </dl>    | EDID-Blockzuordnung<br/>  |
| <dl> <dt>255 (0xFF)</dt> </dl> | Andere<br/>           |



 

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Namespace<br/>                | Root \\ wmi<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> <dt>

[**WmiGetMonitorRawEEdidV1Block**](wmigetmonitorraweedidv1block-wmimonitordescriptormethods.md)
</dt> </dl>

 

 




