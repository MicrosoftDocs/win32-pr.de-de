---
title: Iwmdrmlicenabmanagement restorelicenses-Methode (wmdrmsdk. h)
description: Die restorelicenses-Methode stellt Lizenzen aus einer Lizenz Sicherung wieder her, die durch Aufrufen der backuplicenses-Methode erstellt wurde.
ms.assetid: 83e4b748-0f69-4a9e-b531-047c9a2be1fe
keywords:
- Restorelicenses-Methode Windows Media-Format
- Restorelicenses-Methode, Windows Media-Format, iwmdrmlicenermanagement-Schnittstelle
- Iwmdrmlicenabmanagement Interface Windows Media-Format, restorelicenses-Methode
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
ms.openlocfilehash: fb07f3989ff19faa723e4b1d1cd50dc4e269f219
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370060"
---
# <a name="iwmdrmlicensemanagementrestorelicenses-method"></a>Iwmdrmlicenabmanagement:: restorelicenses-Methode

Die **restorelicenses** -Methode stellt Lizenzen aus einer Lizenz Sicherung wieder her, die durch Aufrufen der [**backuplicenses**](iwmdrmlicensemanagement-backuplicenses.md) -Methode erstellt wurde.

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

*bstraubackupdirectory* \[ in\]
</dt> <dd>

Der UNC-Pfad des Speicher Orts, von dem die Lizenzen wieder hergestellt werden.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Flags, die die zu verwendenden Wiederherstellungsoptionen angeben. Das einzige Flag, das derzeit unterstützt wird, ist WMDRM \_ Restore \_ Individual, das die Methode konfiguriert, um bei Bedarf eine Individualisierung im Rahmen der Wiederherstellung auszuführen.

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

Diese Methode wird asynchron ausgeführt. Sie wird unmittelbar nach dem Aufruf von zurückgegeben und generiert dann eine Reihe von **mewmdrmlicenserestoreprogress** -Ereignissen, gefolgt von einem **mewmdrmlicenserestorecomplete** -Ereignis, wenn die Verarbeitung abgeschlossen ist. Der Wert jedes **mewmdrmlicenserestoreprogress** -Ereignisses, das durch Aufrufen von **imfmediaevent:: GetValue** abgerufen wird, ist ein **IUnknown** -Zeiger. Sie können die **QueryInterface** -Methode der abgerufenen **IUnknown** -Schnittstelle zum Abrufen einer Instanz der [**iwmdrmlicenanbackuprestorestatus**](iwmdrmlicensebackuprestorestatus.md) -Schnittstelle abrufen.

Weitere Informationen zur Verwendung der asynchronen Methoden der erweiterten APIs für den Windows Media DRM-Client finden [Sie unter Verwenden des Media Foundation-Ereignis Modells](using-the-media-foundation-model.md).

Die Sicherung kann vom lokalen Computer oder von einem anderen Computer erfolgen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmdrmlicenabmanagement-Schnittstelle**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





