---
title: Iwmdrmnettransmitter getleaflicenseresponse-Methode (wmdrmsdk. h)
description: Die getleaflicenseresponse-Methode generiert eine Blatt Lizenz-Antwortnachricht.
ms.assetid: b2893d22-b6f3-44d2-b6db-e2b07fbe098d
keywords:
- Getleaflicenseresponse-Methode, Windows Media-Format
- Getleaflicenseresponse-Methode, Windows Media-Format, iwmdrmnettransmitter-Schnittstelle
- Iwmdrmnettransmitter-Schnittstelle Windows Media-Format, getleaflicenseresponse-Methode
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.GetLeafLicenseResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf2374966abfae4353a72755313c1cbbdfb7287
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351211"
---
# <a name="iwmdrmnettransmittergetleaflicenseresponse-method"></a>Iwmdrmnettransmitter:: getleaflicenseresponse-Methode

Die **getleaflicenseresponse** -Methode generiert eine Blatt Lizenz-Antwortnachricht.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetLeafLicenseResponse(
  [in]  BSTR            bstrKID,
  [in]  WMDRMNET_POLICY *pPolicy,
  [out] IWMDRMEncrypt   **ppIWMDRMEncrypt,
  [out] BYTE            **ppbLicenseResponse,
  [out] DWORD           *pcbLicenseResponse
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrinkid* \[ in\]
</dt> <dd>

Base64-codierter Schlüssel Bezeichner, der für die neue Blatt Lizenz verwendet werden soll. Der Schlüssel Bezeichner muss ein zufällig generierter GUID-Wert sein.

</dd> <dt>

*pPolicy* \[ in\]
</dt> <dd>

Ein Zeiger auf die [**wmdrmnet- \_ Richtlinien**](wmdrmnet-policy.md) Struktur, die die Richtlinie definiert, die für die Blatt Lizenz verwendet werden soll.

</dd> <dt>

*ppiwmdrmencrypt* \[ vorgenommen\]
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf die [**iwmdrmencrypt**](iwmdrmencrypt.md) -Schnittstelle empfängt, die zum Verschlüsseln von Daten für die neue Blatt Lizenz verwendet werden kann.

</dd> <dt>

*ppblicenseresponse* \[ vorgenommen\]
</dt> <dd>

Adresse einer Variablen, die die Adresse der generierten Lizenz Antwort empfängt. Wenn Sie mit diesen Daten fertig sind, müssen Sie den Arbeitsspeicher freigeben, indem Sie " **CoTaskMemFree**" aufrufen.

</dd> <dt>

*pcblicenseresponse* \[ vorgenommen\]
</dt> <dd>

Adresse einer Variablen, die die Größe der Lizenz Antwort erhält (in Bytes).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                                | Beschreibung                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**NS \_ E \_ DRM- \_ RIV \_ zu \_ klein**</dt> </dl> | Es wird eine aktualisierte Inhalts Sperr Liste benötigt.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Die Methode wurde erfolgreich ausgeführt.<br/>                         |



 

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmdrmnettransmitter-Schnittstelle**](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





