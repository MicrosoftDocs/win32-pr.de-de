---
title: EM_GETHANDLE (Winuser.h)
description: Ruft ein Handle des Arbeitsspeichers ab, der derzeit für den Text eines mehrzeilenigen Bearbeitungssteuerfelds zugeordnet ist.
ms.assetid: 74271812-9715-4a46-96b3-0788134f8143
keywords:
- EM_GETHANDLE meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- EM_GETHANDLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f09ade5545197df2dbc9310b708cd7521334bba68f41a14329dd865e84fdee6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019648"
---
# <a name="em_gethandle-message"></a>EM \_ GETHANDLE-Nachricht

Ruft ein Handle des Arbeitsspeichers ab, der derzeit für den Text eines mehrzeilenigen Bearbeitungssteuerfelds zugeordnet ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein Speicherhand handle, das den Puffer identifiziert, der den Inhalt des Bearbeitungssteuersteuerpunkts enthält. Wenn ein Fehler auftritt, z. B. das Senden der Nachricht an ein einzeilenbasiertes Bearbeitungssteuer steuerelement, ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Hinweise

Wenn die Funktion erfolgreich ist, kann die Anwendung auf den Inhalt des Edit-Steuerelements zugreifen, indem sie den Rückgabewert in [**HLOCAL**](/windows/desktop/WinProg/windows-data-types) umleitet und an [**LocalLock übergibst.**](/windows/desktop/api/winbase/nf-winbase-locallock) **LocalLock** gibt einen Zeiger auf einen Puffer zurück, bei dem es sich um ein auf NULL beendetes Array von **CHAR** s oder **WCHAR** s handelt, je nachdem, ob das Steuerelement von einer ANSI- oder Unicode-Funktion erstellt wurde. Wenn beispielsweise [**CreateWindowExA**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) verwendet wurde, ist der Puffer ein Array von **CHAR-s,** aber wenn **CreateWindowExW** verwendet wurde, ist der Puffer ein Array von **WCHAR-s.** Die Anwendung ändert möglicherweise nicht den Inhalt des Puffers. Um den Puffer zu entsperren, ruft die Anwendung [**LocalUnlock**](/windows/desktop/api/winbase/nf-winbase-localunlock) auf, bevor dem Bearbeitungssteuerpunkt das Empfangen neuer Nachrichten erlaubt wird.

> [!Note]  
> Bei Comctl32.dll Version 6 enthält der Puffer immer ein Array von **WCHAR-s,** unabhängig davon, ob das Bearbeitungssteuerfeld von einer ANSI- oder Unicode-Funktion erstellt wurde. Weitere Informationen zu DLL-Versionen finden Sie unter [Allgemeine Steuerelementversionen.](common-control-versions.md)

 

Wenn Ihre Anwendung die von EM **\_ GETHANDLE** festgelegten Einschränkungen nicht ein halten kann, verwenden Sie die [**Funktionen GetWindowTextLength**](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha) und [**GetWindowText,**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) um den Inhalt des Bearbeitungssteuer steuerelements in einen von der Anwendung bereitgestellten Puffer zu kopieren.

**Umfangreiche Bearbeitung:** Die **EM \_ GETHANDLE-Nachricht** wird nicht unterstützt. Rich-Edit-Steuerelemente speichern Text nicht als einfaches Array von Zeichen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**EM \_ SETHANDLE**](em-sethandle.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[**GetWindowTextLength**](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[**LocalLock**](/windows/desktop/api/winbase/nf-winbase-locallock)
</dt> <dt>

[**LocalUnlock**](/windows/desktop/api/winbase/nf-winbase-localunlock)
</dt> </dl>

 

