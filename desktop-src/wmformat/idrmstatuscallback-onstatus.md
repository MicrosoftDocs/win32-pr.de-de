---
title: IDRMStatusCallback OnStatus-Methode
description: Die OnStatus-Methode empfängt Statusmeldungen von asynchronen DRM-Prozessen.
ms.assetid: 2a128088-0924-4c54-b08d-a1c7ea91e541
keywords:
- OnStatus-Methode windows Media Format
- OnStatus-Methode Windows Media Format, IDRMStatusCallback-Schnittstelle
- IDRMStatusCallback-Schnittstelle windows Media Format , OnStatus-Methode
topic_type:
- apiref
api_name:
- IDRMStatusCallback.OnStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2c9f8c0424752ababe684b426d78001f2783d62db9781fe3d6a23ed002e91773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847454"
---
# <a name="idrmstatuscallbackonstatus-method"></a>IDRMStatusCallback::OnStatus-Methode

Die **OnStatus-Methode** empfängt Statusmeldungen von asynchronen DRM-Prozessen.

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

*Status* \[ In\]
</dt> <dd>

Statuscode. Nachrichtencodes werden im **MSDRM \_ STATUS-Enumerationstyp** definiert.

</dd> <dt>

*hr* \[ In\]
</dt> <dd>

Gibt Code zurück, der die Statusmeldung unterstützt.

</dd> <dt>

*dwType* \[ In\]
</dt> <dd>

Typ der Daten, auf die *pValue zeigt.* Legen Sie auf einen der Werte der [**DRM \_ ATTR \_ DATATYPE-Enumeration**](drm-attr-datatype.md) fest.

</dd> <dt>

*pValue* \[ In\]
</dt> <dd>

Zeiger auf Daten im Zusammenhang mit der Statusmeldung. Der Datentyp wird durch den Wert des *dwType-Parameters* bestimmt. Weitere Informationen finden Sie in der [**DRM \_ ATTR \_ DATATYPE-Enumeration.**](drm-attr-datatype.md)

</dd> <dt>

*pvContext* \[ In\]
</dt> <dd>

Optionaler Parameter, der verwendet werden kann, um das Objekt zu identifizieren, das die Nachricht gesendet hat. Durch Festlegen *von pvContext* beim Registrieren dieses Rückrufs können Sie denselben Rückruf verwenden, um mehrere asynchrone Prozesse zu verarbeiten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DRM \_ \_ ATTR-DATENTYP**](drm-attr-datatype.md)
</dt> <dt>

[**IDRMStatusCallback-Schnittstelle**](idrmstatuscallback.md)
</dt> </dl>

 

 





