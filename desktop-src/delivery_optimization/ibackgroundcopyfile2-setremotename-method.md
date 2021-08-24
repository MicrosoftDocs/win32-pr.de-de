---
title: IBackgroundCopyFile2 SetRemoteName-Methode (Deliveryoptimization.h)
description: Ändert den Remotenamen in eine neue URL in einem Downloadauftrag.
ms.assetid: 344D4193-C96E-4B94-AA53-F9307FEB2565
keywords:
- SetRemoteName-Methode
- SetRemoteName-Methode, IBackgroundCopyFile2-Schnittstelle
- IBackgroundCopyFile2-Schnittstelle, SetRemoteName-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyFile2.SetRemoteName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e4a2ed93a264aa12d61291c3562a455a026e0dfd0d727648b7d13f6ffe360015
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636020"
---
# <a name="ibackgroundcopyfile2setremotename-method"></a>IBackgroundCopyFile2::SetRemoteName-Methode

Ändert den Remotenamen in eine neue URL in einem Downloadauftrag.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetRemoteName(
  [in] LPCWSTR RemoteName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*RemoteName* \[ In\]
</dt> <dd>

Auf NULL beendete Zeichenfolge, die den Namen der Datei auf dem Server enthält. Informationen zum Angeben des Remotenamens finden Sie unter **RemoteName-Member.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt die folgenden Rückgabewerte sowie andere zurück.



| Rückgabecode                                                                                  | Beschreibung                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK S_OK</dt> </dl>     | Erfolg<br/>                                                                                                    |
| <dl> <dt>**E_INVALIDARG**</dt> </dl> | Der neue Remotename ist eine ungültige URL, oder die neue URL ist zu lang (die URL darf 2.200 Zeichen nicht überschreiten).<br/> |



 

## <a name="remarks"></a>Hinweise

In der Regel rufen Sie diese Methode auf, wenn Sie die URL ändern möchten, die zum Übertragen der Datei verwendet wird, oder wenn Sie den Dateinamen oder Pfad ändern möchten.

Diese Methode serialisiert nicht, wenn sie zurückgegeben wird. Um die Änderung [](ibackgroundcopyjob-suspend.md) zu serialisieren, setzen Sie den Auftrag an, rufen Sie diese Methode auf (wenn Sie mehrere Dateien im Auftrag ändern, verwenden Sie eine Schleife), [**und**](ibackgroundcopyjob-resume.md) setzen Sie den Auftrag wieder auf. Durch Aufrufen **der IBackgroundCopyJob::Resume-Methode** wird die Änderung serialisiert.

Wenn sich der Zeitstempel oder die Dateigröße des neuen Remotenamens vom vorherigen Remotenamen unterscheiden oder der neue Server die Wiederaufnahme des Prüfpunkts (für HTTP-Remotenamen) nicht unterstützt, startet DO den Download neu. Andernfalls wird die Übertragung von derselben Position auf dem neuen Server fortgesetzt. DO startet bereits übertragene Dateien nicht neu.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile2 ist als 83e81b93-0873-474d-8a8c-f2018b1a939c definiert.<br/>             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IBackgroundCopyFile2**](ibackgroundcopyfile2.md)
</dt> </dl>

 

 





