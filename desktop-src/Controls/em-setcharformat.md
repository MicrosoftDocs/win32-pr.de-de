---
title: EM_SETCHARFORMAT Nachricht (Richedit.h)
description: Legt die Zeichenformatierung in einem Rich-Edit-Steuerelement fest.
ms.assetid: 5e7a545d-4ca4-4dc6-badb-584c11194982
keywords:
- EM_SETCHARFORMAT Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_SETCHARFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 100cfb1d322cde2d411a0298ee86c224899669defc585826b16bf96751bb4639
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118673130"
---
# <a name="em_setcharformat-message"></a>EM \_ SETCHARFORMAT-Meldung

Legt die Zeichenformatierung in einem Rich-Edit-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Zeichenformatierung, die für das Steuerelement gilt. Wenn dieser Parameter 0 (null) ist, wird das Standardzeichenformat festgelegt. Andernfalls kann dies einer der folgenden Werte sein.



| Wert                                                                                                                                                                           | Bedeutung                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SCF_ALL"></span><span id="scf_all"></span><dl> <dt>**SCF \_ ALL**</dt> </dl>                                     | Wendet die Formatierung auf den gesamten Text im -Steuerelement an. Ungültig mit **SCF \_ SELECTION** oder **SCF \_ WORD**.<br/>                                                                                                                                                                                         |
| <span id="SCF_ASSOCIATEFONT"></span><span id="scf_associatefont"></span><dl> <dt>**SCF \_ ASSOCIATEFONT**</dt> </dl>       | **RichEdit 4.1:** Ordnet einem bestimmten Skript eine Schriftart zu, wodurch die Standardschriftart für dieses Skript geändert wird. Um die Schriftart anzugeben, verwenden Sie die folgenden Member von [**CHARFORMAT2:**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) **yHeight**, **bCharSet**, **bPitchAndFamily**, **szFaceName** und **lcid**.<br/>                     |
| <span id="SCF_ASSOCIATEFONT2"></span><span id="scf_associatefont2"></span><dl> <dt>**SCF \_ ASSOCIATEFONT2**</dt> </dl>    | **RichEdit 4.1:** Ordnet einem bestimmten Skript eine Ersatzschriftart (plane-2) zu und ändert so die Standardschriftart für dieses Skript. Um die Schriftart anzugeben, verwenden Sie die folgenden Member von [**CHARFORMAT2:**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) **yHeight**, **bCharSet**, **bPitchAndFamily**, **szFaceName** und **lcid**.<br/> |
| <span id="SCF_CHARREPFROMLCID"></span><span id="scf_charrepfromlcid"></span><dl> <dt>**SCF \_ CHARREPFROMLCID**</dt> </dl> | Ruft das Zeichen aus der LCID ab.<br/>                                                                                                                                                                                                                                                   |
| <span id="SCF_DEFAULT"></span><span id="scf_default"></span><dl> <dt>**SCF \_ DEFAULT**</dt> </dl>                         | **RichEdit 4.1:** Legt die Standardschriftart für das Steuerelement fest. <br/>                                                                                                                                                                                                                                      |
| <span id="SPF_DONTSETDEFAULT"></span><span id="spf_dontsetdefault"></span><dl> <dt>**SPF \_ DONTSETDEFAULT**</dt> </dl>    | Verhindert das Festlegen des Standardmäßigen Absatzformats, wenn das Rich Edit-Steuerelement leer ist.<br/>                                                                                                                                                                                                             |
| <span id="SCF_NOKBUPDATE"></span><span id="scf_nokbupdate"></span><dl> <dt>**SCF \_ NOKBUPDATE**</dt> </dl>                | **RichEdit 4.1:** Verhindert, dass die Tastatur zur Übereinstimmung mit der Schriftart wechselt. Wenn z. B. eine arabische Schriftart festgelegt ist, ändert normalerweise die automatische Tastaturfunktion für Bidi-Sprachen die Tastatur in eine arabische Tastatur.<br/>                                                                                 |
| <span id="SCF_SELECTION"></span><span id="scf_selection"></span><dl> <dt>**\_SCF-AUSWAHL**</dt> </dl>                   | Wendet die Formatierung auf die aktuelle Auswahl an. Wenn die Auswahl leer ist, wird die Zeichenformatierung auf die Einfügemarke angewendet, und das neue Zeichenformat ist nur wirksam, bis sich die Einfügemarke ändert.<br/>                                                                      |
| <span id="SPF_SETDEFAULT"></span><span id="spf_setdefault"></span><dl> <dt>**SPF \_ SETDEFAULT**</dt> </dl>                | Legt die Standardmäßige Absatzformatierungsattribute fest.<br/>                                                                                                                                                                                                                                              |
| <span id="SCF_SMARTFONT"></span><span id="scf_smartfont"></span><dl> <dt>**SCF \_ SMARTFONT**</dt> </dl>                   | Wenden Sie die Schriftart nur an, wenn sie Skripts verarbeiten kann.<br/>                                                                                                                                                                                                                                                   |
| <span id="SCF_USEUIRULES"></span><span id="scf_useuirules"></span><dl> <dt>**SCF \_ USEUIRULES**</dt> </dl>                | **RichEdit 4.1:** Wird mit **SCF \_ SELECTION** verwendet. Gibt an, dass das Format von einer Symbolleiste oder einem anderen Benutzeroberflächentool stammt, sodass Ui-Formatierungsregeln anstelle der Literalformatierung verwendet werden sollten.<br/>                                                                                                               |
| <span id="SCF_WORD"></span><span id="scf_word"></span><dl> <dt>**SCF \_ WORD**</dt> </dl>                                  | Wendet die Formatierung auf das ausgewählte Wort oder die ausgewählten Wörter an. Wenn die Auswahl leer ist, sich die Einfügemarke jedoch innerhalb eines Worts befindet, wird die Formatierung auf das Wort angewendet. Der **SCF \_ WORD-Wert** muss in Verbindung mit dem **SCF \_ SELECTION-Wert** verwendet werden.<br/>                                        |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**CHARFORMAT-Struktur,**](/windows/win32/api/richedit/ns-richedit-charformata) die die zu verwendende Zeichenformatierung angibt. Nur die vom **dwMask-Member** angegebenen Formatierungsattribute werden geändert.

Microsoft Rich Edit 2.0 und höher: Dieser Parameter kann ein Zeiger auf eine [**CHARFORMAT2-Struktur**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) sein, die eine Erweiterung der [**CHARFORMAT-Struktur**](/windows/win32/api/richedit/ns-richedit-charformata) ist. Legen Sie vor dem Senden der **EM \_ SETCHARFORMAT-Nachricht** den **cbSize-Member** der Struktur auf fest, `sizeof(CHARFORMAT)` oder geben Sie `sizeof(CHARFORMAT2)` an, welche Version der Struktur verwendet wird.

Die Elemente **szFaceName** und **bCharSet** können überschrieben werden, wenn sie für Zeichen ungültig sind, z. B. Arial für Kanjizeichen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn der Vorgang fehlschlägt, ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Hinweise

Wenn diese Nachricht mehr als einmal mit den gleichen Parametern gesendet wird, wird die Auswirkung auf den Text umgeschaltet. Das heißt, das Senden der Nachricht erzeugt einmal den Effekt, das zweimalige Senden der Nachricht bricht den Effekt ab usw.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata)
</dt> <dt>

[**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> </dl>

 

 





