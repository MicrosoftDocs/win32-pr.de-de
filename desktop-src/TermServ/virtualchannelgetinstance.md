---
title: VirtualChannelGetInstance-Einstiegspunkt
description: Wird aufgerufen, damit das Plug-In eine Instanz der IWTSPlugin-Schnittstelle für alle Plug-Ins erstellt, die von der DLL implementiert werden.
ms.assetid: B81BD61E-1F43-42C9-8839-30F4F4C3973C
ms.tgt_platform: multiple
keywords:
- VirtualChannelGetInstance-Einstiegspunkt Remotedesktopdienste
topic_type:
- apiref
api_name:
- VirtualChannelGetInstance
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f96eac56f737d6f945c3d59d5cdf844e9cc65058a0460f620e6051830806ab99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868620"
---
# <a name="virtualchannelgetinstance-entry-point"></a>VirtualChannelGetInstance-Einstiegspunkt

Wird aufgerufen, damit das Plug-In eine Instanz der [**IWTSPlugin-Schnittstelle**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) für alle Plug-Ins erstellt, die von der DLL implementiert werden.

> [!Note]
>
> Diese Funktion wird vom Plug-In implementiert und muss anhand des Namens exportiert werden, damit eine Anwendung die [**Funktionen LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden kann, um dynamisch eine Verknüpfung mit der Funktion zu erstellen.
>
> Der Prototyp für diese Funktion ist in keiner öffentlichen Headerdatei enthalten, daher müssen Sie ihn genau wie gezeigt deklarieren.

 

## <a name="syntax"></a>Syntax


```C++
HRESULT VCAPITYPE VirtualChannelGetInstance(
  _In_    REFIID refiid,
  _Inout_ ULONG  *pNumObjs,
  _Out_   VOID   **ppObjArray
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*refiid* \[ In\]
</dt> <dd>

Gibt den Typ der zurückzugebenden Schnittstelle an. Dies muss **IID \_ IWTSPlugin** sein.

</dd> <dt>

*pNumObjs* \[ in, out\]
</dt> <dd>

Die Adresse einer **ULONG-Variablen,** die die Anzahl der abgerufenen Schnittstellen empfängt.

</dd> <dt>

*ppObjArray* \[ out\]
</dt> <dd>

Die Adresse eines Arrays von Zeigern, das die Schnittstellenzeiger empfängt. Wenn dieser Parameter **NULL** ist, muss die Implementierung die Anzahl der von der DLL implementierten Plug-Ins im *pNumObjs-Parameter* angeben. Dadurch kann der Aufrufer das richtige Größenarray für *ppObjArray* zuordnen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn dieser Einstiegspunkt erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



 

