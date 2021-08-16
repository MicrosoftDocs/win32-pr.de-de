---
title: ORPC_DBG_ALL-Struktur
description: Die ORPC \_ DBG \_ ALL-Struktur wird verwendet, um Parameter an die Methoden der IOrpcDebugNotify-Schnittstelle zu übergeben.
ms.assetid: 05371beb-9202-40a6-96d2-4b91497e2ee9
keywords:
- ORPC_DBG_ALL-Struktur:COM
- LPORPC_DBG_ALL-Strukturzeiger COM
topic_type:
- apiref
api_name:
- ORPC_DBG_ALL
api_location:
- N/A
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 359e3b3ec2530917c6a502da90ea86771238319687f8dcf8e9b7862e4ddf1954
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118310304"
---
# <a name="orpc_dbg_all-structure"></a>ORPC \_ DBG \_ ALL-Struktur

Die **ORPC \_ DBG \_ ALL-Struktur** wird verwendet, um Parameter an die Methoden der [**IOrpcDebugNotify-Schnittstelle**](iorpcdebugnotify.md) zu übergeben.

> [!Note]  
> Jede Methode der [**IOrpcDebugNotify-Schnittstelle**](iorpcdebugnotify.md) verwendet eine andere Kombination der folgenden Member. Wenn ein Member nicht als von einer Methode verwendet angegeben wird, ist er nicht definiert, wenn er an diese Methode übergeben wird.

 

## <a name="syntax"></a>Syntax


```C++
typedef struct ORPC_DBG_ALL {
  BYTE              *pSignature;
  RPCOLEMESSAGE     *pMessage;
  const IID         *refiid;
  IRpcChannelBuffer *pChannel;
  IUnknown          *pUnkProxyMgr;
  void              *pInterface;
  IUnknown          *pUnkObject;
  HRESULT           hresult;
  void              *pvBuffer;
  ULONG             *cbBuffer;
  ULONG             *lpcbBuffer;
  void              *reserved;
} ORPC_DBG_ALL, *LPORPC_DBG_ALL;
```



## <a name="members"></a>Member

<dl> <dt>

**pSignature**
</dt> <dd>

Ein Zeiger auf einen **BYTE-Puffer,** der Folgendes enthält:

-   Die ersten vier Bytes: die ASCII-Zeichen "MARB" in zunehmender Speicherreihenfolge.
-   Nächste 16 Bytes: Eine **GUID,** die die aufgerufene Benachrichtigung identifiziert. Sie enthält eine der folgenden Angaben:
    1.  [**ClientGetBufferSize:**](iorpcdebugnotify-clientgetbuffersize.md)9ED14F80-9673-101A-B07B-00DD01113F11
    2.  [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md):D A45F3E0-9673-101A-B07B-00DD01113F11
    3.  [**ClientNotify**](iorpcdebugnotify-clientnotify.md):4F60E540-9674-101A-B07B-00DD01113F11
    4.  [**ServerNotify**](iorpcdebugnotify-servernotify.md):1084FA00-9674-101A-B07B-00DD01113F11
    5.  [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md):22080240-9674-101A-B07B-00DD01113F11
    6.  [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md):2FC09500-9674-101A-B07B-00DD01113F11
-   Nächste vier Bytes: Für die zukünftige Verwendung reserviert.

> [!Note]
>
> Wird von allen Methoden der [**IOrpcDebugNotify-Schnittstelle**](iorpcdebugnotify.md) verwendet.

 

</dd> <dt>

**pMessage**
</dt> <dd>

Ein Zeiger auf eine [**RPCOLEMESSAGE-Struktur,**](/windows/win32/api/objidlbase/ns-objidlbase-rpcolemessage) die RPC-Daten marshallinginformationen enthält.

> [!Note]
>
> Wird von den Methoden [**ClientFillBuffer,**](iorpcdebugnotify-clientfillbuffer.md) [**ClientGetBufferSize,**](iorpcdebugnotify-clientgetbuffersize.md) [**ClientNotify,**](iorpcdebugnotify-clientnotify.md) [**ServerFillBuffer,**](iorpcdebugnotify-serverfillbuffer.md) [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)und [**ServerNotify**](iorpcdebugnotify-servernotify.md) verwendet.

 

</dd> <dt>

**Refiid**
</dt> <dd>

Ein Zeiger auf die IID der [**IOrpcDebugNotify-Schnittstelle.**](iorpcdebugnotify.md)

> [!Note]
>
> Wird von den Methoden [**ClientFillBuffer,**](iorpcdebugnotify-clientfillbuffer.md) [**ClientGetBufferSize,**](iorpcdebugnotify-clientgetbuffersize.md) [**ClientNotify,**](iorpcdebugnotify-clientnotify.md) [**ServerFillBuffer,**](iorpcdebugnotify-serverfillbuffer.md) [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)und [**ServerNotify**](iorpcdebugnotify-servernotify.md) verwendet.

 

</dd> <dt>

**pChannel**
</dt> <dd>

Ein Zeiger auf die [**IRpcChannelBuffer-Schnittstelle**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) der COM RPC-Kanalimplementierungen auf dem Server.

> [!Note]
>
> Wird von den Methoden [**ServerFillBuffer,**](iorpcdebugnotify-serverfillbuffer.md) [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)und [**ServerNotify**](iorpcdebugnotify-servernotify.md) verwendet.

 

</dd> <dt>

**pUnkProxyMgr**
</dt> <dd>

Ein Zeiger auf die [**IUnknown-Schnittstelle**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) des Objekts, das an diesem Debuggeraufruf beteiligt ist. Kann **NULL** sein, dies reduziert jedoch die Debuggerfunktionalität.

> [!Note]
>
> Wird von den Methoden [**ClientFillBuffer,**](iorpcdebugnotify-clientfillbuffer.md) [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md)und [**ClientNotify**](iorpcdebugnotify-clientnotify.md) verwendet.

 

</dd> <dt>

**pInterface**
</dt> <dd>

Ein Zeiger auf die COM-Schnittstelle der Methode, die von diesem RPC aufgerufen wird. Darf nicht **NULL** sein.

> [!Note]
>
> Wird von den Methoden [**ServerFillBuffer,**](iorpcdebugnotify-serverfillbuffer.md) [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)und [**ServerNotify**](iorpcdebugnotify-servernotify.md) verwendet.

 

</dd> <dt>

**pUnkObject**
</dt> <dd>

Muss **NULL** sein.

> [!Note]
>
> Wird von den Methoden [**ServerFillBuffer,**](iorpcdebugnotify-serverfillbuffer.md) [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)und [**ServerNotify**](iorpcdebugnotify-servernotify.md) verwendet.

 

</dd> <dt>

**Hresult**
</dt> <dd>

Der Zweck dieses Mitglieds ändert sich für jede der folgenden Benachrichtigungen:

[**ClientGetBufferSize:**](iorpcdebugnotify-clientgetbuffersize.md)Die Anzahl der Bytes, die der Clientdebugger an den Serverdebugger überträgt. Bei 0 (null) müssen keine Informationen übertragen werden.

[**ClientNotify:**](iorpcdebugnotify-clientnotify.md)das **HRESULT** des letzten RPC.

[**ServerGetBufferSize:**](iorpcdebugnotify-servergetbuffersize.md)Die Anzahl der Bytes, die der Clientdebugger an den Serverdebugger überträgt. Bei 0 (null) müssen keine Informationen übertragen werden.

> [!Note]
>
> Wird von den [**Methoden ClientGetBufferSize,**](iorpcdebugnotify-clientgetbuffersize.md) [**ClientNotify**](iorpcdebugnotify-clientnotify.md)und [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md) verwendet.

 

</dd> <dt>

**pvBuffer**
</dt> <dd>

Ein Zeiger auf eine [**ORPC \_ DBG \_ BUFFER-Struktur,**](orpc-dbg-buffer.md) die die debuginformationen für rpc-Marshalling enthält. Ist nicht definiert, wenn **cbBuffer** 0 (null) ist.

> [!Note]
>
> Wird von den Methoden [**ClientFillBuffer,**](iorpcdebugnotify-clientfillbuffer.md) [**ClientNotify,**](iorpcdebugnotify-clientnotify.md) [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)und [**ServerNotify**](iorpcdebugnotify-servernotify.md) verwendet.

 

</dd> <dt>

**cbBuffer**
</dt> <dd>

Die Länge der Daten, auf die **pvBuffer** verweist, in Bytes.

> [!Note]
>
> Wird von den Methoden [**ClientFillBuffer,**](iorpcdebugnotify-clientfillbuffer.md) [**ClientNotify,**](iorpcdebugnotify-clientnotify.md) [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)und [**ServerNotify**](iorpcdebugnotify-servernotify.md) verwendet.

 

</dd> <dt>

**lpcbBuffer**
</dt> <dd>

Die Anzahl der Bytes, die der Clientdebugger an den Serverdebugger überträgt. Bei 0 (null) müssen keine Informationen übertragen werden. Dieser Wert ersetzt den in **hresult** zurückgegebenen Wert.

> [!Note]
>
> Wird von den [**ClientFillBuffer-,**](iorpcdebugnotify-clientfillbuffer.md) [**ClientGetBufferSize-Methoden**](iorpcdebugnotify-clientgetbuffersize.md) verwendet.

 

</dd> <dt>

**reserved**
</dt> <dd>

Reserviert. Darf nicht verwendet werden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>N/V</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_ORPC-DBG-PUFFER \_**](orpc-dbg-buffer.md)
</dt> <dt>

[**ORPC \_ INIT \_ ARGS**](orpc-init-args.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 

