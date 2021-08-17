---
title: IDeviceIcon ContentType-Methode
description: Ruft den Inhaltstyp des Symbols ab.
ms.assetid: 01928A98-B7D0-4523-9259-81FEB33F052E
keywords:
- 'ContentType-Methode: Media Streaming-API'
- 'ContentType-Methode: Media Streaming-API, IDeviceIcon-Schnittstelle'
- IDeviceIcon-Schnittstelle Media Streaming-API, ContentType-Methode
topic_type:
- apiref
api_name:
- IDeviceIcon.ContentType
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d8fb9cb639381b60bb59965d12ce3f0545daf6d2725cde69d3dea3dee589f8f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461744"
---
# <a name="ideviceiconcontenttype-method"></a>IDeviceIcon::ContentType-Methode

Ruft den Inhaltstyp des Symbols ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT ContentType(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*value* \[ out\]
</dt> <dd>

Empfängt einen Zeiger auf den Inhaltstyp des Symbols.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon)
</dt> </dl>

 

