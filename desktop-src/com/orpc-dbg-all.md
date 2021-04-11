---
title: ORPC_DBG_ALL Struktur
description: Die ORPC \_ dbg \_ all-Struktur wird verwendet, um Parameter an die Methoden der iorpcdebugnotify-Schnittstelle zu übergeben.
ms.assetid: 05371beb-9202-40a6-96d2-4b91497e2ee9
keywords:
- COM für ORPC_DBG_ALL Struktur
- LPORPC_DBG_ALL Struktur Zeiger com
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
ms.openlocfilehash: a17f5b09e5fe2f668bf2bcd21e2e7fe6f0f766a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103259"
---
# <a name="orpc_dbg_all-structure"></a>ORPC \_ dbg \_ all-Struktur

Die **ORPC \_ dbg \_ all** -Struktur wird verwendet, um Parameter an die Methoden der [**iorpcdebugnotify**](iorpcdebugnotify.md) -Schnittstelle zu übergeben.

> [!Note]  
> Jede Methode der [**iorpcdebugnotify**](iorpcdebugnotify.md) -Schnittstelle verwendet eine andere Kombination der nachfolgenden Elemente. Wenn ein Member nicht als von einer Methode verwendet angegeben wird, ist er nicht definiert, wenn er an diese Methode übermittelt wird.

 

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

**psignature**
</dt> <dd>

Ein Zeiger auf einen **Byte** Puffer, der Folgendes enthält:

-   Die ersten vier Bytes: die ASCII-Zeichen "Marb" in zunehmender Speicher Reihenfolge.
-   Nächste 16 Bytes: eine **GUID** , die die aufgerufene Benachrichtigung identifiziert. Sie enthält eine der folgenden:
    1.  [**Clientgetbuffersize**](iorpcdebugnotify-clientgetbuffersize.md): 9ed14f 80-9673-101A-b07b-00dd01113f
    2.  [**Clientfillbuffer**](iorpcdebugnotify-clientfillbuffer.md):D a45f3e0-9673-101 a-B07B-00dd01113f 11
    3.  [**Clientnotify**](iorpcdebugnotify-clientnotify.md): 4b60e540-9674-101A-b07b-00dd01113f
    4.  [**Servernotify**](iorpcdebugnotify-servernotify.md): 1084fa00-9674-101A-b07b-00dd01113voll ständig verfügbar
    5.  [**Servergetbuffersize**](iorpcdebugnotify-servergetbuffersize.md): 22080240-9674-101A-b07b-00dd01113f
    6.  [**Serverfillbuffer**](iorpcdebugnotify-serverfillbuffer.md): 2fc09500-9674-101A-b07b-00dd01113f
-   Nächste vier Bytes: für die zukünftige Verwendung reserviert.

> [!Note]
>
> Wird von allen Methoden der [**iorpcdebugnotify**](iorpcdebugnotify.md) -Schnittstelle verwendet.

 

</dd> <dt>

**pMessage**
</dt> <dd>

Ein Zeiger auf eine [**rpcolemess**](/windows/win32/api/objidlbase/ns-objidlbase-rpcolemessage) -Struktur, die Informationen zu RPC-Daten Marshalling enthält.

> [!Note]
>
> Wird von den Methoden [**clientfillbuffer**](iorpcdebugnotify-clientfillbuffer.md), [**clientgetbuffersize**](iorpcdebugnotify-clientgetbuffersize.md), [**clientnotify**](iorpcdebugnotify-clientnotify.md), [**serverfillbuffer**](iorpcdebugnotify-serverfillbuffer.md), [**servergetbuffersize**](iorpcdebugnotify-servergetbuffersize.md)und [**servernotify**](iorpcdebugnotify-servernotify.md) verwendet.

 

</dd> <dt>

**REFIID**
</dt> <dd>

Ein Zeiger auf die IID der [**iorpcdebug**](iorpcdebugnotify.md) -Schnittstelle.

> [!Note]
>
> Wird von den Methoden [**clientfillbuffer**](iorpcdebugnotify-clientfillbuffer.md), [**clientgetbuffersize**](iorpcdebugnotify-clientgetbuffersize.md), [**clientnotify**](iorpcdebugnotify-clientnotify.md), [**serverfillbuffer**](iorpcdebugnotify-serverfillbuffer.md), [**servergetbuffersize**](iorpcdebugnotify-servergetbuffersize.md)und [**servernotify**](iorpcdebugnotify-servernotify.md) verwendet.

 

</dd> <dt>

**pChannel**
</dt> <dd>

Ein Zeiger auf die Schnittstelle " [**iripcchannelbuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) " der com-RPC-Kanal Implementierung auf dem Server.

> [!Note]
>
> Wird von der [**serverfillbuffer**](iorpcdebugnotify-serverfillbuffer.md)-, [**servergetbuffersize**](iorpcdebugnotify-servergetbuffersize.md)-und [**servernotify**](iorpcdebugnotify-servernotify.md) -Methode verwendet.

 

</dd> <dt>

**punkproxymgr**
</dt> <dd>

Ein Zeiger auf die [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) -Schnittstelle des Objekts, das an diesem Debugger-Aufruf beteiligt ist. Kann **null** sein. Dadurch wird jedoch die Debugger-Funktionalität reduziert.

> [!Note]
>
> Wird von den Methoden [**clientfillbuffer**](iorpcdebugnotify-clientfillbuffer.md), [**clientgetbuffersize**](iorpcdebugnotify-clientgetbuffersize.md)und [**clientnotify**](iorpcdebugnotify-clientnotify.md) verwendet.

 

</dd> <dt>

**pinterface**
</dt> <dd>

Ein Zeiger auf die COM-Schnittstelle der Methode, die von diesem RPC aufgerufen wird. Darf nicht **null** sein.

> [!Note]
>
> Wird von der [**serverfillbuffer**](iorpcdebugnotify-serverfillbuffer.md)-, [**servergetbuffersize**](iorpcdebugnotify-servergetbuffersize.md)-und [**servernotify**](iorpcdebugnotify-servernotify.md) -Methode verwendet.

 

</dd> <dt>

**pUnkObject**
</dt> <dd>

Muss **null** sein.

> [!Note]
>
> Wird von der [**serverfillbuffer**](iorpcdebugnotify-serverfillbuffer.md)-, [**servergetbuffersize**](iorpcdebugnotify-servergetbuffersize.md)-und [**servernotify**](iorpcdebugnotify-servernotify.md) -Methode verwendet.

 

</dd> <dt>

**HRESULT**
</dt> <dd>

Der Zweck dieses Members ändert sich für jede der folgenden Benachrichtigungen:

[**Clientgetbuffersize**](iorpcdebugnotify-clientgetbuffersize.md): die Anzahl von Bytes, die vom Client Debugger an den Server Debugger übertragen werden. Wenn der Wert NULL ist, müssen keine Informationen übertragen werden.

[**Clientnotify**](iorpcdebugnotify-clientnotify.md): das **HRESULT** des letzten RPC.

[**Servergetbuffersize**](iorpcdebugnotify-servergetbuffersize.md): die Anzahl von Bytes, die vom Client Debugger an den Server Debugger übertragen werden. Wenn der Wert NULL ist, müssen keine Informationen übertragen werden.

> [!Note]
>
> Wird von der [**clientgetbuffersize**](iorpcdebugnotify-clientgetbuffersize.md)-, [**clientnotify**](iorpcdebugnotify-clientnotify.md)-und [**servergetbuffersize**](iorpcdebugnotify-servergetbuffersize.md) -Methode verwendet.

 

</dd> <dt>

**umschließt**
</dt> <dd>

Ein Zeiger auf eine [**ORPC \_ dbg- \_ Puffer**](orpc-dbg-buffer.md) Struktur, die die per RPC gemarshallte Debuginformationen enthält. Ist nicht definiert, wenn **cbbuffer** NULL ist.

> [!Note]
>
> Wird von der [**clientfillbuffer**](iorpcdebugnotify-clientfillbuffer.md)-, [**clientnotify**](iorpcdebugnotify-clientnotify.md)-, [**serverfillbuffer**](iorpcdebugnotify-serverfillbuffer.md)-und [**servernotify**](iorpcdebugnotify-servernotify.md) -Methode verwendet.

 

</dd> <dt>

**cbbuffer**
</dt> <dd>

Die Länge (in Byte) der Daten, auf die von **pvbuffer** verwiesen wird.

> [!Note]
>
> Wird von der [**clientfillbuffer**](iorpcdebugnotify-clientfillbuffer.md)-, [**clientnotify**](iorpcdebugnotify-clientnotify.md)-, [**serverfillbuffer**](iorpcdebugnotify-serverfillbuffer.md)-und [**servernotify**](iorpcdebugnotify-servernotify.md) -Methode verwendet.

 

</dd> <dt>

**lpcbbuffer**
</dt> <dd>

Die Anzahl von Bytes, die vom Client Debugger an den Server Debugger übertragen werden. Wenn der Wert NULL ist, müssen keine Informationen übertragen werden. Dieser Wert ersetzt den Wert, der in **HRESULT** zurückgegeben wird.

> [!Note]
>
> Wird von der [**clientfillbuffer**](iorpcdebugnotify-clientfillbuffer.md)-Methode, der [**clientgetbuffersize**](iorpcdebugnotify-clientgetbuffersize.md) -Methode verwendet.

 

</dd> <dt>

**bleiben**
</dt> <dd>

Reserviert. Darf nicht verwendet werden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>N/V</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ORPC \_ dbg- \_ Puffer**](orpc-dbg-buffer.md)
</dt> <dt>

[**ORPC-init-Argumente \_ \_**](orpc-init-args.md)
</dt> <dt>

[**Dlldebugobjectrpchook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**Iorpcdebug-Benachrichtigung**](iorpcdebugnotify.md)
</dt> </dl>

 

