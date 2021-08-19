---
title: IBackgroundCopyError GetFile-Methode (Deliveryoptimization.h)
description: Ruft einen Schnittstellenzeiger auf das Dateiobjekt ab, das dem Fehler zugeordnet ist.
ms.assetid: 7E1DB3EE-0690-4D0E-BA98-70F5FBDCF12F
keywords:
- GetFile-Methode
- GetFile-Methode, IBackgroundCopyError-Schnittstelle
- IBackgroundCopyError-Schnittstelle, GetFile-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyError.GetFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fbed5497bcebb3518c7f6a56646976cc01fbfebc501af4a08e861139311f4bc1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096710"
---
# <a name="ibackgroundcopyerrorgetfile-method"></a>IBackgroundCopyError::GetFile-Methode

Ruft einen Schnittstellenzeiger auf das Dateiobjekt ab, das dem Fehler zugeordnet ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetFile(
  [out] IBackgroundCopyFile **ppFile
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppFile* \[ out\]
</dt> <dd>

Ein [**IBackgroundCopyFile-Schnittstellenzeiger,**](ibackgroundcopyfile.md) dessen Methoden Sie verwenden, um die lokalen und Remotedateinamen zu bestimmen, die dem Fehler zugeordnet sind. Der *ppFile-Parameter* wird auf **NULL festgelegt,** wenn der Fehler nicht der lokalen Datei oder Remotedatei zugeordnet ist. Wenn Sie fertig sind, geben Sie *ppFile frei.*

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt die folgenden **HRESULT-Werte** zurück.



| Rückgabecode                                                                                                | Beschreibung                                                                                                    |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK S_OK</dt> </dl>                   | Ein Schnittstellenzeiger auf das Dateiobjekt wurde erfolgreich abgerufen.<br/>                                     |
| <dl> <dt>**DO_E_FILE_NOT_AVAILABLE**</dt> </dl> | Der Fehler ist nicht mit einer lokalen Datei oder Remotedatei verknüpft. Der *ppFile-Parameter* ist auf **NULL festgelegt.**<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, version 1709 desktop apps only (Nur Desktop-Apps der Version 1709) \[\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyError ist als 19C613A0-FCB8-4F28-81AE-897C3D078F81 definiert.<br/>             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IBackgroundCopyError**](ibackgroundcopyerror.md)
</dt> <dt>

[**IBackgroundCopyError::GetError**](ibackgroundcopyerror-geterror-method.md)
</dt> </dl>

 

 





