---
title: Ideviceicon-ContentType-Methode
description: Ruft den Inhaltstyp des Symbols ab.
ms.assetid: 01928A98-B7D0-4523-9259-81FEB33F052E
keywords:
- ContentType-Methode Medien Streaming-API
- ContentType-Methode Medien Streaming-API, ideviceicon-Schnittstelle
- Ideviceicon Interface Medien Streaming-API, ContentType-Methode
topic_type:
- apiref
api_name:
- IDeviceIcon.ContentType
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af48aabb2a64f4c4b8fbd40a3859acc82496a399
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858177"
---
# <a name="ideviceiconcontenttype-method"></a>Ideviceicon:: ContentType-Methode

Ruft den Inhaltstyp des Symbols ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT ContentType(
  [out] HSTRING *value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Wert* \[ vorgenommen\]
</dt> <dd>

Empfängt einen Zeiger auf den Inhaltstyp des Symbols.

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

 

