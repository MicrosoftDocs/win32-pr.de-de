---
title: Ibackgroundcopyfile getremutename-Methode (deliveryoptimization. h)
description: Ruft den Remote Namen der Datei ab.
ms.assetid: 518857E0-C16A-400B-8F3D-5264B3CB43FF
keywords:
- Getremutename-Methode
- Getremutename-Methode, ibackgroundcopyfile-Schnittstelle
- Ibackgroundcopyfile-Schnittstelle, getremutename-Methode
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
ms.openlocfilehash: 9984ed9971fdfb91279dabc5810490b62804b7e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040521"
---
# <a name="ibackgroundcopyfilegetremotename-method"></a>Ibackgroundcopyfile:: getremutename-Methode

Ruft den Remote Namen der Datei ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetRemoteName(
  [out] LPWSTR *ppName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppName* \[ vorgenommen\]
</dt> <dd>

Eine auf NULL endenden Zeichenfolge, die den Remote Namen der zu übertragenden Datei enthält. Der Name ist voll qualifiziert. Wenn Sie die Funktion " [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) " aufrufen, wird " *ppName* " freigegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt **S_OK** bei Erfolg oder einen der standardmäßigen com **HRESULT** -Werte bei einem Fehler zurück.

## <a name="remarks"></a>Bemerkungen

Um den Remote Dateinamen zu ändern, nennen Sie die [**IBackgroundCopyFile2::**](ibackgroundcopyfile2-setremotename-method.md) Setup-Methode.

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

[**Ibackgroundcopyfile:: getLocalName**](ibackgroundcopyfile-getlocalname-method.md)
</dt> </dl>

 

