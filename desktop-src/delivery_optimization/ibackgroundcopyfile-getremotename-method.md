---
title: IBackgroundCopyFile GetRemoteName-Methode (Deliveryoptimization.h)
description: Ruft den Remotenamen der Datei ab.
ms.assetid: 518857E0-C16A-400B-8F3D-5264B3CB43FF
keywords:
- GetRemoteName-Methode
- GetRemoteName-Methode, IBackgroundCopyFile-Schnittstelle
- IBackgroundCopyFile-Schnittstelle, GetRemoteName-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyFile.GetRemoteName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e84827f4c1144c4242f382aff822984b24dd83610c1ebd5d2540ba7c4ca65d2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118810332"
---
# <a name="ibackgroundcopyfilegetremotename-method"></a>IBackgroundCopyFile::GetRemoteName-Methode

Ruft den Remotenamen der Datei ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetRemoteName(
  [out] LPWSTR *ppName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppName* \[ out\]
</dt> <dd>

Auf NULL endende Zeichenfolge, die den Remotenamen der zu übertragenden Datei enthält. Der Name ist vollqualifiziert. Rufen Sie die [**CoTaskMemFree-Funktion**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) auf, um *ppName* frei zu machen, wenn Sie fertig sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt **S_OK** bei Erfolg oder einen der COM **HRESULT-Standardwerte** bei Einem Fehler zurück.

## <a name="remarks"></a>Hinweise

Um den Remotedateinamen zu ändern, rufen Sie die [**IBackgroundCopyFile2::SetRemoteName-Methode**](ibackgroundcopyfile2-setremotename-method.md) auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, nur Desktop-Apps der Version 1709 \[\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, nur Desktop-Apps der Version 1709 \[\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile ist als 01B7BD23-FB88-4A77-8490-5891D3E4653A definiert.<br/>              |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)
</dt> <dt>

[**IBackgroundCopyFile::GetLocalName**](ibackgroundcopyfile-getlocalname-method.md)
</dt> </dl>

 

