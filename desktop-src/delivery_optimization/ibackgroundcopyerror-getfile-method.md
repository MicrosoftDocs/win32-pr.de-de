---
title: Ibackgroundcopyerror GetFile-Methode (deliveryoptimization. h)
description: Ruft einen Schnittstellen Zeiger auf das File-Objekt ab, das dem Fehler zugeordnet ist.
ms.assetid: 7E1DB3EE-0690-4D0E-BA98-70F5FBDCF12F
keywords:
- GetFile-Methode
- GetFile-Methode, ibackgroundcopyerror-Schnittstelle
- Ibackgroundcopyerror-Schnittstelle, GetFile-Methode
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
ms.openlocfilehash: b84396797378c77a6f774b4c63a3966b0d601b7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337735"
---
# <a name="ibackgroundcopyerrorgetfile-method"></a>Ibackgroundcopyerror:: GetFile-Methode

Ruft einen Schnittstellen Zeiger auf das File-Objekt ab, das dem Fehler zugeordnet ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetFile(
  [out] IBackgroundCopyFile **ppFile
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppfile* \[ vorgenommen\]
</dt> <dd>

Ein [**ibackgroundcopyfile**](ibackgroundcopyfile.md) -Schnittstellen Zeiger, dessen Methoden Sie verwenden, um die dem Fehler zugeordneten lokalen und Remote Dateinamen zu bestimmen. Der *ppfile* -Parameter wird auf **null** festgelegt, wenn der Fehler nicht der lokalen Datei oder Remote Datei zugeordnet ist. Wenn Sie den Vorgang abgeschlossen haben, geben Sie *ppfile* frei

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt die folgenden **HRESULT** -Werte zurück.



| Rückgabecode                                                                                                | Beschreibung                                                                                                    |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>                   | Ein Schnittstellen Zeiger auf das Datei Objekt wurde erfolgreich abgerufen.<br/>                                     |
| <dl> <dt>**DO_E_FILE_NOT_AVAILABLE**</dt> </dl> | Der Fehler ist keiner lokalen oder Remote Datei zugeordnet. Der *ppfile* -Parameter ist auf **null** festgelegt.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1709, \[ nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Server, Version 1709, \[ nur Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Deliveryoptimization. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyError ist als 19c613a0-fcb8-4f 28-81ae-897c3d078-Datei definiert.<br/>             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ibackgroundcopyerror**](ibackgroundcopyerror.md)
</dt> <dt>

[**Ibackgroundcopyerror:: getError**](ibackgroundcopyerror-geterror-method.md)
</dt> </dl>

 

 





