---
title: IWMDRMLicenseQuery QueryLicenseState-Methode (Wmdrmsdk.h)
description: Die QueryLicenseState-Methode fragt den lokalen Lizenzspeicher nach Lizenzinformationen ab, die für eine Schlüssel-ID für ein oder mehrere bestimmte Rechte gelten.
ms.assetid: 17f40c56-2266-4c94-9e95-a33a92ddef74
keywords:
- 'QueryLicenseState-Methode : Windows Media Format'
- QueryLicenseState-Methode windows Media Format, IWMDRMLicenseQuery-Schnittstelle
- IWMDRMLicenseQuery-Schnittstelle windows Media Format , QueryLicenseState-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery.QueryLicenseState
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 580a9bf635a7a817c63e990b0215bb6b124d468f2437ecc32a6e7d8e2ddc560c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846820"
---
# <a name="iwmdrmlicensequeryquerylicensestate-method"></a>IWMDRMLicenseQuery::QueryLicenseState-Methode

Die **QueryLicenseState-Methode** fragt den lokalen Lizenzspeicher nach Lizenzinformationen ab, die für eine Schlüssel-ID für ein oder mehrere bestimmte Rechte gelten.

## <a name="syntax"></a>Syntax


```C++
HRESULT QueryLicenseState(
  [in]  BSTR                   bstrKID,
  [in]  DWORD                  cActionsToQuery,
  [in]  BSTR                   rgbstrActionsToQuery[],
  [out] DRM_LICENSE_STATE_DATA rgResultStateData[]
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrKID* \[ In\]
</dt> <dd>

Schlüssel-ID, für die eine Abfrage ausgeführt werden soll. Nur Lizenzen, die für diese Schlüssel-ID gelten, werden ausgewertet.

</dd> <dt>

*cActionsToQuery* \[ In\]
</dt> <dd>

Die Anzahl der Aktionen, für die eine Abfrage durchgeführt werden soll. Dieser Wert muss auf die Anzahl der Elemente in den Arrays festgelegt werden, die für die Parameter *rgbstrActionsToQuery* und *rgResultStateData übergeben* werden.

</dd> <dt>

*rgbstrActionsToQuery \[ \]* \[in\]
</dt> <dd>

Array mit einem oder mehr Rechten, für die eine Abfrage ausgeführt werden soll. Dieses Array muss so viele Elemente enthalten, wie von *cActionsToQuery angegeben.* Jedes Element muss auf eine der folgenden Konstanten festgelegt werden.



| Konstante                                        | Beschreibung                                                                                                                                        |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| g \_ wszWMDRM \_ LicenseState \_ Backup               | Fügen Sie ein, um details zum Recht zum Sichern und Wiederherstellen der Lizenz abfragt.                                                               |
| g \_ wszWMDRM \_ LicenseState \_ CollaborativePlay    | Fügen Sie ein, um die Details zum Recht zum Freigeben des Inhalts für eine Gruppe von Benutzern im Rahmen eines gemeinsamen Wiedergabeszenarios abfragt.          |
| g \_ wszWMDRM \_ LicenseState \_ Copy                 | Fügen Sie ein, um details zum Recht zum Kopieren des Inhalts auf externe Geräte oder Medien abfragt.                                                 |
| g \_ wszWMDRM \_ LicenseState \_ CopyToCD             | Fügen Sie ein, um die Details zum Recht zum Kopieren des Inhalts auf CD abfragt.                                                                        |
| g \_ wszWMDRM \_ LicenseState \_ CopyToNonSDMIDevice  | Fügen Sie ein, um details zum Recht zum Kopieren des Inhalts auf ein Gerät abfragt, das die Initiative für sichere digitale Medien (SDMI) nicht unterstützt. |
| g \_ wszWMDRM \_ LicenseState \_ CopyToSDMIDevice     | Fügen Sie ein, um die Details zum Recht zum Kopieren des Inhalts auf ein Gerät, das die SDMI unterstützt, abfragt.                                           |
| g \_ wszWMDRM \_ LicenseState \_ CreateThumbnailImage | Fügen Sie ein, um die Details zum Recht zum Erstellen eines Miniaturbilds aus dem Inhalt abfragt.                                                     |
| g \_ wszWMDRM \_ LicenseState \_ Playback             | Fügen Sie ein, um die Details zum Recht zum Wiederspielen des Inhalts abfragt.                                                                              |
| g \_ wszWMDRM \_ LicenseState \_ PlaylistPlayList         | Schließen Sie ein, um die Details zum Recht zum Kopieren des Inhalts auf cd als Teil einer Wiedergabeliste abfragt.                                                  |



 

</dd> <dt>

*rgResultStateData \[ \]* \[out\]
</dt> <dd>

Array von einer oder mehr [**DRM \_ LICENSE STATE \_ \_ DATA-Strukturen,**](drmdrm-license-state-data.md) die die Lizenzstatusinformationen erhalten, die für die rechte im entsprechenden Element des *rgbstrActionsToQuery-Parameters* gelten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Hinweise

Alle Lizenzen, die für die angegebene Schlüssel-ID gelten, werden durchsucht und ausgewertet. Die Ergebnisse werden aggregiert, sodass jede **DRM \_ LICENSE STATE \_ \_ DATA-Struktur** Informationen aus mehreren Lizenzen enthalten kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMDRMLicenseQuery-Schnittstelle**](iwmdrmlicensequery.md)
</dt> </dl>

 

 





