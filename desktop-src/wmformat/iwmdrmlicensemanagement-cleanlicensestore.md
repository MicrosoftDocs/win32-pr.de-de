---
title: Iwmdrmlicenabmanagement cleanlicensstore-Methode (wmdrmsdk. h)
description: Die cleanlicenserstore-Methode entfernt nicht verwendbare Lizenzen aus dem temporären Lizenz Speicher und defragmentiert den lokalen Lizenz Speicher, um die Leistung zu verbessern.
ms.assetid: 07ddd6f8-a091-4c18-81d3-c4d0c6026b6b
keywords:
- Cleanlicenerstore-Methode Windows Media-Format
- Cleanlicenerstore-Methode Windows Media-Format, iwmdrmlicenermanagement-Schnittstelle
- Iwmdrmlicenabmanagement Interface Windows Media-Format, cleanlicenerstore-Methode
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
ms.openlocfilehash: b9327fd836cf742f5495c29767be93d914c0f187
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351213"
---
# <a name="iwmdrmlicensemanagementcleanlicensestore-method"></a>Iwmdrmlicenabmanagement:: cleanlicensstore-Methode

Die **cleanlicenserstore** -Methode entfernt nicht verwendbare Lizenzen aus dem temporären Lizenz Speicher und defragmentiert den lokalen Lizenz Speicher, um die Leistung zu verbessern.

## <a name="syntax"></a>Syntax


```C++
HRESULT CleanLicenseStore(
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Flags, die die zu verwendenden Reinigungs Optionen für den Lizenz Speicher angeben. Legen Sie auf eine der Konstanten in der folgenden Tabelle fest.



| Konstante                            | BESCHREIBUNG                                                                                                                                                                    |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Synchronisierung des WMDRM- \_ \_ Lizenz \_ Speicher bereinigen \_  | Der Clean-Vorgang wird synchron ausgeführt. Diese Methode wird erst zurückgegeben, wenn der Vorgang beendet ist.                                                              |
| WMDRM- \_ Clean \_ License \_ Store \_ Async | Der Clean-Vorgang wird asynchron ausgeführt. Diese Methode wird sofort zurückgegeben. Wenn der Vorgang beendet ist, wird das Medienereignis "melicensetup" gesendet. |



 

</dd> <dt>

*ppunkcancelationcookie* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger, der einen Zeiger auf die **IUnknown** -Schnittstelle eines Objekts empfängt, das diesen asynchronen-Befehl identifiziert. Dieser Schnittstellen Zeiger kann zum Abbrechen des asynchronen Aufrufs verwendet werden, indem die [**iwmdrmeventgenerator:: cancelasyncoperation**](iwmdrmeventgenerator-cancelasyncoperation.md) -Methode aufgerufen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                            | Beschreibung                                                            |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Die Methode wurde erfolgreich ausgeführt.<br/>                                       |
| <dl> <dt>**DRM- \_ E \_ licensenotfound**</dt> </dl> | Auf dem Client Computer ist kein temporärer Lizenz Speicher vorhanden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode wird asynchron ausgeführt. Sie wird sofort nach dem Aufruf von zurückgegeben und generiert dann ein **mewmdrmlicenabgelig-Ereignis** , wenn die Verarbeitung fertiggestellt ist.

Weitere Informationen zur Verwendung der asynchronen Methoden der erweiterten APIs für den Windows Media DRM-Client finden [Sie unter Verwenden des Media Foundation-Ereignis Modells](using-the-media-foundation-model.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmdrmlicenabmanagement-Schnittstelle**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





