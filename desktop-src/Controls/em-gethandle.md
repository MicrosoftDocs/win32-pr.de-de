---
title: EM_GETHANDLE Meldung (Winuser. h)
description: Ruft ein Handle des Speichers ab, der dem Text eines mehrzeiligen Bearbeitungs Steuer Elements zugeordnet ist.
ms.assetid: 74271812-9715-4a46-96b3-0788134f8143
keywords:
- Windows-Steuerelemente für EM_GETHANDLE Meldung
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
ms.openlocfilehash: 88a466394b48d2d726621e50a7e2c5df2f747f08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518299"
---
# <a name="em_gethandle-message"></a>\_GetHandle-Nachricht

Ruft ein Handle des Speichers ab, der dem Text eines mehrzeiligen Bearbeitungs Steuer Elements zugeordnet ist.

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

Der Rückgabewert ist ein Speicher handle, das den Puffer identifiziert, der den Inhalt des Bearbeitungs Steuer Elements enthält. Wenn ein Fehler auftritt, z. b. das Senden der Nachricht an ein einzeilige Bearbeitungs Steuerelement, ist der Rückgabewert 0 (null).

## <a name="remarks"></a>Bemerkungen

Wenn die Funktion erfolgreich ausgeführt wird, kann die Anwendung auf den Inhalt des Bearbeitungs Steuer Elements zugreifen, indem Sie den Rückgabewert in [**hlocal**](/windows/desktop/WinProg/windows-data-types) umwandeln und an [**loczuweisung**](/windows/desktop/api/winbase/nf-winbase-locallock)übergibt. **Loczuweisung** gibt einen Zeiger auf einen Puffer zurück, der ein mit Null endendes Array von **char** s oder **WCHAR** s ist, je nachdem, ob eine ANSI-oder Unicode-Funktion das Steuerelement erstellt hat. Wenn z. b. " [**featewindowexa**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " verwendet wurde, ist der Puffer ein Array von " **char** s", aber wenn " **featewindowexw** " verwendet wurde, ist der Puffer ein Array von **WCHAR** s. Der Inhalt des Puffers wird möglicherweise nicht von der Anwendung geändert. Um den Puffer zu entsperren, ruft die Anwendung [**localunlock**](/windows/desktop/api/winbase/nf-winbase-localunlock) auf, bevor das Bearbeitungs Steuerelement neue Nachrichten empfangen kann.

> [!Note]  
> Für Comctl32.dll Version 6 enthält der Puffer immer ein Array von **WCHAR** s, unabhängig davon, ob eine ANSI-oder Unicode-Funktion das Bearbeitungs Steuerelement erstellt hat. Weitere Informationen zu DLL-Versionen finden Sie unter [allgemeine Steuerelement Versionen](common-control-versions.md).

 

Wenn Ihre Anwendung die von **EM \_ GetHandle** vorgegebenen Einschränkungen nicht einhalten kann, verwenden Sie die Funktionen [**getwindowtextlength**](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha) und [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) , um den Inhalt des Bearbeitungs Steuer Elements in einen von der Anwendung bereitgestellten Puffer zu kopieren.

Umfassende **Bearbeitung:** Die **\_ GetHandle** -Nachricht wird nicht unterstützt. Rich Edit-Steuerelemente speichern Text nicht als einfaches Zeichen Array.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**EM- \_ andle**](em-sethandle.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[**Getwindowtextlength**](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[**Loczuweisung**](/windows/desktop/api/winbase/nf-winbase-locallock)
</dt> <dt>

[**Localunlock**](/windows/desktop/api/winbase/nf-winbase-localunlock)
</dt> </dl>

 

