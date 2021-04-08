---
title: EM_AUTOURLDETECT Meldung (RichEdit. h)
description: Aktiviert oder deaktiviert die automatische Erkennung von Hyperlinks von einem Rich-Edit-Steuerelement.
ms.assetid: 6970ff36-ff3f-4413-a471-9389a76c8f38
keywords:
- Windows-Steuerelemente für EM_AUTOURLDETECT Meldung
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
ms.openlocfilehash: 5cc8f76b89e5e8aa529084b5c8c0898200e28ed2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956730"
---
# <a name="em_autourldetect-message"></a>EM \_ autourldetect-Meldung

Aktiviert oder deaktiviert die automatische Erkennung von Hyperlinks von einem Rich-Edit-Steuerelement.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Geben Sie 0 an, um die automatische Link Erkennung zu deaktivieren, oder einen der folgenden Werte, um verschiedene Arten von Erkennung zu aktivieren.



| Wert                                                                                                                                                                                       | Bedeutung                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AURL_DISABLEMIXEDLGC"></span><span id="aurl_disablemixedlgc"></span><dl> <dt>**aurl \_ disablemixedlgc**</dt> </dl>          | **Windows 8**: Deaktivieren Sie die Erkennung von Domänen Namen, die Bezeichnungen mit Zeichen enthalten, die zu mehr als einem der folgenden Skripts gehören: Lateinisch, Griechisch und Kyrillisch. <br/> |
| <span id="AURL_ENABLEDRIVELETTERS"></span><span id="aurl_enabledriveletters"></span><dl> <dt>**aurl- \_ enabledriveletters**</dt> </dl> | **Windows 8**: Erkennen von Dateinamen mit einer führenden Laufwerk Spezifikation, z. b. "c: \\ Temp".<br/>                                                                           |
| <span id="AURL_ENABLEEA"></span><span id="aurl_enableea"></span><dl> <dt>**aurl- \_ enableea**</dt> </dl>                               | Dieser Wert ist veraltet. Verwenden Sie stattdessen **aurl- \_ enableeaurls** .<br/>                                                                                                            |
| <span id="AURL_ENABLEEAURLS"></span><span id="aurl_enableeaurls"></span><dl> <dt>**aurl- \_ enableeaurls**</dt> </dl>                   | Erkennen von URLs, die ostasiatische Zeichen enthalten. <br/>                                                                                                                      |
| <span id="AURL_ENABLEEMAILADDR"></span><span id="aurl_enableemailaddr"></span><dl> <dt>**aurl \_ enableemailaddr**</dt> </dl>          | **Windows 8**: Erkennen von e-Mail-Adressen.<br/>                                                                                                                                |
| <span id="AURL_ENABLETELNO"></span><span id="aurl_enabletelno"></span><dl> <dt>**aurl- \_ enabletelno**</dt> </dl>                      | **Windows 8**: Erkennen von Telefonnummern.<br/>                                                                                                                              |
| <span id="AURL_ENABLEURL"></span><span id="aurl_enableurl"></span><dl> <dt>**aurl- \_ EnableURL**</dt> </dl>                            | **Windows 8**: erkennen Sie URLs, die den Pfad enthalten.<br/>                                                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter bestimmt die URL-Schemas, die erkannt werden, wenn **aurl- \_ EnableURL** aktiv ist. Wenn *LPARAM* den Wert NULL hat, wird die Liste der Standardschema Namen verwendet (siehe Hinweise). Alternativ kann *LPARAM* auf eine mit NULL endenden Zeichenfolge zeigen, die aus bis zu 50 durch Doppelpunkten beendeten Schema Namen besteht, die die Standardschema Namen Liste ablösen. Die Zeichenfolge könnte z. b. "News: http: FTP: Telnet:" lauten. Die Schema Namen Syntax ist in der Website der Internet Engineering Task Force (IETF)-Website in der [URI (Uniform Resource Identifier): Generisches Syntax]( https://www.ietf.org/rfc/rfc2396.txt) Dokument definiert. Ein Schema Name kann beispielsweise bis zu 13 Zeichen (einschließlich des Doppelpunkts) enthalten, muss mit einem alphabetischen ASCII-Wert beginnen. Anschließend kann eine Mischung aus ASCII-alphabetik, Ziffern und den drei Interpunktions Zeichen folgen: ".", "+" und "-". Der Zeichen folgertyp kann entweder ** \* char* _ oder _*WCHAR \**_ lauten; das Rich Edit-Steuerelement erkennt den Typ automatisch.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Nachricht erfolgreich ist, ist der Rückgabewert 0 (null).

Wenn die Meldung fehlschlägt, ist der Rückgabewert ein Wert ungleich 0 (null). Beispielsweise kann die Nachricht aufgrund von unzureichendem Arbeitsspeicher, einer ungültigen Erkennungs Option oder einer ungültigen Schema namens Zeichenfolge fehlschlagen.

Wenn _lParam * mehr als 50 Schema Namen enthält, schlägt die Nachricht mit dem Rückgabewert **E \_ invalidArg** fehl.

## <a name="remarks"></a>Bemerkungen

Wenn die automatische URL-Erkennung aktiviert ist (d. h., *wParam* enthält **aurl- \_ EnableURL**), scannt das Rich Edit-Steuerelement den geänderten Text, um zu bestimmen, ob der Text mit dem Format einer URL übereinstimmt (oder allgemeiner in Windows 8 oder höher eine IRI International Resource Identifier). Wenn *LPARAM* den Wert NULL hat, erkennt das-Steuerelement URLs, die mit den folgenden Schema Namen beginnen:

-   callto
-   file
-   ftp
-   Gopher
-   http
-   https
-   mailto
-   news
-   notes
-   NNTP-
-   onenote
-   positiv
-   Prospero
-   tel
-   telnet
-   wais
-   webcal

Wenn die automatische Verknüpfungs Erkennung aktiviert ist, entfernt das Rich Edit-Steuerelement den **CFE- \_ Link** Effekt aus dem geänderten Text, der nicht vom Steuerelement erkannt wird. Aktivieren Sie die automatische Link Erkennung nicht, wenn Ihre Anwendung den **CFE- \_ Link** Effekt verwendet, um andere Text Typen zu markieren. Das Rich Edit-Steuerelement prüft nicht, ob ein erkannter Link vorhanden ist. Diese Verantwortung gehört zum Client.

Wenn ein Rich-Edit-Steuerelement den Mauszeiger über Text mit dem **Link "CFE- \_ Link** " empfängt, sendet er eine Benachrichtigung über den [ \_ Link "en](en-link.md) ". Weitere Informationen finden Sie unter [Automatische RichEdit-Hyperlinks](/archive/blogs/murrays/automatic-richedit-hyperlinks) und [RichEdit-Anzeige Name Hyperlinks](/archive/blogs/murrays/richedit-friendly-name-hyperlinks).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> <dt>

[Link "en" \_](en-link.md)
</dt> </dl>

 

