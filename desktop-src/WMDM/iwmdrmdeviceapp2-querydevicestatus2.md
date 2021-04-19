---
title: IWMDRMDeviceApp2 QueryDeviceStatus2-Methode (wmdrmdeviceapp. h)
description: Die QueryDeviceStatus2-Methode fragt ein Gerät nach einem bestimmten DRM-Status oder einer bestimmten Funktion ab.
ms.assetid: f7e95fb7-5929-4a70-8580-a443e152e6d1
keywords:
- QueryDeviceStatus2-Methode Windows Media Device Manager
- QueryDeviceStatus2-Methode, Windows Media Device Manager, IWMDRMDeviceApp2-Schnittstelle
- IWMDRMDeviceApp2-Schnittstelle Windows Media Device Manager, QueryDeviceStatus2-Methode
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp2.QueryDeviceStatus2
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 338d1f03f8d1e63086bb260c9854c7dcf3e88514
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366737"
---
# <a name="iwmdrmdeviceapp2querydevicestatus2-method"></a>IWMDRMDeviceApp2:: QueryDeviceStatus2-Methode

Die **QueryDeviceStatus2** -Methode fragt ein Gerät nach einem bestimmten DRM-Status oder einer bestimmten Funktion ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT QueryDeviceStatus2(
  [in]  IWMDMDevice *pDevice,
  [in]  DWORD       dwFlags,
  [out] DWORD       *pdwStatus
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdevice* \[ in\]
</dt> <dd>

Zeiger auf ein [**iwmdmdevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) -Objekt.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Einer oder mehrere der folgenden **DWORD** -Werte, die angeben, welche Funktionen angefordert werden sollen, kombiniert mit einem bitweisen **or**.



| Flag                              | Beschreibung                                                                  |
|-----------------------------------|------------------------------------------------------------------------------|
| WMDRM- \_ Abfrage \_ Client \_ indivstatus | Fragen Sie ab, ob die DRM-Komponenten des Computers individualisiert werden müssen.       |
| WMDRM- \_ Abfrage \_ Gerät \_ Clockstatus | Fragen Sie ab, ob die sichere Uhr des Geräts hinzugefügt oder aktualisiert werden muss.        |
| WMDRM- \_ Abfrage \_ Gerät wurde \_ gesperrt.   | Fragen Sie ab, ob das Gerät widerrufen wurde.                                         |
| WMDRM- \_ Abfrage \_ Gerät \_ iswmdrm     | Fragen Sie ab, ob das Gerät Windows Media DRM 10 für tragbare Geräte unterstützt. |



 

</dd> <dt>

*pdwstatus* \[ vorgenommen\]
</dt> <dd>

NULL oder mehr der folgenden **DWORD** -Werte, die den angeforderten Gerätestatus in Kombination mit einem bitweisen **or** angeben.



| Status                      | BESCHREIBUNG                                              |
|-----------------------------|----------------------------------------------------------|
| WMDRM- \_ Gerät \_ iswmdrm      | Das Gerät unterstützt Windows Media DRM.                   |
| WMDRM- \_ Geräte- \_ needclock    | Das Gerät hat keine sichere Uhr.                 |
| WMDRM- \_ Gerät gesperrt \_      | Das Gerät wurde widerrufen.                             |
| WMDRM- \_ Client- \_ needindiv    | Die DRM-Komponenten des Computers müssen individualisiert werden. |
| WMDRM- \_ Geräte \_ Erfrischung | Die Uhr muss aktualisiert werden.                         |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                                              | Beschreibung                                                               |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                     | Die Methode wurde erfolgreich ausgeführt.<br/>                                          |
| <dl> <dt>**DRM \_ E \_ invalidArg**</dt> </dl>                        | Mindestens ein Argument ist ungültig.<br/>                           |
| <dl> <dt>**\_Ungültiges NS E- \_ DRM- \_ \_ Zertifikat**</dt> </dl>          | Das vom Gerät abgerufene Gerätezertifikat ist ungültig.<br/> |
| <dl> <dt>**NS \_ E \_ DRM \_ kann \_ das \_ \_ Geräte \_ Zertifikat nicht erhalten.**</dt> </dl> | Fehler beim Abrufen des Geräte Zertifikats vom Gerät.<br/>     |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode sollte aufgerufen werden, bevor Eingeschränkte Aktionen für DRM-Inhalte durchgeführt werden, z. b. das Übertragen von DRM-Inhalten auf das Gerät oder das Abrufen von Messungs Informationen. Wenn die von *pdwstatus* abgerufenen Werte angeben, dass eine Aktion ausgeführt werden muss (z. b. für den Desktop oder das Abrufen einer Uhr für das Gerät), sollte die [**Anwendung iwmdrmdeviceapp:: acquiredevicedata**](iwmdrmdeviceapp-acquiredevicedata.md) aufrufen und den abgerufenen *pdwstatus* -Wert aus dieser Funktion an den *dwFlags* -Parameter in **acquiredevicedata** übergeben. Wenn 0 (null) zurückgegeben wird, unterstützt das Gerät Windows Media DRM 10 für tragbare Geräte nicht, und es müssen keine Aktionen durchgeführt werden. Weitere Informationen finden Sie [unter behandeln geschützter Inhalte in der Anwendung](handling-protected-content-in-the-application.md) .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmdeviceapp. h (erfordert auch wmdrmdeviceapp \_ i. c, erstellt von wmdrmdeviceapp. idl)</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>Mssachlp. lib</dt> </dl>                                                                        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Behandeln geschützter Inhalte in der Anwendung**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**Iwmdrmdeviceapp:: querydevicestatus**](iwmdrmdeviceapp-querydevicestatus.md)
</dt> <dt>

[**IWMDRMDeviceApp2-Schnittstelle**](iwmdrmdeviceapp2.md)
</dt> </dl>

 

 





