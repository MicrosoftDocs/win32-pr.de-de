---
title: Ideviceicon-streammethode
description: Ruft das Symbol als Datenstrom ab.
ms.assetid: 0B9E852F-4F72-4721-8F88-24A850A088C4
keywords:
- Stream-Methode Medien Streaming-API
- Stream-Methode Medien Streaming-API, ideviceicon-Schnittstelle
- Ideviceicon-Schnittstelle Medien Streaming-API, Stream-Methode
topic_type:
- apiref
api_name:
- IDeviceIcon.Stream
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fd00d757fceb90cf5ee7199256b003464063abcb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315086"
---
# <a name="ideviceiconstream-method"></a>Ideviceicon:: Stream-Methode

Ruft das Symbol als Datenstrom ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT Stream(
  [out] IRandomAccessStreamWithContentType **value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wert* \[ vorgenommen\]
</dt> <dd>

Empfängt einen Verweis auf einen " [**tyandomaccessstreamwithcontenttype**](/uwp/api/Windows.Storage.Streams.IRandomAccessStreamWithContentType) ", der zum Abrufen der Bilddaten verwendet werden kann.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ideviceicon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)
</dt> </dl>

 

