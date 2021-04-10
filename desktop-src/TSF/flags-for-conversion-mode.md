---
title: Flags für den Konvertierungsmodus (ctffunc. h)
description: Die folgenden Flags werden als Wert von "GUID Depot \_ - \_ Tastatur \_ Eingabe im InputMode" verwendet \_ . Dies entspricht den IME- \_ cmode-Werten für imm32.
ms.assetid: 6e545af5-5fdb-49de-b24e-aaee82b51326
keywords:
- Flags für den Konvertierungsmodus-Text Dienst-Framework
topic_type:
- apiref
api_name:
- Flags for Conversion Mode
api_location:
- Ctffunc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 022712ff45f213992bf3d40bd0149959e4864faa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104121"
---
# <a name="flags-for-conversion-mode"></a>Flags für den Konvertierungsmodus

Die folgenden Flags werden als Wert von " [GUID Depot \_ - \_ Tastatur \_ Eingabe im InputMode \_ ](predefined-compartments.md)" verwendet. Dies entspricht den [IME- \_ cmode](../intl/ime-conversion-mode-values.md) -Werten für imm32.



| Flag                             | Wert  | BESCHREIBUNG                                                     |
|----------------------------------|--------|-----------------------------------------------------------------|
| TF in der \_ alphanumerischen Version des TF-Modus \_ | 0x0000 | Auf 1 festgelegt, wenn alphanumerischer Modus.                                  |
| TF- \_ Konfigurations Modus ( \_ nativ)       | 0x0001 | Auf 1 festgelegt, wenn der einheitliche Modus ist; 0 (null), wenn der alphanumerische Modus ist.                |
| TF- \_ systemversionmoduskatakana \_     | 0x0002 | Auf 1 festgelegt, wenn Katakana-Modus; 0, wenn der Hiragana-Modus ist.                  |
| TF-Konstante für den Verbindungs \_ Modus \_    | 0x0008 | Auf 1 festgelegt, wenn vollständiger Shape-Modus; 0 (null), wenn Halbform Modus.              |
| TF-Verbindungs \_ Modus \_        | 0x0010 | Auf 1 festgelegt, um die Verarbeitung von Konvertierungen durch IME zu verhindern. 0, wenn nicht. |
| TF- \_ konforme \_ CharCode     | 0x0020 | Auf 1 festgelegt, wenn Zeichencode Eingabemodus; 0, wenn nicht.                |
| TF-Verbindungs \_ Modus-Bildschirm \_ Tastatur | 0x0080 | Auf 1 festgelegt, wenn weicher Tastaturmodus 0, wenn nicht.                       |
| TF- \_ Konversions Modus- \_ noconversion | 0x0100 | Auf 1 festgelegt, um die Verarbeitung von Konvertierungen durch IME zu verhindern. 0, wenn nicht. |
| TF-Symbol für " \_ deversionmode" \_       | 0x0400 | Auf 1 festgelegt, wenn der Modus für die Symbol Konvertierung 0, wenn nicht.                   |
| TF-Verbindungs \_ Modus \_ korrigiert        | 0x0800 | Auf 1 festgelegt, wenn fester Konvertierungsmodus; 0, wenn nicht.                    |



 

Die folgenden Werte werden als Wert von " [GUID Depot \_ \_ Tastatur \_ InputMode- \_ Satz](predefined-compartments.md)" verwendet. Dies entspricht den [IME- \_ smode](../intl/ime-composition-string-values.md) -Werten für imm32.



| Flag                            | Wert  | BESCHREIBUNG                                                                |
|---------------------------------|--------|----------------------------------------------------------------------------|
| TF \_ sentencemode \_ None          | 0x0000 | Keine Informationen für einen Satz.                                               |
| TF \_ sentencemode- \_ plauralklausel | 0x0001 | Der IME verwendet die Plural-klauselinformationen, um die Konvertierungs Verarbeitung auszuführen. |
| TF \_ sentencemode \_ singleconvert | 0x0002 | Der IME führt die Konvertierungs Verarbeitung im Einzelzeichen Modus aus.        |
| TF \_ sentencemode \_ automatisch     | 0x0004 | Der IME führt die Konvertierungs Verarbeitung im automatischen Modus aus.               |
| TF \_ sentencemode \_ phraervorhersage | 0x0008 | Der IME verwendet Ausdrucks Informationen, um das nächste Zeichen vorherzusagen.             |
| TF \_ sentencemode- \_ Konversation  | 0x0010 | Der IME verwendet den Konversationsmodus. Dies ist nützlich für Chat Anwendungen.      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Verteilbare Komponente<br/>          | TSF 1,0 onwindows NT 4.0, Windows 2000 professionalandwindows meWindows 98<br/>   |
| Header<br/>                   | <dl> <dt>Ctffunc. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Ctffunc. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Vordefinierte Depots](predefined-compartments.md)
</dt> </dl>

 

