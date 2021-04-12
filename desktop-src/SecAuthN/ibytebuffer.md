---
description: Die ibytebuffer-Schnittstelle wird zum Lesen, schreiben und Verwalten von Streamobjekten bereitgestellt. Bei diesem Objekt handelt es sich im Wesentlichen um einen Wrapper für das IStream-Objekt.
ms.assetid: dbc46d53-a421-45c0-a86b-b8a0a212a672
title: Ibytebuffer-Schnittstelle (scardssp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: dfba15dee78134a9787bf7af994f1d4e2b064339
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960542"
---
# <a name="ibytebuffer-interface"></a>Ibytebuffer-Schnittstelle

\[Die **ibytebuffer** -Schnittstelle ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) -Schnittstelle bietet eine ähnliche Funktionalität.\]

Die **ibytebuffer** -Schnittstelle wird zum Lesen, schreiben und Verwalten von Streamobjekten bereitgestellt. Bei diesem Objekt handelt es sich im Wesentlichen um einen Wrapper für das **IStream** -Objekt.

## <a name="members"></a>Member

Die **ibytebuffer** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Ibytebuffer** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ibytebuffer** -Schnittstelle verfügt über diese Methoden.



| Methode                                           | BESCHREIBUNG                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**Klon**](ibytebuffer-clone.md)               | Klont ein **ibytebuffer** -Objekt.<br/>                                                              |
| [**Einzusetzen**](ibytebuffer-commit.md)             | Führt einen Commit einer [*Transaktion*](/windows/desktop/SecGloss/t-gly)aus.<br/> |
| [**CopyTo**](ibytebuffer-copyto.md)             | Kopiert Bytes in ein anderes Objekt.<br/>                                                                |
| [**Initialisieren**](ibytebuffer-initialize.md)     | Initialisiert das **ibytebuffer** -Objekt.<br/>                                                        |
| [**Lock Region**](ibytebuffer-lockregion.md)     | Schränkt den Zugriff auf einen Bereich von Bytes ein.<br/>                                                          |
| [**Lesen**](ibytebuffer-read.md)                 | Liest Bytes in den Arbeitsspeicher.<br/>                                                                       |
| [**Umzukehren**](ibytebuffer-revert.md)             | Verwirft Änderungen seit dem letzten [**Commit**](ibytebuffer-commit.md) -Befehl.<br/>                     |
| [**Seek**](ibytebuffer-seek.md)                 | Ändert den Such Zeiger.<br/>                                                                      |
| [**SetSize**](ibytebuffer-setsize.md)           | Ändert die Größe des Streamobjekts.<br/>                                                         |
| [**Stat**](ibytebuffer-stat.md)                 | Ruft statistische Informationen zu einem Stream ab.<br/>                                              |
| [**UnlockRegion**](ibytebuffer-unlockregion.md) | Entfernt die Zugriffs Einschränkung, die zuvor von [**LockRegion**](ibytebuffer-lockregion.md)festgelegt wurde.<br/>     |
| [**Schreiben**](ibytebuffer-write.md)               | Schreibt Bytes in den Stream.<br/>                                                                    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>"Scardssp. h"</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scardssp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ibytebuffer ist als E126F8FE-A7AF-11D0-B88A-00C04FD424B9 definiert.<br/>          |



 

