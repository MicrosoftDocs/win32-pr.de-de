---
title: ACM_OPEN Meldung (Commctrl.h)
description: Öffnet einen AVI-Clip und zeigt seinen ersten Frame in einem Animationssteuerelement an. Sie können diese Nachricht explizit senden oder das Makro "Animieren \_ öffnen" oder \_ "Animieren von OpenEx" verwenden. Es wird empfohlen, die Unicode-Version dieser Nachricht, ACM \_ OPENW, zu verwenden.
ms.assetid: 87f476ce-bb27-4b5f-bfdf-dff84bd7e4f4
keywords:
- ACM_OPEN Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 4c5af2bd996af159217c92d78102a97e5c530d34cf445d5ad34186cecb93ab85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922170"
---
# <a name="acm_open-message"></a>ACM \_ OPEN-Nachricht

Öffnet einen AVI-Clip und zeigt seinen ersten Frame in einem Animationssteuerelement an. Sie können diese Nachricht explizit senden oder das [**Makro \_ "Animieren öffnen"**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) oder [**\_ "Animieren von OpenEx"**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex) verwenden. Es wird empfohlen, die Unicode-Version dieser Nachricht, ACM \_ OPENW, zu verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

[Version 4.71](common-control-versions.md) und höher. Ein Instanzhandle für das Modul, aus dem die Ressource geladen werden soll. Legen Sie diesen Wert auf **NULL** fest, damit das Steuerelement den HINSTANCE-Wert verwendet, der zum Erstellen des Fensters verwendet wird. Beachten Sie Folgendes: Wenn das Fenster von einer DLL erstellt wird, ist der Standardwert für *wParam* der HINSTANCE-Wert der DLL und nicht der Anwendung, die die DLL aufruft.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf einen Puffer, der den Pfad der AVI-Datei oder den Namen einer AVI-Ressource enthält. Alternativ kann dieser Parameter aus dem AVI-Ressourcenbezeichner in [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) und 0 (null) im [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))bestehen. Um diesen Wert zu erstellen, verwenden Sie das [**MAKEINTRESOURCE-Makro.**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) Das Steuerelement lädt die AVI-Ressource aus dem Modul, das durch das Instanzhandle angegeben wird, das an die [**CreateWindow-Funktion,**](/windows/desktop/api/winuser/nf-winuser-createwindowa) das [**Makro Animieren \_ der Erstellung**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) oder die Funktion zum Erstellen des Dialogfelds übergeben wurde, die das Steuerelement erstellt hat. In [Version 4.71](common-control-versions.md) und höher wird die Ressource aus dem von *wParam* angegebenen Modul geladen. Eine AVI-Ressource muss den Typ "AVI" aufweisen. Wenn dieser Parameter **NULL** ist, schließt das System ggf. die AVI-Datei, die zuvor für das angegebene Animationssteuerelement geöffnet wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück. Andernfalls wird 0 (null) zurückgegeben.

## <a name="remarks"></a>Hinweise

Die von *lpszName* angegebene AVI-Datei oder -Ressource darf keine Audiodaten enthalten.

Es wird empfohlen, die Unicode-Version dieser Nachricht, ACM \_ OPENW, zu verwenden.

Sie können nur automatische AVI-Clips öffnen. ACM \_ OPEN und Animate [**\_ Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) schlagen fehl, wenn *lParam* einen AVI-Clip angibt, der Sound enthält.

Sie können [**Animate \_ Close**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close) verwenden, um eine AVI-Datei oder EINE AVI-Ressource zu schließen, die zuvor für das angegebene Animationssteuerelement geöffnet wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **ACM \_ OPENW** (Unicode) und **ACM \_ OPENA** (ANSI)<br/>                         |



 

