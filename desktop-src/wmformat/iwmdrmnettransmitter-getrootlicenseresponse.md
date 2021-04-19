---
title: Iwmdrmnettransmitter getrootlicenseresponse-Methode (wmdrmsdk. h)
description: Die getrootlicenseresponse-Methode generiert eine Stamm Lizenz-Antwortnachricht.
ms.assetid: c735ee52-f0e0-4404-881b-18ee9a7fa9f9
keywords:
- Getrootlicenseresponse-Methode Windows Media-Format
- Getrootlicenseresponse-Methode, Windows Media-Format, iwmdrmnettransmitter-Schnittstelle
- Iwmdrmnettransmitter-Schnittstelle Windows Media-Format, getrootlicenseresponse-Methode
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.GetRootLicenseResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3497a3eaedb872b7d2c9eb5d7782d01f8b35462
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359345"
---
# <a name="iwmdrmnettransmittergetrootlicenseresponse-method"></a>Iwmdrmnettransmitter:: getrootlicenseresponse-Methode

Die **getrootlicenseresponse** -Methode generiert eine Stamm Lizenz-Antwortnachricht.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetRootLicenseResponse(
  [in]  BSTR  bstrKID,
  [out] BYTE  **ppbLicenseResponse,
  [out] DWORD *pcbLicenseResponse
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrinkid* \[ in\]
</dt> <dd>

Base64-codierter Schlüssel Bezeichner, der für die neue Stamm Lizenz verwendet werden soll. Der Schlüssel Bezeichner muss ein zufällig generierter GUID-Wert sein.

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

Die generierte Stamm Lizenz wird mithilfe der Informationen aus den Lizenz Abfrage Daten erstellt, die für die Schnittstelle verarbeitet werden, indem [**setlicensechallenge**](iwmdrmnettransmitter-setlicensechallenge.md)aufgerufen wird.

Die Stamm Lizenz wird bei der Generierung von Blatt Lizenzen verwendet. Dies wird durch Aufrufen der [**getleaflicenseresponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) -Methode erreicht. Die **iwmdrmnettransmitter** -Schnittstelle verwaltet eine Kopie der Stamm Lizenz für diese Verwendung.

Die Stamm Lizenz, die durch den Aufruf dieser Methode erstellt wurde, verfügt über keine Richtlinien und ist so konfiguriert, dass Sie auf dem empfangenden Gerät nicht persistent gespeichert werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmdrmnettransmitter-Schnittstelle**](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





