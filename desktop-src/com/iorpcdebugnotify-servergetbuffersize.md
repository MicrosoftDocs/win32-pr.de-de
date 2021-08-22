---
title: IOrpcDebugNotify ServerGetBufferSize-Methode
description: Ruft die RPC-Puffergröße vom serverseitigen Debugger ab.
ms.assetid: 1e9ef194-c85b-4f6d-8b89-1f7ee6941189
keywords:
- ServerGetBufferSize-Methode COM
- ServerGetBufferSize-Methode COM, IOrpcDebugNotify-Schnittstelle
- IOrpcDebugNotify-Schnittstelle COM, ServerGetBufferSize-Methode
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ServerGetBufferSize
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 570c7371b1aa19bf5a7b3932a9560103ba0b7f25072ad7cb69d5bd53e82bb90e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500730"
---
# <a name="iorpcdebugnotifyservergetbuffersize-method"></a>IOrpcDebugNotify::ServerGetBufferSize-Methode

Ruft die RPC-Puffergröße vom serverseitigen Debugger ab.

> [!Note]  
> Eine Importbibliothek, die die **ServerGetBufferSize-Funktion** enthält, ist nicht im Microsoft Windows Software Development Kit (SDK) enthalten. Eine Anwendung kann die Funktionen [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) und [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) verwenden, um einen Funktionszeiger auf [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) aus oleaut.dll abzurufen und diese Funktion über die [**IOrpcDebugNotify-Schnittstelle**](iorpcdebugnotify.md) bereitzustellen.

 

## <a name="syntax"></a>Syntax


```C++
void ServerGetBufferSize(
   ORPC_DBG_ALL *lpOrpcDebugAll
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpOrpcDebugAll* 
</dt> <dd>

Ein Zeiger auf eine [**ORPC \_ DBG \_ ALL-Struktur,**](orpc-dbg-all.md) die Benachrichtigungsinformationen enthält, die das COM-RPC-System an den Debugger übergibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>N/V</dt> </dl> |
| Idl<br/>                      | <dl> <dt>N/V</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ORPC \_ INIT \_ ARGS**](orpc-init-args.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 

