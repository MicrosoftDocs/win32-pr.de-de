---
title: Vordefinierte Listen Attribute ("tsatyd. h")
description: Die folgenden Werte identifizieren Listen Attribute, die mit der ITF Context getappproperty-Methode abgerufen werden. Das Datenformat und der Inhalt der einzelnen Eigenschaftentypen sind eingeschlossen.
ms.assetid: 9a9e1912-51c0-40e0-9e3a-b84ea7077dbe
keywords:
- Vordefinierte Listen Attribute Text Dienst-Framework
topic_type:
- apiref
api_name:
- Predefined List Attributes
api_location:
- TsAttrid.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81ade2403e124b934c6872f39c01fc7fc1ea6f6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105386"
---
# <a name="predefined-list-attributes"></a>Vordefinierte Listen Attribute

Die folgenden Werte identifizieren Listen Attribute, die mit der [ITF context:: getappproperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) -Methode abgerufen werden. Das Datenformat und der Inhalt der einzelnen Eigenschaftentypen sind eingeschlossen.

## <a name="properties"></a>Eigenschaften



| Eigenschaft                          | BESCHREIBUNG                                                                                     |
|-----------------------------------|-------------------------------------------------------------------------------------------------|
| Liste der "Tsat-ID" \_                    | Nicht verwendet.                                                                                       |
| "- \_ \_ Levelliste"        | Enthält die Index Ebene der Liste. 1 ist die äußerste Ebene, 2 ist die nächste Ebene usw. |
| Der Typ der der- \_ Liste. \_              | Nicht verwendet.                                                                                       |
| Der Typ "" der "der- \_ \_ Typ" \_      | Enthält einen Wert ungleich 0 (null), wenn die Liste eine arabische Zahlenliste ist, andernfalls NULL.               |
| Aufzählungs Zeichen- \_ Aufzählungs Zeichen \_ \_      | Enthält einen Wert ungleich 0 (null), wenn die Liste eine Auflistungs Liste ist, andernfalls NULL.                      |
| In der \_ Liste der \_ vom Typ "". \_ | Enthält einen Wert ungleich 0 (null), wenn die Liste eine durch klein geschriebene Liste ist oder andernfalls 0 (null) ist.            |
| Der-Typ der der-Gruppe ist " \_ \_ \_ LowerRoman"  | Enthält einen Wert ungleich 0 (null), wenn die Liste eine klein geschriebene römische Ziffern Liste ist, andernfalls NULL.       |
| Der Typ "der" \_ \_ \_ | Enthält einen Wert ungleich 0 (null), wenn es sich bei der Liste um eine schreibgeschützte Großbuchstaben oder andernfalls um NULL handelt.          |
| Der-Typ der der-Klasse, \_ \_ \_ UpperRoman  | Enthält einen Wert ungleich 0 (null), wenn die Liste eine römische Zahlenliste in Großbuchstaben oder andernfalls NULL ist.      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Verteilbare Komponente<br/>          | TSF 1,0 unter Windows 2000 Professional<br/>                                       |
| Header<br/>                   | <dl> <dt>"Tsatphd. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ITF context:: getappproperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty)
</dt> </dl>

 

