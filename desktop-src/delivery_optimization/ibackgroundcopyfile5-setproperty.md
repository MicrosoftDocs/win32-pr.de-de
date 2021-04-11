---
title: IBackgroundCopyFile5 SetProperty-Methode (deliveryoptimization. h)
description: Legt eine generische Eigenschaft einer Übermittlungs Optimierungs Datei-Übertragung (Do) fest.
ms.assetid: 63B6806E-47D6-49B0-9867-628C110540D0
keywords:
- SetProperty-Methode
- SetProperty-Methode, IBackgroundCopyFile5-Schnittstelle
- IBackgroundCopyFile5 Interface, SetProperty-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7f519ee77af0ae6e0c3d1d036aeeb6a8ad712870
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949785"
---
# <a name="ibackgroundcopyfile5setproperty-method"></a>IBackgroundCopyFile5:: SetProperty-Methode

Legt eine generische Eigenschaft einer Übermittlungs Optimierungs Datei-Übertragung (Do) fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetProperty(
  [in]  BITS_FILE_PROPERTY_ID    PropertyId,
  [out] BITS_FILE_PROPERTY_VALUE *ProertyValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PropertyId* \[ in\]
</dt> <dd>

Gibt die festzulegende Eigenschaft an.

</dd> <dt>

*Proertyvalue* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Union, die den festzulegenden Wert angibt. Das für die eigen schafts-ID geeignete Unionmember wird verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Deliveryoptimization. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile5 ist als "85c1657f-DAFC-40e8-8834-df18ea25717e" definiert.<br/>             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IBackgroundCopyFile5**](ibackgroundcopyfile5.md)
</dt> <dt>

[**IBackgroundCopyFile5. GetProperty**](ibackgroundcopyfile5-getproperty.md)
</dt> </dl>

 

 





