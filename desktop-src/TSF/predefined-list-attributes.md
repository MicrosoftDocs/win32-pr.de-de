---
title: Vordefinierte Listenattribute (TsAttrid.h)
description: Die folgenden Werte identifizieren Listenattribute, die mit der ITfContext GetAppProperty-Methode ermittelt wurden. Das Datenformat und der Inhalt der einzelnen Eigenschaftentypen sind enthalten.
ms.assetid: 9a9e1912-51c0-40e0-9e3a-b84ea7077dbe
keywords:
- Vordefinierte Listenattribute Textdienstframework
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
ms.openlocfilehash: 4b1242a5483b00a67784486c4a53b6f312d5af6e60d1d3676f09d5f357f9081e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117951875"
---
# <a name="predefined-list-attributes"></a>Vordefinierte Listenattribute

Die folgenden Werte identifizieren Listenattribute, die mit der [ITfContext::GetAppProperty-Methode erhalten](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) wurden. Das Datenformat und der Inhalt der einzelnen Eigenschaftentypen sind enthalten.

## <a name="properties"></a>Eigenschaften



| Eigenschaft                          | Beschreibung                                                                                     |
|-----------------------------------|-------------------------------------------------------------------------------------------------|
| TSATTRID-Liste \_                    | Wird nicht verwendet.                                                                                       |
| TSATTRID \_ List \_ LevelIndel        | Enthält die Indexebene der Liste. 1 ist die äußerste Ebene, 2 ist die nächste Ebene und so weiter. |
| \_TSATTRID-Listentyp \_              | Wird nicht verwendet.                                                                                       |
| TSATTRID-Listentyp \_ \_ \_ Arabisch      | Enthält einen Wert ungleich 0 (null), wenn die Liste eine arabische Zahlenliste oder andernfalls 0 (null) ist.               |
| TSATTRID-Listentyp \_ \_ \_ Aufzählungszeichen      | Enthält einen Wert ungleich 0 (null), wenn die Liste eine Aufzählung oder andernfalls 0 (null) ist.                      |
| \_TSATTRID-Listentyp \_ \_ LowerLetter | Enthält einen Wert ungleich 0 (null), wenn es sich bei der Liste um eine Liste mit Kleinbuchstaben oder andernfalls um 0 (null) handelt.            |
| \_TSATTRID-Listentyp \_ Lower \_ Dateityp  | Enthält einen Wert ungleich 0 (null), wenn es sich bei der Liste um eine Kleinbuchstabe oder andernfalls um 0 (null) handelt.       |
| TSATTRID-Listentyp \_ \_ \_ UpperLetter | Enthält einen Wert ungleich 0 (null), wenn die Liste eine Liste mit Großbuchstaben oder andernfalls 0 (null) ist.          |
| TSATTRID-Listentyp \_ \_ Upper \_ Dateityp  | Enthält einen Wert ungleich 0 (null), wenn es sich bei der Liste um eine liste mit groß geschriebenen Zahlen handelt, andernfalls 0 (null).      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Verteilbare Komponente<br/>          | TSF 1.0 auf Windows 2000 Professional<br/>                                       |
| Header<br/>                   | <dl> <dt>TsAttrid.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ITfContext::GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty)
</dt> </dl>

 

