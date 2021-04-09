---
description: Zeigt ein Dialogfeld an, in dem die Signatur Geber Informationen für eine signierte Nachricht enthalten sind.
ms.assetid: e4552cbb-90f4-46f4-a271-3a91ccd5f806
title: CryptUIDlgViewSignerInfo-Funktion
ms.topic: reference
ms.date: 05/29/2020
ms.openlocfilehash: 7ae677692b9266893eabf1002039c5efbf0ca5c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862311"
---
# <a name="cryptuidlgviewsignerinfo-function"></a>CryptUIDlgViewSignerInfo-Funktion

\[Die **cryptuidlgviewsignerinfo** -Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. \]

Die Funktion **cryptuidlgviewsignerinfo** zeigt ein Dialogfeld an, in dem die Signatur Geber Informationen für eine signierte Nachricht enthalten sind.

> [!Note]  
> Diese Funktion ist nicht in einer veröffentlichten Header Datei deklariert. Um diese Struktur zu verwenden, deklarieren Sie Sie im exakten Format.

## <a name="syntax"></a>Syntax


```C++
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcvsi* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**cryptui \_ viewsignerinfo \_**](cryptui-viewsignerinfo-struct.md) -Struktur Struktur, die die anzuzeigenden Signatur Geber Informationen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt bei Erfolg einen Wert ungleich 0 (null) und NULL bei einem Fehler zurück. Für erweiterte Fehlerinformationen aufrufen Sie die [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion.

Mögliche Fehlercodes von [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) sind u. a. die folgenden.



| Rückgabecode                                                                                   | Beschreibung                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Mindestens ein Argument ist ungültig.<br/>  |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Es ist ein Fehler bei der Speicher Belegung aufgetreten.<br/> |

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                        |
| Ende des Supports<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                       |
| Bibliothek<br/>                  | <dl> <dt>Cryptui. lib</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>Cryptui.dll</dt> </dl>      |
| Unicode- und ANSI-Name<br/>   | **Cryptuidlgviewsignerinfow** (Unicode) und **cryptuidlgviewsignerinfoa** (ANSI)<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**cryptui \_ viewsignerinfo- \_ Struktur**](cryptui-viewsignerinfo-struct.md)
</dt> </dl>
