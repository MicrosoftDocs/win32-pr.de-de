---
title: Ibackgroundcopyfile getLocalName-Methode (deliveryoptimization. h)
description: Ruft den lokalen Namen der Datei ab.
ms.assetid: 9AA57EB7-5C29-4E5E-972B-DD34B130E6E4
keywords:
- GetLocalName-Methode
- GetLocalName-Methode, ibackgroundcopyfile-Schnittstelle
- Ibackgroundcopyfile-Schnittstelle, getLocalName-Methode
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
ms.openlocfilehash: e1c3a957e64701242d9c698a014ec2ab4028cd85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040523"
---
# <a name="ibackgroundcopyfilegetlocalname-method"></a>Ibackgroundcopyfile:: getLocalName-Methode

Ruft den lokalen Namen der Datei ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetLocalName(
  [out] LPWSTR *ppName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppName* \[ vorgenommen\]
</dt> <dd>

Eine auf NULL endenden Zeichenfolge, die den Namen der Datei auf dem Client enthält. Der Name ist voll qualifiziert. Wenn Sie die Funktion " [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) " aufrufen, wird " *ppName* " freigegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt **S_OK** bei Erfolg oder einen der standardmäßigen com **HRESULT** -Werte bei einem Fehler zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Deliveryoptimization. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile ist als 01b7bd23-B88-4a77-8490-5891d3e4653a definiert.<br/>              |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ibackgroundcopyfile**](ibackgroundcopyfile.md)
</dt> <dt>

[**Ibackgroundcopyfile:: getremutename**](ibackgroundcopyfile-getremotename-method.md)
</dt> </dl>

 

