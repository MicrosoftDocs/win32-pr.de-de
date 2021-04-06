---
title: EM_GETTEXTLENGTHEX Meldung (RichEdit. h)
description: Berechnet die Textlänge auf verschiedene Weise. Sie wird in der Regel vor dem Erstellen eines Puffers aufgerufen, um den Text aus dem Steuerelement zu empfangen.
ms.assetid: 42c89b7b-e48d-4517-9993-ce58ff9e4e40
keywords:
- Windows-Steuerelemente für EM_GETTEXTLENGTHEX Meldung
topic_type:
- apiref
api_name:
- EM_GETTEXTLENGTHEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de2d91674e07ef60c2ce95535983a31cf380f9e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858848"
---
# <a name="em_gettextlengthex-message"></a>EM \_ gettextverlänex-Meldung

Berechnet die Textlänge auf verschiedene Weise. Sie wird in der Regel vor dem Erstellen eines Puffers aufgerufen, um den Text aus dem Steuerelement zu empfangen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Zeiger auf eine [**gettextverlänex**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) -Struktur, die die Textlängen Informationen empfängt.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. Er muss NULL sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Meldung gibt die Anzahl von **TCHAR** s im Bearbeitungs Steuerelement zurück, abhängig von der Einstellung der Flags in der [**gettextverlänex**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) -Struktur. Wenn inkompatible Flags im **Flags** -Member festgelegt wurden, gibt die Nachricht E \_ invalidArg zurück.

## <a name="remarks"></a>Bemerkungen

Diese Meldung ist eine schnelle und einfache Möglichkeit, die Anzahl der Zeichen in der Unicode-Version des Rich Edit-Steuer Elements zu bestimmen. Für eine nicht-Unicode-Ziel Codepage können Sie jedoch möglicherweise in eine Kombination aus Einzel Byte-und Doppelbyte Zeichen wandeln.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Gettextverlänex**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex)
</dt> </dl>

 

 





