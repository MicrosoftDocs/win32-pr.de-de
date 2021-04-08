---
title: Ibackgroundcopyjob GetDisplayName-Methode (deliveryoptimization. h)
description: Ruft den anzeigen Amen für den Auftrag ab. In der Regel verwenden Sie den anzeigen Amen, um den Auftrag auf einer Benutzeroberfläche zu identifizieren.
ms.assetid: E3D906E1-5D58-4BA8-A3AB-24BCDCD487F5
keywords:
- GetDisplayName-Methode
- GetDisplayName-Methode, ibackgroundcopyjob-Schnittstelle
- Ibackgroundcopyjob-Schnittstelle, GetDisplayName-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetDisplayName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 981e4b60ea3c25d48a3b098237232e517e4ed1c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956948"
---
# <a name="ibackgroundcopyjobgetdisplayname-method"></a>Ibackgroundcopyjob:: GetDisplayName-Methode

Ruft den anzeigen Amen für den Auftrag ab. In der Regel verwenden Sie den anzeigen Amen, um den Auftrag auf einer Benutzeroberfläche zu identifizieren.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDisplayName(
  [out] LPWSTR *ppDisplayName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppdisplayname* \[ vorgenommen\]
</dt> <dd>

Eine auf NULL endenden Zeichenfolge, die den anzeigen Amen enthält, der den Auftrag identifiziert. Mehrere Aufträge können denselben anzeigen Amen aufweisen. Aufrufen der Funktion " [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) ", um " *ppdisplayname* " zu beenden

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt sowohl die folgenden **HRESULT** -Werte als auch andere zurück.



| Rückgabecode                                                                                  | Beschreibung                                                  |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>     | Der Anzeige Name wurde erfolgreich abgerufen.<br/>          |
| <dl> <dt>**E_INVALIDARG**</dt> </dl> | Der *ppdisplayname* -Parameter darf nicht **null** sein.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Deliveryoptimization. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob ist als 37668d37-507E-4160-9316-26306d150b12 definiert.<br/>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> </dl>

 

