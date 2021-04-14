---
title: ACM_OPEN Meldung (kommstrg. h)
description: Öffnet einen AVI-Clip und zeigt seinen ersten Frame in einem Animations Steuerelement an. Sie können diese Nachricht explizit senden oder das Makro animieren \_ Open oder animieren \_ OpenEx verwenden. Wir empfehlen die Verwendung der Unicode-Version dieser Nachricht, ACM \_ openw.
ms.assetid: 87f476ce-bb27-4b5f-bfdf-dff84bd7e4f4
keywords:
- Windows-Steuerelemente für ACM_OPEN Meldung
topic_type:
- apiref
api_name:
- ACM_OPEN
- ACM_OPENA
- ACM_OPENW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0588c0e321efe5cace63baf4016dbaa97f735252
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391648"
---
# <a name="acm_open-message"></a>Geöffnete ACM- \_ Nachricht

Öffnet einen AVI-Clip und zeigt seinen ersten Frame in einem Animations Steuerelement an. Sie können diese Nachricht explizit senden oder das Makro [**animieren \_ Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) oder [**animieren \_ OpenEx**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex) verwenden. Wir empfehlen die Verwendung der Unicode-Version dieser Nachricht, ACM \_ openw.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

[Version 4,71](common-control-versions.md) und höher. Ein Instanzhandle für das Modul, von dem die Ressource geladen werden soll. Legen Sie diesen Wert auf **null** fest, damit das Steuerelement den HINSTANCE-Wert verwendet, der zum Erstellen des Fensters verwendet wird. Beachten Sie Folgendes: Wenn das Fenster durch eine DLL erstellt wird, ist der Standardwert für *wParam* der HINSTANCE-Wert der dll, nicht die Anwendung, die die DLL aufruft.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf einen Puffer, der den Pfad der AVI-Datei oder den Namen einer AVI-Ressource enthält. Alternativ kann dieser Parameter aus dem AVI-Ressourcen Bezeichner in [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) und NULL im [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))bestehen. Verwenden Sie das [**makeintresource**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) -Makro, um diesen Wert zu erstellen. Das-Steuerelement lädt die AVI-Ressource aus dem Modul, das vom Instanzhandle angegeben wurde [**, das an die Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowa) "-Funktion", " [**animieren \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) " oder die Dialogfeld-Erstellungs Funktion, die das Steuerelement erstellt hat, In [Version 4,71](common-control-versions.md) und höher wird die Ressource aus dem Modul geladen, das von *wParam* angegeben wird. Eine AVI-Ressource muss den Typ "AVI" aufweisen. Wenn dieser Parameter **null** ist, schließt das System die AVI-Datei, die zuvor für das angegebene Animations Steuerelement geöffnet war, sofern vorhanden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.

## <a name="remarks"></a>Bemerkungen

Die von *lpszname* angegebene AVI-Datei oder-Ressource darf kein Audioformat enthalten.

Wir empfehlen die Verwendung der Unicode-Version dieser Nachricht, ACM \_ openw.

Sie können nur automatische AVI-Clips öffnen. \_Das Öffnen und [**Animieren von \_**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) ACM schlägt fehl, wenn *LPARAM* einen AVI-Clip angibt, der Sound enthält.

Sie können Animation [**\_ Close**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close) verwenden, um eine AVI-Datei oder eine AVI-Ressource zu schließen, die zuvor für das angegebene Animations Steuerelement geöffnet wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **ACM \_ Openw** (Unicode) und **ACM \_ Opena** (ANSI)<br/>                         |



 

