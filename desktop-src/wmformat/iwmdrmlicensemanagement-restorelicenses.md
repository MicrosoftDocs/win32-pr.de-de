---
title: IWMDRMLicenseManagement RestoreLicenses-Methode (Wmdrmsdk.h)
description: Die RestoreLicenses-Methode stellt Lizenzen aus einer Lizenzsicherung wieder her, die durch Aufrufen der BackupLicenses-Methode erstellt wurde.
ms.assetid: 83e4b748-0f69-4a9e-b531-047c9a2be1fe
keywords:
- 'RestoreLicenses-Methode : Windows Media Format'
- RestoreLicenses-Methode windows Media Format, IWMDRMLicenseManagement-Schnittstelle
- IWMDRMLicenseManagement-Schnittstelle windows Media Format , RestoreLicenses-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.RestoreLicenses
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2a35fdd33df2387bb59dfac64f554dd8b5953fa3015afec6ca643725b9bd58f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846938"
---
# <a name="iwmdrmlicensemanagementrestorelicenses-method"></a>IWMDRMLicenseManagement::RestoreLicenses-Methode

Die **RestoreLicenses-Methode** stellt Lizenzen aus einer Lizenzsicherung wieder her, die durch Aufrufen der [**BackupLicenses-Methode erstellt**](iwmdrmlicensemanagement-backuplicenses.md) wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT RestoreLicenses(
  [in]  BSTR     bstrBackupDirectory,
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrBackupDirectory* \[ In\]
</dt> <dd>

UNC-Pfad des Speicherorts, von dem die Lizenzen wiederhergestellt werden.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Flags, die die zu verwendenden Wiederherstellungsoptionen angeben. Das einzige derzeit unterstützte Flag ist WMDRM RESTORE INDIVIDUALIZE, das die -Methode so konfiguriert, dass die Individualisierung im Rahmen der Wiederherstellung bei Bedarf \_ \_ durchzuführen ist.

</dd> <dt>

*ppunkCancelationCookie* \[ out\]
</dt> <dd>

Zeiger, der einen Zeiger auf die **IUnknown-Schnittstelle** eines Objekts empfängt, das diesen asynchronen Aufruf identifiziert. Dieser Schnittstellenzeiger kann verwendet werden, um den asynchronen Aufruf abzubricht, indem die [**IWMDRMEventGenerator::CancelAsyncOperation-Methode aufgerufen**](iwmdrmeventgenerator-cancelasyncoperation.md) wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode wird asynchron ausgeführt. Sie wird unmittelbar nach dem Aufgerufenen zurückgegeben und generiert dann eine Reihe von **MEWMDRMLicenseRestoreProgress-Ereignissen** gefolgt von einem **MEWMDRMLicenseRestoreCompleted-Ereignis,** wenn die Verarbeitung abgeschlossen ist. Der Wert der einzelnen **MEWMDRMLicenseRestoreProgress-Ereignisse,** die durch aufrufen von **DURCHSCHMediaEvent::GetValue** erhalten werden, ist ein **IUnknown-Zeiger.** Sie können die **QueryInterface-Methode** der abgerufenen **IUnknown-Schnittstelle** aufrufen, um eine Instanz der [**IWMDRMLicenseBackupRestoreStatus-Schnittstelle**](iwmdrmlicensebackuprestorestatus.md) abzurufen.

Weitere Informationen zur Verwendung der asynchronen Methoden der erweiterten APIs des Windows Media DRM-Clients finden Sie unter [Verwenden des Media Foundation-Ereignismodells.](using-the-media-foundation-model.md)

Die Sicherung kann vom lokalen Computer oder von einem anderen Computer aus erstellt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMDRMLicenseManagement-Schnittstelle**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





