---
title: IWMDRMLicenseManagement CleanLicenseStore-Methode (Wmdrmsdk.h)
description: Die CleanLicenseStore-Methode entfernt nicht verwendbare Lizenzen aus dem temporären Lizenzspeicher und defragmentiert den lokalen Lizenzspeicher, um die Leistung zu verbessern.
ms.assetid: 07ddd6f8-a091-4c18-81d3-c4d0c6026b6b
keywords:
- 'CleanLicenseStore-Methode : Windows-Medienformat'
- CleanLicenseStore-Methode windows Media Format, IWMDRMLicenseManagement-Schnittstelle
- IWMDRMLicenseManagement-Schnittstelle windows Media Format , CleanLicenseStore-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.CleanLicenseStore
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6010313efaca6855c403f9ee698284ff4aebb2e0ab8a5e08e5862a5890224a1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846952"
---
# <a name="iwmdrmlicensemanagementcleanlicensestore-method"></a>IWMDRMLicenseManagement::CleanLicenseStore-Methode

Die **CleanLicenseStore-Methode** entfernt nicht verwendbare Lizenzen aus dem temporären Lizenzspeicher und defragmentiert den lokalen Lizenzspeicher, um die Leistung zu verbessern.

## <a name="syntax"></a>Syntax


```C++
HRESULT CleanLicenseStore(
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Flags, die die zu verwendenden Bereinigungsoptionen für den Lizenzspeicher angeben. Legen Sie auf eine der Konstanten in der folgenden Tabelle fest.



| Konstante                            | Beschreibung                                                                                                                                                                    |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMDRM \_ CLEAN \_ LICENSE \_ STORE \_ SYNC  | Der Bereinigungsvorgang wird synchron ausgeführt. Diese Methode gibt erst dann zurück, wenn der Vorgang abgeschlossen ist.                                                              |
| WMDRM \_ CLEAN \_ LICENSE \_ STORE \_ ASYNC | Der Bereinigungsvorgang wird asynchron ausgeführt. Diese Methode gibt sofort zurück. Wenn der Vorgang abgeschlossen ist, wird das Medienereignis MELicenseStoreCleaned gesendet. |



 

</dd> <dt>

*ppunkCancelationCookie* \[ out\]
</dt> <dd>

Zeiger, der einen Zeiger auf die **IUnknown-Schnittstelle** eines Objekts empfängt, das diesen asynchronen Aufruf identifiziert. Dieser Schnittstellenzeiger kann verwendet werden, um den asynchronen Aufruf abzubricht, indem die [**IWMDRMEventGenerator::CancelAsyncOperation-Methode aufgerufen**](iwmdrmeventgenerator-cancelasyncoperation.md) wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                            | Beschreibung                                                            |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Die Methode wurde erfolgreich ausgeführt.<br/>                                       |
| <dl> <dt>**DRM \_ E \_ LICENSENOTFOUND**</dt> </dl> | Auf dem Clientcomputer ist kein temporärer Lizenzspeicher verfügbar.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode wird asynchron ausgeführt. Er wird unmittelbar nach dem Aufgerufenen zurückgegeben und generiert dann ein **MEWMDRMLicenseStoreCleaned-Ereignis,** wenn die Verarbeitung abgeschlossen ist.

Weitere Informationen zur Verwendung der asynchronen Methoden der erweiterten APIs des Windows Media DRM-Clients finden Sie unter [Verwenden des Media Foundation-Ereignismodells.](using-the-media-foundation-model.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMDRMLicenseManagement-Schnittstelle**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





