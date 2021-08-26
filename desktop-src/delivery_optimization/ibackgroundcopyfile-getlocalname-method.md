---
title: IBackgroundCopyFile GetLocalName-Methode (Deliveryoptimization.h)
description: Ruft den lokalen Namen der Datei ab.
ms.assetid: 9AA57EB7-5C29-4E5E-972B-DD34B130E6E4
keywords:
- GetLocalName-Methode
- GetLocalName-Methode, IBackgroundCopyFile-Schnittstelle
- IBackgroundCopyFile-Schnittstelle, GetLocalName-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyFile.GetLocalName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0d8c3f3e6a722c7d98fffd5904b398a9573b7a809225e35ae89b5910eb965f5e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953600"
---
# <a name="ibackgroundcopyfilegetlocalname-method"></a>IBackgroundCopyFile::GetLocalName-Methode

Ruft den lokalen Namen der Datei ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetLocalName(
  [out] LPWSTR *ppName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppName* \[ out\]
</dt> <dd>

Auf NULL beendete Zeichenfolge, die den Namen der Datei auf dem Client enthält. Der Name ist vollqualifiziert. Rufen Sie die [**CoTaskMemFree-Funktion**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) auf, um *ppName frei* zu geben, wenn Sie fertig sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt **S_OK** bei Erfolg oder einen der STANDARDMÄßIGEN COM **HRESULT-Werte** bei einem Fehler zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, version 1709 desktop apps only (Nur \[ Desktop-Apps der Version 1709)\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile ist als 01B7BD23-FB88-4A77-8490-5891D3E4653A definiert.<br/>              |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)
</dt> <dt>

[**IBackgroundCopyFile::GetRemoteName**](ibackgroundcopyfile-getremotename-method.md)
</dt> </dl>

 

