---
title: Iwmdrmlicenabmanagement processlicenserevocationresponse-Methode (wmdrmsdk. h)
description: Mit der processlicenserevocationresponse-Methode werden Lizenzen aus dem lokalen Lizenz Speicher widerrufen. Bei dieser Methode wird ein von einem Lizenz Sperr Server empfangener Lizenzierungs-BLOB (License Lock BLOB, LRB) verwendet, um die zu widerrufenden
ms.assetid: 4428ac44-c3f4-404e-9997-cbc7360faedf
keywords:
- Processlicenserevocationresponse-Methode Windows Media-Format
- Processlicenserevocationresponse-Methode, Windows Media-Format, iwmdrmlicenermanagement-Schnittstelle
- Iwmdrmlicenabmanagement Interface Windows Media-Format, processlicenserevocationresponse-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.ProcessLicenseRevocationResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 534ead406107957971bbf1501dff2850478fae08
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372558"
---
# <a name="iwmdrmlicensemanagementprocesslicenserevocationresponse-method"></a>Iwmdrmlicensmanagement::P rocess licenserevocationresponse-Methode

Mit der **processlicenserevocationresponse** -Methode werden Lizenzen aus dem lokalen Lizenz Speicher widerrufen. Bei dieser Methode wird ein von einem Lizenz Sperr Server empfangener Lizenzierungs-BLOB (License Lock BLOB, LRB) verwendet, um die zu widerrufenden

## <a name="syntax"></a>Syntax


```C++
HRESULT ProcessLicenseRevocationResponse(
  [in]  BYTE  *pbSignedLRB,
  [in]  DWORD cbSignedLRB,
  [out] BYTE  **ppbSignedACK,
  [out] DWORD *pcbSignedACK
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbsignetdlrb* \[ in\]
</dt> <dd>

Vom Lizenz Sperr Server empfangener Lizenz Sperr-BLOB (LRB) als Antwort auf eine Aufforderung, die durch Aufrufen der [**createlicenserevocationchallenge**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) -Methode generiert wurde.

</dd> <dt>

*cbsignetdlrb* \[ in\]
</dt> <dd>

Die LRB-Größe in Bytes.

</dd> <dt>

*ppbsignedack* \[ vorgenommen\]
</dt> <dd>

Adresse eines Zeigers, der die Adresse der Lizenz Sperr Bestätigung empfängt. Die Bestätigung sollte an den Lizenz Sperr Dienst gesendet werden. Wenn Sie mit diesen Daten fertig sind, müssen Sie den Arbeitsspeicher freigeben, indem Sie " **CoTaskMemFree**" aufrufen.

</dd> <dt>

*pcbsignedack* \[ vorgenommen\]
</dt> <dd>

Adresse einer Variablen, die die Größe der Bestätigung in Bytes empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmdrmlicenabmanagement-Schnittstelle**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





