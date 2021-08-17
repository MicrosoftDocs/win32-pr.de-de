---
title: IWMDRMSecurity GetMachineCertificate-Methode (Wmdrmsdk.h)
description: Die GetMachineCertificate-Methode ruft das Computerzertifikat des DRM-Subsystems auf dem Clientcomputer ab.
ms.assetid: 38b8e812-e997-4a63-b906-ebd26a5556be
keywords:
- GetMachineCertificate-Methode windows Media Format
- GetMachineCertificate-Methode windows Media Format , IWMDRMSecurity-Schnittstelle
- IWMDRMSecurity-Schnittstelle windows Media Format , GetMachineCertificate-Methode
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetMachineCertificate
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fd85a3b74ee28e5faa8df5fc264d50366803f4073ec97a36920577d417e4f97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084697"
---
# <a name="iwmdrmsecuritygetmachinecertificate-method"></a>IWMDRMSecurity::GetMachineCertificate-Methode

Die **GetMachineCertificate-Methode** ruft das Computerzertifikat des DRM-Subsystems auf dem Clientcomputer ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetMachineCertificate(
  [in]      DWORD dwCertificateType,
  [out]     BYTE  rgbVersion[4],
  [out]     BYTE  **ppbCertificate,
  [in, out] DWORD *pcbCertificate
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwCertificateType* \[ In\]
</dt> <dd>

Typ des abzurufende Zertifikats. Legen Sie auf einen der Werte in der folgenden Tabelle fest.



| Wert                        | Beschreibung                                                                           |
|------------------------------|---------------------------------------------------------------------------------------|
| \_WMDRM-ZERTIFIKATTYP \_ \_ V1 | Das Zertifikat wird in dem von Legacykomponenten verwendeten Format abgerufen.            |
| \_WMDRM-ZERTIFIKATTYP \_ \_ V2 | Das Zertifikat wird in dem Format abgerufen, das von den Windows Vista-Komponenten verwendet wird. |



 

</dd> <dt>

*rgbVersion \[ 4 \]* \[ out\]
</dt> <dd>

Array mit vier Bytes, das die Version des DRM-Subsystems auf dem Clientcomputer angibt.

</dd> <dt>

*ppbCertificate* \[ out\]
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf die Zertifikatdaten empfängt. Legen Sie diese Einstellung auf **NULL** fest, damit die -Methode die Puffergröße bereitstellt, die zum Speichern des Zertifikats in *"zertifikateCertificate"* erforderlich ist.

</dd> <dt>

*pwCertificate* \[ in, out\]
</dt> <dd>

Größe des Zertifikats in Bytes. Wenn *ppbCertificate* **NULL** ist, wird dieser Wert auf die Größe des Zertifikats festgelegt. Wenn *ppbCertificate* nicht **NULL** ist, muss dieser Wert auf die Größe des Puffers festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMDRMSecurity-Schnittstelle**](iwmdrmsecurity.md)
</dt> </dl>

 

 





