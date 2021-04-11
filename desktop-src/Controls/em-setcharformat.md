---
title: EM_SETCHARFORMAT Meldung (RichEdit. h)
description: Legt die Zeichen Formatierung in einem Rich-Edit-Steuerelement fest.
ms.assetid: 5e7a545d-4ca4-4dc6-badb-584c11194982
keywords:
- Windows-Steuerelemente für EM_SETCHARFORMAT Meldung
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
ms.openlocfilehash: ba8f37960659f29dd33d5b8f27f0b5a2e3d35eb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105585"
---
# <a name="em_setcharformat-message"></a>EM \_ setcharformat-Meldung

Legt die Zeichen Formatierung in einem Rich-Edit-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Zeichen Formatierung, die auf das-Steuerelement angewendet wird. Wenn dieser Parameter 0 (null) ist, wird das Standard Zeichenformat festgelegt. Andernfalls kann es sich um einen der folgenden Werte handeln:



| Wert                                                                                                                                                                           | Bedeutung                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SCF_ALL"></span><span id="scf_all"></span><dl> <dt>**SCF \_ alle**</dt> </dl>                                     | Wendet die Formatierung auf den gesamten Text im-Steuerelement an. Ungültig bei der **SCF- \_ Auswahl** oder dem **SCF- \_ Wort**.<br/>                                                                                                                                                                                         |
| <span id="SCF_ASSOCIATEFONT"></span><span id="scf_associatefont"></span><dl> <dt>**SCF- \_ associatefont**</dt> </dl>       | **RichEdit 4,1:** Ordnet einem angegebenen Skript eine Schriftart zu und ändert somit die Standard Schriftart für dieses Skript. Um die Schriftart anzugeben, verwenden Sie die folgenden Member von [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a): **yHeight**, **bcharset**, **bpitchandfamily**, **szfakename** und **LCID**.<br/>                     |
| <span id="SCF_ASSOCIATEFONT2"></span><span id="scf_associatefont2"></span><dl> <dt>**SCF \_ ASSOCIATEFONT2**</dt> </dl>    | **RichEdit 4,1:** Ordnet einem angegebenen Skript eine Ersatz Zeichen Schriftart (Plane-2) zu, sodass die Standard Schriftart für dieses Skript geändert wird. Um die Schriftart anzugeben, verwenden Sie die folgenden Member von [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a): **yHeight**, **bcharset**, **bpitchandfamily**, **szfakename** und **LCID**.<br/> |
| <span id="SCF_CHARREPFROMLCID"></span><span id="scf_charrepfromlcid"></span><dl> <dt>**SCF \_ charrepfromlcid**</dt> </dl> | Ruft das Zeichen Repertoire aus der LCID ab.<br/>                                                                                                                                                                                                                                                   |
| <span id="SCF_DEFAULT"></span><span id="scf_default"></span><dl> <dt>**SCF- \_ Standard**</dt> </dl>                         | **RichEdit 4,1:** Legt die Standard Schriftart für das-Steuerelement fest. <br/>                                                                                                                                                                                                                                      |
| <span id="SPF_DONTSETDEFAULT"></span><span id="spf_dontsetdefault"></span><dl> <dt>**SPF- \_ dontsetdefault**</dt> </dl>    | Verhindert das Festlegen des Standard Absatz Formats, wenn das Rich Edit-Steuerelement leer ist.<br/>                                                                                                                                                                                                             |
| <span id="SCF_NOKBUPDATE"></span><span id="scf_nokbupdate"></span><dl> <dt>**SCF- \_ nokbupdate**</dt> </dl>                | **RichEdit 4,1:** Verhindert, dass der Tastatur Wechsel der Schriftart entspricht. Wenn z. b. eine arabische Schriftart festgelegt ist, ändert die automatische Tastatur Funktion für Bidi-Sprachen die Tastatur in eine arabische Tastatur.<br/>                                                                                 |
| <span id="SCF_SELECTION"></span><span id="scf_selection"></span><dl> <dt>**SCF- \_ Auswahl**</dt> </dl>                   | Wendet die Formatierung auf die aktuelle Auswahl an. Wenn die Auswahl leer ist, wird die Zeichen Formatierung auf die Einfügemarke angewendet, und das neue Zeichenformat ist nur bis zur Änderung der Einfügemarke wirksam.<br/>                                                                      |
| <span id="SPF_SETDEFAULT"></span><span id="spf_setdefault"></span><dl> <dt>**SPF ( \_ SetDefault)**</dt> </dl>                | Legt die standardmäßigen Absatz Formatierungs Attribute fest.<br/>                                                                                                                                                                                                                                              |
| <span id="SCF_SMARTFONT"></span><span id="scf_smartfont"></span><dl> <dt>**SCF- \_ smartfont**</dt> </dl>                   | Wenden Sie die Schriftart nur an, wenn Sie das Skript behandeln kann.<br/>                                                                                                                                                                                                                                                   |
| <span id="SCF_USEUIRULES"></span><span id="scf_useuirules"></span><dl> <dt>**SCF- \_ useuirules**</dt> </dl>                | **RichEdit 4,1:** Wird bei der **SCF- \_ Auswahl** verwendet. Gibt an, dass das Format von einer Symbolleiste oder einem anderen UI-Tool stammt, sodass anstelle der literalen Formatierung UI-Formatierungs Regeln verwendet werden sollen.<br/>                                                                                                               |
| <span id="SCF_WORD"></span><span id="scf_word"></span><dl> <dt>**SCF- \_ Wort**</dt> </dl>                                  | Wendet die Formatierung auf das ausgewählte Wort oder die Wörter an. Wenn die Auswahl leer ist, die Einfügemarke aber in einem Wort liegt, wird die Formatierung auf das Wort angewendet. Der **SCF- \_ Wort** Wert muss in Verbindung mit dem **SCF- \_ Auswahl** Wert verwendet werden.<br/>                                        |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata) -Struktur, die die zu verwendende Zeichen Formatierung angibt. Nur die Formatierungs Attribute, die vom **dwMask** -Member angegeben werden, werden geändert.

Microsoft Rich Edit 2,0 und höher: dieser Parameter kann ein Zeiger auf eine [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) -Struktur sein, die eine Erweiterung der [**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata) -Struktur ist. Vor dem Senden der **EM- \_ setcharformat** -Meldung legen Sie den **CBSIZE** -Member der Struktur auf fest, `sizeof(CHARFORMAT)` oder geben Sie an, `sizeof(CHARFORMAT2)` welche Version der Struktur verwendet wird.

Die Elemente **szfakename** und **bcharset** können überschrieben werden, wenn Sie für Zeichen ungültig sind, z. b. Arial für Kanji-Zeichen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn der Vorgang fehlschlägt, ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Bemerkungen

Wenn diese Nachricht mehrmals mit denselben Parametern gesendet wird, wird die Auswirkung auf den Text ein-und ausgeschaltet. Das bedeutet, dass das Senden der Nachricht einmal den Effekt erzeugt, dass das Senden der Nachricht zweimal den Effekt abbricht usw.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata)
</dt> <dt>

[**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> </dl>

 

 





