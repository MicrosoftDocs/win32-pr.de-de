---
title: Idrmstatuscallback OnStatus-Methode
description: Die OnStatus-Methode empfängt Statusmeldungen von asynchronen DRM-Prozessen.
ms.assetid: 2a128088-0924-4c54-b08d-a1c7ea91e541
keywords:
- OnStatus-Methode Windows Media-Format
- OnStatus-Methode Windows Media-Format, idrmstatuscallback-Schnittstelle
- Idrmstatuscallback-Schnittstelle Windows Media-Format, OnStatus-Methode
topic_type:
- apiref
api_name:
- IDRMStatusCallback.OnStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 754d59d74fb0365f423243e92565ac17b46628a5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104037848"
---
# <a name="idrmstatuscallbackonstatus-method"></a>Idrmstatuscallback:: OnStatus-Methode

Die **OnStatus** -Methode empfängt Statusmeldungen von asynchronen DRM-Prozessen.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnStatus(
  [in] MSDRM_STATUS      Status,
  [in] HRESULT           hr,
  [in] DRM_ATTR_DATATYPE dwType,
  [in] BYTE              *pValue,
  [in] void              *pvContext
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Status* \[ in\]
</dt> <dd>

Statuscode. Nachrichten Codes werden im Enumerationstyp " **msdrm- \_ Status** " definiert.

</dd> <dt>

*Personalabteilung* \[ in\]
</dt> <dd>

Rückgabecode, der die Statusmeldung unterstützt.

</dd> <dt>

*dwType* \[ in\]
</dt> <dd>

Der Typ der Daten, auf die von *pValue* verwiesen wird. Legen Sie auf einen der Werte der " [**DRM \_ attr \_ DataType**](drm-attr-datatype.md) "-Enumeration fest.

</dd> <dt>

*pValue* \[ in\]
</dt> <dd>

Zeiger auf Daten, die mit der Statusmeldung verknüpft sind. Der Typ der Daten wird durch den Wert des *dwType* -Parameters bestimmt. Weitere Informationen finden Sie in der " [**DRM \_ attr \_ DataType**](drm-attr-datatype.md) "-Enumeration.

</dd> <dt>

*pvcontext* \[ in\]
</dt> <dd>

Optionaler Parameter, der verwendet werden kann, um das Objekt zu identifizieren, das die Nachricht gesendet hat. Wenn Sie *pvcontext* festlegen, wenn Sie diesen Rückruf registrieren, können Sie denselben Rückruf verwenden, um mehrere asynchrone Prozesse zu verarbeiten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DRM- \_ attr- \_ Datentyp**](drm-attr-datatype.md)
</dt> <dt>

[**Idrmstatus Callback-Schnittstelle**](idrmstatuscallback.md)
</dt> </dl>

 

 





