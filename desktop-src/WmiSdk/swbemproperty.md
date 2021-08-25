---
description: Das SWbemProperty-Objekt stellt eine einzelne WMI-Eigenschaft eines verwalteten Objekts dar. Dieses Objekt kann nicht durch den VBScript-CreateObject-Aufruf erstellt werden.
ms.assetid: 2ddcfffa-a7b4-4fd6-926d-411de27f6212
ms.tgt_platform: multiple
title: SWbemProperty-Objekt (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty
- ISWbemProperty
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 51f4b1b22849fc5a6ae22f49c5c30411563efb9d133cf2440c301eabfde18e0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898070"
---
# <a name="swbemproperty-object"></a>SWbemProperty-Objekt

Das **SWbemProperty-Objekt** stellt eine einzelne WMI-Eigenschaft eines verwalteten Objekts dar. Dieses Objekt kann nicht durch den [VBScript-CreateObject-Aufruf](creating-an-object-using-vbscript.md) erstellt werden.

## <a name="members"></a>Member

Das **SWbemProperty-Objekt** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **SWbemProperty-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                     | Zugriffstyp           | Beschreibung                                                                                                                   |
|:-------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------|
| [**Cimtype**](swbemproperty-cimtype.md)<br/>          | Schreibgeschützt<br/>  | Typ dieser Eigenschaft.<br/>                                                                                             |
| [**Isarray**](swbemproperty-isarray.md)<br/>          | Schreibgeschützt<br/>  | Boolescher Wert, der angibt, ob diese Eigenschaft über einen Arraytyp verfügt.<br/>                                                   |
| [**IsLocal**](swbemproperty-islocal.md)<br/>          | Schreibgeschützt<br/>  | Boolescher Wert, der angibt, ob diese Eigenschaft lokal ist.<br/>                                                            |
| [**Name**](swbemproperty-name.md)<br/>                | Schreibgeschützt<br/>  | Name dieser WMI-Eigenschaft.<br/>                                                                                         |
| [**Origin**](swbemproperty-origin.md)<br/>            | Schreibgeschützt<br/>  | Enthält die ursprüngliche Klasse dieser Eigenschaft.<br/>                                                                   |
| [**Qualifikation\_**](swbemproperty-qualifiers-.md)<br/> | Schreibgeschützt<br/>  | Ein [**SWbemQualifierSet-Objekt,**](swbemqualifierset.md) das die Auflistung der Qualifizierer für diese Eigenschaft ist.<br/> |
| [**Wert**](swbemproperty-value.md)<br/>              | Lesen/Schreiben<br/> | Tatsächlicher Wert dieser Eigenschaft. Dies ist die Standardautomatisierungseigenschaft dieses Objekts.<br/>                             |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemProperty<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemProperty<br/>                                                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Skripterstellung für API-Objekte](scripting-api-objects.md)
</dt> </dl>

 

 




