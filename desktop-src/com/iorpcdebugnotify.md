---
title: Iorpcdebug bugnotify-Schnittstelle
description: Bietet Remotedebugfunktionen.
ms.assetid: f91987c0-2e4b-4872-8ed6-e208a23baa49
keywords:
- Iorpcdebug-Schnittstelle com
- Iorpcdebug-Schnittstelle com, beschrieben
topic_type:
- apiref
api_name:
- IOrpcDebugNotify
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f4db08daf93997b2a7fa0ed383591cb5d111ac7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519055"
---
# <a name="iorpcdebugnotify-interface"></a>Iorpcdebug bugnotify-Schnittstelle

Bietet Remotedebugfunktionen.

## <a name="when-to-implement"></a>Gründe für die Implementierung

Implementieren Sie diese Schnittstelle, um Remote Debugging über RPC zu aktivieren.

## <a name="when-to-use"></a>Verwendung

Diese Schnittstelle sollte für das Prozess interne Remote Debuggen verwendet werden, wenn für die com-Debugger-Benachrichtigungen keine Software Ausnahmen verwendet werden sollen. Sie ermöglicht es, in-Process-Debuggern durch direkte Aufrufe mithilfe dieser Methoden benachrichtigt zu werden.

## <a name="members"></a>Member

Die Schnittstelle **iorpcdebug bugnotify** erbt von der [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) -Schnittstelle. " **Iorpcdebug bugnotify** " verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iorpcdebugnotify** -Schnittstelle verfügt über diese Methoden.



| Methode                                                              | BESCHREIBUNG                                                                    |
|:--------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**Clientfillbuffer**](iorpcdebugnotify-clientfillbuffer.md)       | Sendet Daten vom Client Debugger an den Server Debugger.<br/>         |
| [**Clientgetbuffersize**](iorpcdebugnotify-clientgetbuffersize.md) | Ruft die RPC-Puffergröße aus dem Client seitigen Debugger ab.<br/>        |
| [**Clientnotify**](iorpcdebugnotify-clientnotify.md)               | Informiert den Client über eine ausgehende Debugger-Anforderung an den Server.<br/>   |
| [**Serverfillbuffer**](iorpcdebugnotify-serverfillbuffer.md)       | Sendet Daten vom Server Debugger an den Client Debugger.<br/>         |
| [**Servergetbuffersize**](iorpcdebugnotify-servergetbuffersize.md) | Ruft die RPC-Puffergröße aus dem serverseitigen Debugger ab.<br/>        |
| [**Servernotify**](iorpcdebugnotify-servernotify.md)               | Informiert den Server über eine eingehende Debugger-Anforderung vom Client.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Eine Import Bibliothek mit der **iorpcdebugnotify** -Schnittstelle ist nicht im Microsoft Windows Software Development Kit (SDK) enthalten. Eine Anwendung kann die Funktionen [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) und [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) verwenden, um aus oleaut.dll einen Funktionszeiger auf [**dlldebugobjectrpchook**](dlldebugobjectrpchook.md) abzurufen und diese Methoden über die **iorpcdebugnotify** -Schnittstelle bereitzustellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>N/V</dt> </dl> |
| IDL<br/>                      | <dl> <dt>N/V</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)
</dt> <dt>

[**ORPC \_ dbg \_ alle**](orpc-dbg-all.md)
</dt> <dt>

[**ORPC \_ dbg- \_ Puffer**](orpc-dbg-buffer.md)
</dt> <dt>

[**ORPC-init-Argumente \_ \_**](orpc-init-args.md)
</dt> <dt>

[**Dlldebugobjectrpchook**](dlldebugobjectrpchook.md)
</dt> </dl>

 

