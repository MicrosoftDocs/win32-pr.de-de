---
description: Stellt erweiterte Funktionen für SWbemObject zur Verfügung. Wie SWbemObject können die Methoden dieses erweiterten Objekts von allen WMI-Objekten verwendet werden.
ms.assetid: 944d4cdc-ad35-4b53-b755-f10131a087fb
ms.tgt_platform: multiple
title: SWbemObjectEx-Objekt (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx
- SetFromText_
- ISWbemObjectEx
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 642b76cde4f4e27979dae0e930ec987dc9a02d36aa8d17c7dcdd9b8785204ac9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860150"
---
# <a name="swbemobjectex-object"></a>SWbemObjectEx-Objekt

Das **SWbemObjectEx-Objekt** stellt erweiterte Funktionen für [**SWbemObject zur Verfügung.**](swbemobject.md) Wie **SWbemObject** können die Methoden dieses erweiterten Objekts von allen WMI-Objekten verwendet werden. Dieses Objekt kann nicht durch den VBScript [CreateObject-Aufruf erstellt](/previous-versions//xzysf6hc(v=vs.85)) werden.

## <a name="members"></a>Member

Das **SWbemObjectEx-Objekt** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **SWbemObjectEx-Objekt** verfügt über diese Methoden.



| Methode                                      | BESCHREIBUNG                                                              |
|:--------------------------------------------|:-------------------------------------------------------------------------|
| [**GetText\_**](swbemobjectex-gettext-.md) | Gibt eine Textdatei zurück, die den Inhalt eines Objekts in XML zeigt.<br/> |
| [**Aktualisieren\_**](swbemobjectex-refresh-.md) | Aktualisiert Daten in einem -Objekt.<br/>                                  |
| **SetFromText\_**                           | Für die zukünftige Verwendung reserviert.<br/>                                      |



 

### <a name="properties"></a>Eigenschaften

Das **SWbemObjectEx-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                                 | Zugriffstyp           | BESCHREIBUNG                                                                                                                                              |
|:-------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SystemEigenschaften\_**](swbemobjectex-systemproperties-.md)<br/> | Lesen/Schreiben<br/> | Ein [**SWbemPropertySet-Objekt,**](swbempropertyset.md) das die Auflistung der Systemeigenschaften enthält, die für **SWbemObjectEx gelten.**<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectEx<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemObjectEx<br/>                                                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Skripterstellung für API-Objekte](scripting-api-objects.md)
</dt> <dt>

[**Swbemobject**](swbemobject.md)
</dt> <dt>

[WbemObjectTextFormatEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum)
</dt> </dl>

 

