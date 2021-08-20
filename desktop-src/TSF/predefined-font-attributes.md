---
title: Vordefinierte Schriftartattribute (TsAttrid.h)
description: Die folgenden Werte identifizieren Schriftartattribute, die mit der ITfContext GetAppProperty-Methode abgerufen werden. Das Datenformat und der Inhalt jedes Eigenschaftstyps sind enthalten.
ms.assetid: 8d73c258-77d5-46db-9d31-ac41d9e7acb3
keywords:
- Vordefinierte Schriftartattribute Textdienstframework
topic_type:
- apiref
api_name:
- Predefined Font Attributes
api_location:
- TsAttrid.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fb586258bb6eca1639121fa3b33a26ad560f00bb9b002c347a4e026a53442f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117951946"
---
# <a name="predefined-font-attributes"></a>Vordefinierte Schriftartattribute

Die folgenden Werte identifizieren Schriftartattribute, die mit der [ITfContext::GetAppProperty-Methode](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) abgerufen werden. Das Datenformat und der Inhalt jedes Eigenschaftstyps sind enthalten.

## <a name="properties"></a>Eigenschaften



| Eigenschaft                                                 | Beschreibung                                                                                                                 |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| **\_TSATTRID-Schriftart**                                       | Wird nicht verwendet.                                                                                                                   |
| **TSATTRID \_ Font \_ FaceName**                             | Enthält den Gesichtsnamen der Textschriftart.                                                                                    |
| **TSATTRID \_ Font \_ SizePts**                              | Enthält die Punktgröße der Textschriftart.                                                                                   |
| **\_TSATTRID-Schriftschnitt \_**                                | Wird nicht verwendet.                                                                                                                   |
| **ANIMATION DES \_ TSATTRID-Schriftschnitts \_ \_**                     | Wird nicht verwendet.                                                                                                                   |
| **TSATTRID \_ Font \_ Style \_ Animation \_ BlinkingBackground** | Enthält einen Wert ungleich 0 (null), wenn der Text über die angegebene Animation verfügt, andernfalls 0 (null).                                         |
| **TSATTRID \_ Font \_ Style \_ Animation \_ LasVegasLights**     | Enthält einen Wert ungleich 0 (null), wenn der Text über die angegebene Animation verfügt, andernfalls 0 (null).                                         |
| **TSATTRID \_ Font \_ Style \_ Animation \_ MarchingBlackAnts**  | Enthält einen Wert ungleich 0 (null), wenn der Text über die angegebene Animation verfügt, andernfalls 0 (null).                                         |
| **TSATTRID \_ Font \_ Style \_ Animation \_ MarchingRedAnts**    | Enthält einen Wert ungleich 0 (null), wenn der Text über die angegebene Animation verfügt, andernfalls 0 (null).                                         |
| **TSATTRID \_ Font \_ Style \_ Animation \_ Shimmer**            | Enthält einen Wert ungleich 0 (null), wenn der Text über die angegebene Animation verfügt, andernfalls 0 (null).                                         |
| **TSATTRID \_ Font \_ Style \_ Animation \_ SparkleText**        | Enthält einen Wert ungleich 0 (null), wenn der Text über die angegebene Animation verfügt, andernfalls 0 (null).                                         |
| **TSATTRID \_ Font \_ Style \_ Animation \_ WipeDown**           | Enthält einen Wert ungleich 0 (null), wenn der Text über die angegebene Animation verfügt, andernfalls 0 (null).                                         |
| **TSATTRID \_ Font \_ Style \_ Animation \_ WipeRight**          | Enthält einen Wert ungleich 0 (null), wenn der Text über die angegebene Animation verfügt, andernfalls 0 (null).                                         |
| **HINTERGRUNDFARBE DES \_ TSATTRID-Schriftschnitts \_ \_**               | Enthält den RGB-Wert des Texthintergrunds. Enthält 0xFF000000, wenn die Textfarbe automatisch ist.                          |
| **\_TSATTRID-Schriftschnitt \_ \_ Blink**                         | Enthält einen Wert ungleich 0 (null), wenn der Text blinkt, andernfalls 0 (null).                                                         |
| **\_TSATTRID-Schriftschnitt \_ \_ Fett**                          | Enthält einen Wert ungleich 0 (null), wenn der Text fett oder 0 (null) ist.                                                             |
| **Großschreibung des \_ TSATTRID-Schriftschnitts \_ \_**                    | Enthält einen Wert ungleich 0 (null), wenn der Text großgeschrieben wird oder andernfalls 0 (null).                                                      |
| **Schriftschnittfarbe "TSATTRID" \_ \_ \_**                         | Enthält den RGB-Wert der Textfarbe. Enthält 0xFF000000, wenn die Textfarbe automatisch ist.                               |
| **\_TSATTRID-Schriftschnitt- \_ \_ Emboss**                        | Enthält einen Wert ungleich 0 (null), wenn der Text eingebettet ist oder andernfalls 0 (null).                                                         |
| **TSATTRID \_ Font \_ Style \_ (Tsattrid-Schriftschnitt)**                       | Enthält einen Wert ungleich 0 (null), wenn der Text verschoben wird, andernfalls 0 (null).                                                         |
| **HÖHE DES \_ TSATTRID-Schriftschnitts \_ \_**                        | Enthält die Schrifthöhe. Weitere Informationen finden Sie unter dem **lfHeight-Member** der LOGFONT-Struktur.                       |
| **\_TSATTRID-Schriftschnitt \_ \_ ausgeblendet**                        | Enthält einen Wert ungleich 0 (null), wenn der Text ausgeblendet ist oder andernfalls 0 (null).                                                           |
| **\_TSATTRID-Schriftschnitt \_ \_ italisch**                        | Enthält einen Wert ungleich 0 (null), wenn der Text italisch oder andernfalls 0 (null) ist.                                                           |
| **TSATTRID \_ Font \_ Style \_ Kerning**                       | Enthält die minimale Kerninggröße. Weitere Informationen finden Sie unter ITextFont::GetKerning.                                         |
| **\_TSATTRID-Schriftschnitt \_ \_ In Kleinbuchstaben**                     | Enthält einen Wert ungleich 0 (null), wenn der Text klein geschrieben ist oder andernfalls 0 (null).                                                        |
| **\_Umrandete TSATTRID-Schriftschnitt \_ \_**                      | Enthält einen Wert ungleich 0 (null), wenn der Text umrandt ist, oder 0 (null).                                                         |
| **\_ \_ \_ TSATTRID-Schriftschnittüberlinie**                      | Enthält einen Wert ungleich 0 (null), wenn der Text über- oder null ist.                                                        |
| **TSATTRID \_ Font \_ Style \_ Overline \_ Double**              | Enthält einen Wert ungleich 0 (null), wenn der Text doppelt über- oder null ist.                                                 |
| **TSATTRID \_ Font \_ Style \_ Overline \_ Single**              | Enthält einen Wert ungleich 0 (null), wenn der Text single overlined oder andernfalls 0 (null) ist.                                                 |
| **\_ \_ \_ TSATTRID-Schriftschnittposition**                      | Enthält die Schriftartposition.                                                                                                 |
| **GESCHÜTZTER \_ TSATTRID-Schriftschnitt \_ \_**                     | Enthält einen Wert ungleich 0 (null), wenn der Text geschützt ist, andernfalls 0 (null).                                                        |
| **SCHATTEN IM \_ TSATTRID-Schriftschnitt \_ \_**                        | Enthält einen Wert ungleich 0 (null), wenn der Text überschatten wird oder andernfalls 0 (null).                                                         |
| **\_ \_ TSATTRID-Schriftschnitt \_ SmallCaps**                     | Enthält einen Wert ungleich 0 (null), wenn der Text klein geschrieben ist oder andernfalls 0 (null).                                                        |
| **\_TSATTRID-Schriftschnittabstand \_ \_**                       | Enthält den Schriftabstand.                                                                                                  |
| **\_TSATTRID-Schriftschnitt \_ \_ durchgestrichen**                 | Wird nicht verwendet.                                                                                                                   |
| **TSATTRID \_ Font \_ Style \_ Strikethrough \_ Double**         | Enthält einen Wert ungleich 0 (null), wenn der Text doppelt durchgestrichen ist oder andernfalls 0 (null).                                             |
| **TSATTRID \_ Font \_ Style \_ Strikethrough \_ Single**         | Enthält einen Wert ungleich 0 (null), wenn der Text durchgestrichen ist oder andernfalls 0 (null).                                             |
| **TSATTRID \_ Font \_ Style \_ Subscript**                     | Enthält einen Wert ungleich 0 (null), wenn der Text tiefgestellt ist oder andernfalls 0 (null).                                                        |
| **TSATTRID \_ Font \_ Style \_ Superscript**                   | Enthält einen Wert ungleich 0 (null), wenn der Text superscript oder 0 (null) ist.                                                      |
| **\_TSATTRID-Schriftschnitt \_ \_ unterstrichen**                     | Enthält einen Wert ungleich 0 (null), wenn der Text unterstrichen ist, andernfalls 0 (null).                                                       |
| **TSATTRID \_ Font \_ Style \_ Underline \_ Double**             | Enthält einen Wert ungleich 0 (null), wenn der Text doppelt unterstrichen ist oder andernfalls 0 (null).                                                |
| **TSATTRID \_ Font \_ Style \_ Underline \_ Single**             | Enthält einen Wert ungleich 0 (null), wenn der Text einfach unterstrichen ist oder andernfalls 0 (null).                                                |
| **\_TSATTRID-Schriftschnitt \_ \_ in Großbuchstaben**                     | Enthält einen Wert ungleich 0 (null), wenn der Text groß geschrieben ist oder andernfalls 0 (null).                                                        |
| **TSATTRID \_ \_ \_ Schriftschnittgewichtung**                        | Enthält die Schriftgradung. Weitere Informationen zu möglichen Werten finden Sie unter dem **lfWeight-Member** der LOGFONT-Struktur. |



 

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

 

