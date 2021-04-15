---
title: IBackgroundCopyFile2-Methode "Setup-Servername" ("deliveryoptimization. h")
description: Ändert den Remote Namen in einen neuen URL in einem Download Auftrag.
ms.assetid: 344D4193-C96E-4B94-AA53-F9307FEB2565
keywords:
- Methode "Setup Name"
- Methode "Setup-webtename", IBackgroundCopyFile2-Schnittstelle
- IBackgroundCopyFile2 Interface, Methode "Setup Name"
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
ms.openlocfilehash: 4afb5448144867c799bd401bc2d7c180d3958f2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476365"
---
# <a name="ibackgroundcopyfile2setremotename-method"></a>IBackgroundCopyFile2:: Setup-Methode

Ändert den Remote Namen in einen neuen URL in einem Download Auftrag.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetRemoteName(
  [in] LPCWSTR RemoteName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Remotename* \[ in\]
</dt> <dd>

Eine auf NULL endenden Zeichenfolge, die den Namen der Datei auf dem Server enthält. Weitere Informationen zum Angeben des Remote namens finden Sie unter dem **Remotename** -Member.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt sowohl die folgenden Rückgabewerte als auch andere zurück.



| Rückgabecode                                                                                  | Beschreibung                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>     | Erfolg<br/>                                                                                                    |
| <dl> <dt>**E_INVALIDARG**</dt> </dl> | Der neue Remote Name ist eine ungültige URL, oder die neue URL ist zu lang (die URL darf 2.200 Zeichen nicht überschreiten).<br/> |



 

## <a name="remarks"></a>Bemerkungen

In der Regel wird diese Methode aufgerufen, wenn Sie die URL ändern möchten, die zum Übertragen der Datei verwendet wird, oder wenn Sie den Dateinamen oder den Pfad ändern möchten.

Diese Methode wird bei der Rückgabe nicht serialisiert. Zum Serialisieren der Änderung unter [**brechen**](ibackgroundcopyjob-suspend.md) Sie den Auftrag, indem Sie diese Methode (wenn Sie mehrere Dateien im Auftrag ändern, [**eine-Schleife**](ibackgroundcopyjob-resume.md) verwenden) und den Auftrag fortsetzen. Durch Aufrufen der Methode **ibackgroundcopyjob:: Resume** wird die Änderung serialisiert.

Wenn sich der Zeitstempel oder die Dateigröße des neuen Remote namens vom vorherigen Remote Namen unterscheidet oder der neue Server die Prüf Punkt Fortsetzung (bei http-Remote Namen) nicht unterstützt, wird der Download neu gestartet. Andernfalls wird die Übertragung von der gleichen Position auf dem neuen Server fortgesetzt. Führt keine Neustarts bereits übertragener Dateien aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Deliveryoptimization. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile2 ist als 83e81b93-0873-474d-8a8c-f 2018b1a939c definiert.<br/>             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IBackgroundCopyFile2**](ibackgroundcopyfile2.md)
</dt> </dl>

 

 





