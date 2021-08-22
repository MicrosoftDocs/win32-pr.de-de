---
title: IOrpcDebugNotify-Schnittstelle
description: Stellt Remotedebuggingfunktionen zur Verfügung.
ms.assetid: f91987c0-2e4b-4872-8ed6-e208a23baa49
keywords:
- IOrpcDebugNotify-Schnittstelle COM
- IOrpcDebugNotify-Schnittstelle COM , beschrieben
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
ms.openlocfilehash: e3dd051819b70ae93b7c615d803e12134221d55ffbd464c60d5b9c41d983eb9f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678580"
---
# <a name="iorpcdebugnotify-interface"></a>IOrpcDebugNotify-Schnittstelle

Stellt Remotedebuggingfunktionen zur Verfügung.

## <a name="when-to-implement"></a>Gründe für die Implementierung

Implementieren Sie diese Schnittstelle, um das Remotedebuggen über RPC zu ermöglichen.

## <a name="when-to-use"></a>Verwendung

Diese Schnittstelle sollte für das Prozess-Remotedebuggen verwendet werden, wenn Softwareausnahmen nicht für die Benachrichtigungen des COM-Debuggers verwendet werden sollen. Mithilfe dieser Methoden können Prozessin-Process-Debugger durch direkte Aufrufe benachrichtigt werden.

## <a name="members"></a>Member

Die **IOrpcDebugNotify-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) **IOrpcDebugNotify** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IOrpcDebugNotify-Schnittstelle** verfügt über diese Methoden.



| Methode                                                              | BESCHREIBUNG                                                                    |
|:--------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md)       | Sendet Daten vom Clientdebugger an den Serverdebugger.<br/>         |
| [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md) | Ruft die RPC-Puffergröße aus dem clientseitigen Debugger ab.<br/>        |
| [**ClientNotify**](iorpcdebugnotify-clientnotify.md)               | Informiert den Client über eine ausgehende Debuggeranforderung an den Server.<br/>   |
| [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)       | Sendet Daten vom Serverdebugger an den Clientdebugger.<br/>         |
| [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md) | Ruft die RPC-Puffergröße aus dem serverseitigen Debugger ab.<br/>        |
| [**ServerNotify**](iorpcdebugnotify-servernotify.md)               | Informiert den Server über eine eingehende Debuggeranforderung vom Client.<br/> |



 

## <a name="remarks"></a>Hinweise

Eine Importbibliothek, die die **IOrpcDebugNotify-Schnittstelle** enthält, ist nicht im Microsoft Windows Software Development Kit (SDK) enthalten. Eine Anwendung kann die [**Funktionen GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) und [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) verwenden, um einen Funktionszeiger auf [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) aus oleaut.dll abzurufen und diese Methoden über die **IOrpcDebugNotify-Schnittstelle** zur Verfügung zu stellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>N/V</dt> </dl> |
| Idl<br/>                      | <dl> <dt>N/V</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)
</dt> <dt>

[**ORPC \_ DBG \_ ALL**](orpc-dbg-all.md)
</dt> <dt>

[**\_ORPC-DBG-PUFFER \_**](orpc-dbg-buffer.md)
</dt> <dt>

[**ORPC \_ INIT \_ ARGS**](orpc-init-args.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> </dl>

 

