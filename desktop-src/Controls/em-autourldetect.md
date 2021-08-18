---
title: EM_AUTOURLDETECT (Richedit.h)
description: Aktiviert oder deaktiviert die automatische Erkennung von Links durch ein Rich-Edit-Steuerelement.
ms.assetid: 6970ff36-ff3f-4413-a471-9389a76c8f38
keywords:
- EM_AUTOURLDETECT von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- EM_AUTOURLDETECT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e7c53df29b1d106c537543983f1734aef7facaaca5d0965c3a2588f285a7391
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049430"
---
# <a name="em_autourldetect-message"></a>EM \_ AUTOURLDETECT-Nachricht

Aktiviert oder deaktiviert die automatische Erkennung von Links durch ein Rich-Edit-Steuerelement.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Geben Sie 0 an, um die automatische Linkerkennung zu deaktivieren, oder einen der folgenden Werte, um verschiedene Arten der Erkennung zu aktivieren.



| Wert                                                                                                                                                                                       | Bedeutung                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AURL_DISABLEMIXEDLGC"></span><span id="aurl_disablemixedlgc"></span><dl> <dt>**AURL \_ DISABLEMIXEDLGC**</dt> </dl>          | **Windows 8**: Deaktivieren Sie die Erkennung von Domänennamen, die Bezeichnungen mit Zeichen enthalten, die zu mehr als einem der folgenden Skripts gehören: Lateinisch, Griechisch und Kyrillisch. <br/> |
| <span id="AURL_ENABLEDRIVELETTERS"></span><span id="aurl_enabledriveletters"></span><dl> <dt>**AURL \_ ENABLEDRIVELETTERS**</dt> </dl> | **Windows 8**: Erkennt Dateinamen, die über eine führende Laufwerkspezifikation verfügen, z. B. c: \\ temp.<br/>                                                                           |
| <span id="AURL_ENABLEEA"></span><span id="aurl_enableea"></span><dl> <dt>**AURL \_ ENABLEEA**</dt> </dl>                               | Dieser Wert ist veraltet. verwenden **Sie stattdessen AURL \_ ENABLERLRLS.**<br/>                                                                                                            |
| <span id="AURL_ENABLEEAURLS"></span><span id="aurl_enableeaurls"></span><dl> <dt>**AURL \_ ENABLERLRLS**</dt> </dl>                   | Erkennen von URLs, die ostasiatische Zeichen enthalten. <br/>                                                                                                                      |
| <span id="AURL_ENABLEEMAILADDR"></span><span id="aurl_enableemailaddr"></span><dl> <dt>**AURL \_ ENABLEEMAILADDR**</dt> </dl>          | **Windows 8:** Erkennen von E-Mail-Adressen.<br/>                                                                                                                                |
| <span id="AURL_ENABLETELNO"></span><span id="aurl_enabletelno"></span><dl> <dt>**AURL \_ ENABLETELNO**</dt> </dl>                      | **Windows 8**: Telefonnummern erkennen.<br/>                                                                                                                              |
| <span id="AURL_ENABLEURL"></span><span id="aurl_enableurl"></span><dl> <dt>**AURL \_ ENABLEURL**</dt> </dl>                            | **Windows 8**: Erkennt URLs, die den Pfad enthalten.<br/>                                                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter bestimmt die URL-Schemas, die erkannt werden, **wenn AURL \_ ENABLEURL** aktiv ist. Wenn *lParam* NULL ist, wird die Standardschemanamenliste verwendet (siehe Hinweise). Alternativ kann *lParam* auf eine auf NULL terminierte Zeichenfolge verweisen, die aus bis zu 50 auf Doppelpunkt terminierten Schemanamen besteht, die die Standardschemanamenliste absetzen. Die Zeichenfolge könnte beispielsweise "news:http:ftp:telnet:" sein. Die Schemanamenssyntax ist im Dokument [Uniform Resource Identifiers (URI): Generische Syntax]( https://www.ietf.org/rfc/rfc2396.txt) auf der IETF-Website (Internet Engineering Task Force) definiert. Insbesondere kann ein Schemaname bis zu 13 Zeichen (einschließlich des Doppelpunkts) enthalten, mit einem ASCII-Alphabet beginnen und auf eine Mischung aus ASCII-Alphabetisch, Ziffern und den drei Interpunktionszeichen folgen: ".", "+" und "-". Der Zeichenfolgentyp kann entweder **char _ oder \* *_* WCHAR sein. \*** Das Rich-Edit-Steuerelement erkennt den Typ automatisch.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Nachricht erfolgreich ist, ist der Rückgabewert 0 (null).

Wenn die Nachricht fehlschlägt, ist der Rückgabewert ein Wert ungleich 0 (null). Beispielsweise kann die Meldung aufgrund von unzureichendem Arbeitsspeicher, einer ungültigen Erkennungsoption oder einer ungültigen Schemanamenzeichenfolge fehlschlagen.

Wenn *lParam* mehr als 50 Schemanamen enthält, schlägt die Meldung mit dem Rückgabewert **E \_ INVALIDARG fehl.**

## <a name="remarks"></a>Hinweise

Wenn die automatische URL-Erkennung aktiviert ist (d. h., *wParam* enthält **AURL \_ ENABLEURL),** scannt das Rich Edit-Steuerelement geänderten Text, um zu bestimmen, ob der Text mit dem Format einer URL (oder im Allgemeinen in Windows 8 oder höher einem internationalen IRI-Ressourcenbezeichner) entspricht. Wenn *lParam* NULL ist, erkennt das Steuerelement URLs, die mit den folgenden Schemanamen beginnen:

-   callto
-   file
-   ftp
-   Gopher
-   http
-   https
-   mailto
-   news
-   notes
-   Nntp
-   onenote
-   Outlook
-   Prospero
-   tel
-   telnet
-   wais
-   Webcal

Wenn die automatische Linkerkennung aktiviert ist, entfernt das Rich Edit-Steuerelement den **CFE \_ LINK-Effekt** aus geändertem Text, der nicht über ein vom Steuerelement erkanntes Format verfügt. Wenn Ihre Anwendung den **CFE \_ LINK-Effekt** verwendet, um andere Texttypen zu markieren, aktivieren Sie die automatische Linkerkennung nicht. Das Rich-Edit-Steuerelement überprüft nicht, ob ein erkannter Link vorhanden ist. dass die Verantwortung dem Client gehört.

Ein umfangreiches Bearbeitungssteuerfeld sendet die [EN \_ LINK-Benachrichtigung,](en-link.md) wenn es verschiedene Nachrichten empfängt, während sich der Mauszeiger über Text mit **dem CFE \_ LINK-Effekt** befindet. Weitere Informationen finden Sie unter [Automatische RichEdit Hyperlinks](/archive/blogs/murrays/automatic-richedit-hyperlinks) und [RichEdit Friendly Name Hyperlinks](/archive/blogs/murrays/richedit-friendly-name-hyperlinks).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> <dt>

[EN \_ LINK](en-link.md)
</dt> </dl>

 

