---
title: IWMDRMLicenseManagement BackupLicenses-Methode (Wmdrmsdk.h)
description: Die BackupLicenses-Methode erstellt eine Sicherung der Lizenzen im lokalen Lizenzspeicher.
ms.assetid: f265254d-b240-4a9f-9c67-de9c92e8a14d
keywords:
- BackupLicenses-Methode windows Media Format
- BackupLicenses-Methode windows Media Format , IWMDRMLicenseManagement-Schnittstelle
- IWMDRMLicenseManagement-Schnittstelle Windows Media Format , BackupLicenses-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.BackupLicenses
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3905f8fd464645f7fcd22551360e6a9610913eeea7f191d7e770e24f5ea8cd49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027648"
---
# <a name="iwmdrmlicensemanagementbackuplicenses-method"></a>IWMDRMLicenseManagement::BackupLicenses-Methode

Die **BackupLicenses-Methode** erstellt eine Sicherung der Lizenzen im lokalen Lizenzspeicher.

## <a name="syntax"></a>Syntax


```C++
HRESULT BackupLicenses(
  [in]  BSTR     bstrBackupDirectory,
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrBackupDirectory* \[ In\]
</dt> <dd>

UNC-Pfad des Standorts, an dem die Lizenzen gesichert werden.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Flags, die die zu verwendenden Sicherungsoptionen angeben. Das einzige derzeit unterstützte Flag ist WMDRM \_ BACKUP \_ OVERWRITE, das die -Methode zum Überschreiben vorhandener Sicherungsdateien im Verzeichnis konfiguriert.

</dd> <dt>

*ppunkCancelationCookie* \[ out\]
</dt> <dd>

Zeiger, der einen Zeiger auf die **IUnknown-Schnittstelle** eines Objekts empfängt, das diesen asynchronen Aufruf identifiziert. Dieser Schnittstellenzeiger kann verwendet werden, um den asynchronen Aufruf abzubrechen, indem die [**IWMDRMEventGenerator::CancelAsyncOperation-Methode**](iwmdrmeventgenerator-cancelasyncoperation.md) aufgerufen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode wird asynchron ausgeführt. Sie gibt sofort nach dem Aufruf zurück und generiert dann eine Reihe von **MEWMDRMLicenseBackupProgress-Ereignissen,** gefolgt von einem **MEWMDRMLicenseBackupCompleted-Ereignis,** wenn die Verarbeitung abgeschlossen ist. Der Wert jedes **MEWMDRMLicenseBackupProgress-Ereignisses,** das durch Aufrufen von **"POINTERMediaEvent::GetValue"** abgerufen wird, ist ein **IUnknown-Zeiger.** Sie können die **QueryInterface-Methode** der abgerufenen **IUnknown-Schnittstelle** aufrufen, um eine Instanz der [**IWMDRMLicenseBackupRestoreStatus-Schnittstelle**](iwmdrmlicensebackuprestorestatus.md) abzurufen.

Weitere Informationen zur Verwendung der asynchronen Methoden der erweiterten APIs des Windows Media DRM-Clients finden Sie unter [Verwenden des Media Foundation Ereignismodells.](using-the-media-foundation-model.md)

Nicht alle Lizenzen dürfen gesichert werden. Mit dieser Methode werden nur Lizenzen gesichert, die dies zulassen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMDRMLicenseManagement-Schnittstelle**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





