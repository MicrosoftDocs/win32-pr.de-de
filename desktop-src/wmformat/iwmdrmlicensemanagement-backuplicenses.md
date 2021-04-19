---
title: Methode "iwmdrmlicentmanagement" backuplicenses (wmdrmsdk. h)
description: Die backuplicenses-Methode erstellt eine Sicherung der Lizenzen im lokalen Lizenz Speicher.
ms.assetid: f265254d-b240-4a9f-9c67-de9c92e8a14d
keywords:
- Backuplicenses-Methode (Windows Media-Format)
- Backuplicenses-Methode Windows Media-Format, iwmdrmlicensmanagement-Schnittstelle
- Iwmdrmlicenabmanagement Interface Windows Media-Format, backuplicenses-Methode
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
ms.openlocfilehash: 61c7f676b532353c839a428571f6d28540851bee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360405"
---
# <a name="iwmdrmlicensemanagementbackuplicenses-method"></a>Iwmdrmlicensmanagement:: backuplicenses-Methode

Die **backuplicenses** -Methode erstellt eine Sicherung der Lizenzen im lokalen Lizenz Speicher.

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

*bstraubackupdirectory* \[ in\]
</dt> <dd>

Der UNC-Pfad des Speicher Orts, an dem die Lizenzen gesichert werden.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Flags, die die zu verwendenden Sicherungs Optionen angeben. Das einzige Flag, das derzeit unterstützt wird, ist die WMDRM- \_ Sicherung \_ überschreiben, bei der die Methode zum Überschreiben vorhandener Sicherungsdateien im Verzeichnis konfiguriert wird.

</dd> <dt>

*ppunkcancelationcookie* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger, der einen Zeiger auf die **IUnknown** -Schnittstelle eines Objekts empfängt, das diesen asynchronen-Befehl identifiziert. Dieser Schnittstellen Zeiger kann zum Abbrechen des asynchronen Aufrufs verwendet werden, indem die [**iwmdrmeventgenerator:: cancelasyncoperation**](iwmdrmeventgenerator-cancelasyncoperation.md) -Methode aufgerufen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode wird asynchron ausgeführt. Sie wird unmittelbar nach dem Aufruf von zurückgegeben und generiert dann eine Reihe von **mewmdrmlicencbackupprogress** -Ereignissen, gefolgt von einem **mewmdrmlicenabcomplete** -Ereignis, wenn die Verarbeitung abgeschlossen ist. Der Wert jedes **mewmdrmlicencbackupprogress** -Ereignisses, das durch Aufrufen von **imfmediaevent:: GetValue** abgerufen wird, ist ein **IUnknown** -Zeiger. Sie können die **QueryInterface** -Methode der abgerufenen **IUnknown** -Schnittstelle zum Abrufen einer Instanz der [**iwmdrmlicenanbackuprestorestatus**](iwmdrmlicensebackuprestorestatus.md) -Schnittstelle abrufen.

Weitere Informationen zur Verwendung der asynchronen Methoden der erweiterten APIs für den Windows Media DRM-Client finden [Sie unter Verwenden des Media Foundation-Ereignis Modells](using-the-media-foundation-model.md).

Nicht alle Lizenzen dürfen gesichert werden. Diese Methode sichert nur Lizenzen, die dies zulassen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmdrmlicenabmanagement-Schnittstelle**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





