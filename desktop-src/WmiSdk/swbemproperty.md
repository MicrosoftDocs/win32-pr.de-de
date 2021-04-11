---
description: Das taubemproperty-Objekt stellt eine einzelne WMI-Eigenschaft eines verwalteten Objekts dar. Dieses Objekt kann nicht durch den VBScript-Befehl "up-Object" erstellt werden.
ms.assetid: 2ddcfffa-a7b4-4fd6-926d-411de27f6212
ms.tgt_platform: multiple
title: Taubemproperty-Objekt (wbemdisp. h)
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
ms.openlocfilehash: 9c71db4063f5de6b48b2e8213f21ca1320a880fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218482"
---
# <a name="swbemproperty-object"></a>Swap Property-Objekt

Das **taubemproperty** -Objekt stellt eine einzelne WMI-Eigenschaft eines verwalteten Objekts dar. Dieses Objekt kann nicht durch den VBScript-Befehl "up- [Object](creating-an-object-using-vbscript.md) " erstellt werden.

## <a name="members"></a>Member

Das Objekt " **Swap Property** " verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **taubemproperty** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                     | Zugriffstyp           | BESCHREIBUNG                                                                                                                   |
|:-------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------|
| [**CimType**](swbemproperty-cimtype.md)<br/>          | Schreibgeschützt<br/>  | Der Typ dieser Eigenschaft.<br/>                                                                                             |
| [**IsArray**](swbemproperty-isarray.md)<br/>          | Schreibgeschützt<br/>  | Boolescher Wert, der angibt, ob diese Eigenschaft einen Arraytyp aufweist.<br/>                                                   |
| [**IsLocal**](swbemproperty-islocal.md)<br/>          | Schreibgeschützt<br/>  | Boolescher Wert, der angibt, ob diese Eigenschaft lokal ist.<br/>                                                            |
| [**Name**](swbemproperty-name.md)<br/>                | Schreibgeschützt<br/>  | Der Name dieser WMI-Eigenschaft.<br/>                                                                                         |
| [**Entstehungs**](swbemproperty-origin.md)<br/>            | Schreibgeschützt<br/>  | Enthält die Ursprungs Klasse dieser Eigenschaft.<br/>                                                                   |
| [**Qualifikation\_**](swbemproperty-qualifiers-.md)<br/> | Schreibgeschützt<br/>  | Ein " [**taubemqualifierset**](swbemqualifierset.md) "-Objekt, das die Auflistung der Qualifizierer für diese Eigenschaft ist.<br/> |
| [**Wert**](swbemproperty-value.md)<br/>              | Lesen/Schreiben<br/> | Tatsächlicher Wert dieser Eigenschaft. Dies ist die standardmäßige Automatisierungs Eigenschaft dieses Objekts.<br/>                             |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Swap-Eigenschaft<br/>                                                         |
| IID<br/>                      | IID \_ iswbemproperty<br/>                                                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[API-Skript Objekte](scripting-api-objects.md)
</dt> </dl>

 

 




