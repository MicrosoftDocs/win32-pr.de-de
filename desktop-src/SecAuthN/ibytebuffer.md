---
description: Die IByteBuffer-Schnittstelle wird zum Lesen, Schreiben und Verwalten von Streamobjekten bereitgestellt. Dieses Objekt ist im Wesentlichen ein Wrapper für das IStream-Objekt.
ms.assetid: dbc46d53-a421-45c0-a86b-b8a0a212a672
title: IByteBuffer-Schnittstelle (Scardssp.h)
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
ms.openlocfilehash: 8f0aa81106629142efeec7e22bdb495bea853c3c689d6b55887a62f896d89d62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119417410"
---
# <a name="ibytebuffer-interface"></a>IByteBuffer-Schnittstelle

\[Die **IByteBuffer-Schnittstelle** ist für die Verwendung in den Im Abschnitt Anforderungen angegebenen Betriebssystemen verfügbar. Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die [**IStream-Schnittstelle**](/windows/desktop/api/objidl/nn-objidl-istream) bietet ähnliche Funktionen.\]

Die **IByteBuffer-Schnittstelle** wird zum Lesen, Schreiben und Verwalten von Streamobjekten bereitgestellt. Dieses Objekt ist im Wesentlichen ein Wrapper für das **IStream-Objekt.**

## <a name="members"></a>Member

Die **IByteBuffer-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IByteBuffer** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IByteBuffer-Schnittstelle** verfügt über diese Methoden.



| Methode                                           | Beschreibung                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**Klon**](ibytebuffer-clone.md)               | Klont ein **IByteBuffer-Objekt.**<br/>                                                              |
| [**Commit**](ibytebuffer-commit.md)             | Commits für eine [*Transaktion.*](/windows/desktop/SecGloss/t-gly)<br/> |
| [**CopyTo**](ibytebuffer-copyto.md)             | Kopiert Bytes in ein anderes Objekt.<br/>                                                                |
| [**Initialisieren**](ibytebuffer-initialize.md)     | Initialisiert das **IByteBuffer-Objekt.**<br/>                                                        |
| [**LockRegion**](ibytebuffer-lockregion.md)     | Schränkt den Zugriff auf einen Bytebereich ein.<br/>                                                          |
| [**Überwachungsdaten**](ibytebuffer-read.md)                 | Liest Bytes in den Arbeitsspeicher.<br/>                                                                       |
| [**Zurücksetzen**](ibytebuffer-revert.md)             | Verwirft Änderungen seit dem letzten [**Commitaufruf.**](ibytebuffer-commit.md)<br/>                     |
| [**Seek**](ibytebuffer-seek.md)                 | Ändert den Suchzeiger.<br/>                                                                      |
| [**Setsize**](ibytebuffer-setsize.md)           | Ändert die Größe des Streamobjekts.<br/>                                                         |
| [**Stat**](ibytebuffer-stat.md)                 | Ruft statistische Informationen zu einem Stream ab.<br/>                                              |
| [**UnlockRegion**](ibytebuffer-unlockregion.md) | Entfernt die zugriffseinschränkung, die zuvor von [**LockRegion festgelegt wurde.**](ibytebuffer-lockregion.md)<br/>     |
| [**Schreiben**](ibytebuffer-write.md)               | Schreibt Bytes in den Stream.<br/>                                                                    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Scardssp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ IByteBuffer ist als E126F8FE-A7AF-11D0-B88A-00C04FD424B9 definiert.<br/>          |



 

