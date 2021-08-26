---
title: IWMDRMLicenseManagement ProcessLicenseRevocationResponse-Methode (Wmdrmsdk.h)
description: Die ProcessLicenseRevocationResponse-Methode widerruft Lizenzen aus dem lokalen Lizenzspeicher. Diese Methode verwendet ein Lizenzsperrblob (LRB), das von einem Lizenzsperrserver empfangen wurde, um die zu widerrufenden Lizenzen zu identifizieren.
ms.assetid: 4428ac44-c3f4-404e-9997-cbc7360faedf
keywords:
- ProcessLicenseRevocationResponse-Methode windows Media Format
- ProcessLicenseRevocationResponse-Methode windows Media Format , IWMDRMLicenseManagement-Schnittstelle
- IWMDRMLicenseManagement-Schnittstelle windows Media Format , ProcessLicenseRevocationResponse-Methode
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
ms.openlocfilehash: d58c33f79db575dec37d7d2ac51e3c65b10416b9ca35a50084f36a56693854be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930310"
---
# <a name="iwmdrmlicensemanagementprocesslicenserevocationresponse-method"></a>IWMDRMLicenseManagement::P rocessLicenseRevocationResponse-Methode

Die **ProcessLicenseRevocationResponse-Methode** widerruft Lizenzen aus dem lokalen Lizenzspeicher. Diese Methode verwendet ein Lizenzsperrblob (LRB), das von einem Lizenzsperrserver empfangen wurde, um die zu widerrufenden Lizenzen zu identifizieren.

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

*pbSignedLRB* \[ In\]
</dt> <dd>

Lizenzsperrblob (License Revocation Blob, LRB), das vom Lizenzsperrserver als Reaktion auf eine Herausforderung empfangen wurde, die durch Aufrufen der [**CreateLicenseRevocationCantenge-Methode generiert**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) wurde.

</dd> <dt>

*cbSignedLRB* \[ In\]
</dt> <dd>

Größe des LRB in Bytes.

</dd> <dt>

*ppbSignedACK* \[ out\]
</dt> <dd>

Adresse eines Zeigers, der die Adresse der Lizenzsperrbestätigung empfängt. Die Bestätigung sollte an den Lizenzsperrdienst gesendet werden. Wenn Sie mit diesen Daten fertig sind, müssen Sie den Arbeitsspeicher durch Aufrufen von **CoTaskMemFree frei geben.**

</dd> <dt>

*–signedACK* \[ out\]
</dt> <dd>

Adresse einer Variablen, die die Größe der Bestätigung in Bytes empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Keine.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMDRMLicenseManagement-Schnittstelle**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





