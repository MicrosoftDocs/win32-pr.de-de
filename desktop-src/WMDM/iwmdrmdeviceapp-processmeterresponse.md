---
title: Iwmdrmdeviceapp processmeterresponse-Methode (wmdrmdeviceapp. h)
description: Die processmeterresponse-Methode setzt einige oder alle Messungs Zähler auf einem Gerät zurück, nachdem die Daten vom Gerät an den Server gesendet und vom Server verarbeitet wurden.
ms.assetid: bafc4bb2-aa3c-4b2a-a818-1a78577cefc5
keywords:
- Processmeterresponse-Methode (Windows Media Device Manager)
- Processmeterresponse-Methode Windows Media Device Manager, iwmdrmdeviceapp-Schnittstelle
- Iwmdrmdeviceapp-Schnittstelle Windows Media Device Manager, processmeterresponse-Methode
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.ProcessMeterResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b57312dc2f401207e41f38f5bf75cddf69a13b1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372375"
---
# <a name="iwmdrmdeviceappprocessmeterresponse-method"></a>Iwmdrmdeviceapp::P rocess Meter Response-Methode

Die **processmeterresponse** -Methode setzt einige oder alle Messungs Zähler auf einem Gerät zurück, nachdem die Daten vom Gerät an den Server gesendet und vom Server verarbeitet wurden.

## <a name="syntax"></a>Syntax


```C++
HRESULT ProcessMeterResponse(
  [in]  IWMDMDevice *pDevice,
  [in]  BYTE        *pbResponse,
  [in]  DWORD       cbResponse,
  [out] DWORD       *pdwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdevice* \[ in\]
</dt> <dd>

Zeiger auf ein [**iwmdmdevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) -Objekt.

</dd> <dt>

*pbresponse* \[ in\]
</dt> <dd>

Antwort von einem Messungs Server nach dem Senden von Daten, die mithilfe von [**generatemeterchallenge**](iwmdrmdeviceapp-generatemeterchallenge.md)generiert wurden.

</dd> <dt>

*cbresponse* \[ in\]
</dt> <dd>

Größe von *pbresponse* in Bytes.

</dd> <dt>

*pdwflags* \[ vorgenommen\]
</dt> <dd>

Ein **DWORD** aus der folgenden Tabelle, das angibt, ob auf dem zu verarbeitenden Gerät weitere Messungs Daten vorhanden sind.



| Flag                            | Beschreibung                                     |
|---------------------------------|-------------------------------------------------|
| WMDRM- \_ Zähler für \_ \_ alle Zähler     | Alle Messungs Daten wurden verarbeitet.           |
| WMDRM- \_ Messgeräte \_ Antwort \_ partiell | Zusätzliche Messungs Daten müssen verarbeitet werden. |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                                      | Beschreibung                                                                   |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                             | Die Methode wurde erfolgreich ausgeführt.<br/>                                              |
| <dl> <dt>**DRM \_ E \_ invalidArg**</dt> </dl>                | Mindestens ein Argument ist ungültig.<br/>                               |
| <dl> <dt>**Fehler des Geräts**</dt> </dl>            | Eine beliebige Anzahl von Gerätefehlern.<br/>                                  |
| <dl> <dt>**Fehler vom DRM-Client**</dt> </dl>        | Eine beliebige Anzahl interner DRM-Client Fehler.<br/>                     |
| <dl> <dt>**NS \_ E \_ Gerät \_ nicht \_ WMDRM- \_ Gerät**</dt> </dl> | Das angegebene Gerät ist kein Windows Media DRM-kompatibles Gerät.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Weitere Informationen zur Messung, einschließlich Codebeispielen, finden Sie im Whitepaper [Messung der Verwendung digitaler Medieninhalte mit Windows Media DRM 10](/previous-versions//bb614723(v=vs.85)) auf der MSDN-Website.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmdeviceapp. h (erfordert auch wmdrmdeviceapp \_ i. c, erstellt von wmdrmdeviceapp. idl)</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>Mssachlp. lib</dt> </dl>                                                                        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Behandeln geschützter Inhalte in der Anwendung**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**Iwmdmdevice-Schnittstelle**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> <dt>

[**Iwmdrmdeviceapp-Schnittstelle**](iwmdrmdeviceapp.md)
</dt> </dl>

 

