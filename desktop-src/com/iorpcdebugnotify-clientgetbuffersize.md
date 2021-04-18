---
title: Iorpcdebugnotify clientgetbuffersize-Methode
description: Ruft die RPC-Puffergröße aus dem Client seitigen Debugger ab.
ms.assetid: 05475156-1508-4eb2-82a6-bb1701839fbd
keywords:
- Clientgetbuffersize-Methode com
- Clientgetbuffersize-Methode com, iorpcdebugnotify-Schnittstelle
- Iorpcdebugnotify-Schnittstelle com, clientgetbuffersize-Methode
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ClientGetBufferSize
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50bd925b9c518c78ca37aa8219a00965f398c415
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339601"
---
# <a name="iorpcdebugnotifyclientgetbuffersize-method"></a>Iorpcdebugnotify:: clientgetbuffersize-Methode

Ruft die RPC-Puffergröße aus dem Client seitigen Debugger ab.

> [!Note]  
> Eine Import Bibliothek mit der Funktion " **clientgetbuffersize** " ist nicht im Microsoft Windows Software Development Kit (SDK) enthalten. Eine Anwendung kann die Funktionen [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) und [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) verwenden, um aus oleaut.dll einen Funktionszeiger auf [**dlldebugobjectrpchook**](dlldebugobjectrpchook.md) abzurufen und diese Funktion über die [**iorpcdebugnotify**](iorpcdebugnotify.md) -Schnittstelle bereitzustellen.

 

## <a name="syntax"></a>Syntax


```C++
void ClientGetBufferSize(
   ORPC_DBG_ALL *lpOrpcDebugAll
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lporpcdebug* 
</dt> <dd>

Ein Zeiger auf eine [**ORPC \_ dbg \_ all**](orpc-dbg-all.md) -Struktur, die Benachrichtigungs spezifische Informationen enthält, die das com-RPC-System an den Debugger übergibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>N/V</dt> </dl> |
| IDL<br/>                      | <dl> <dt>N/V</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ORPC-init-Argumente \_ \_**](orpc-init-args.md)
</dt> <dt>

[**Dlldebugobjectrpchook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**Iorpcdebug-Benachrichtigung**](iorpcdebugnotify.md)
</dt> </dl>

 

