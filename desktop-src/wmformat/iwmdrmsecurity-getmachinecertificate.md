---
title: Iwmdrmsecurity getmachinecertificate-Methode (wmdrmsdk. h)
description: Die getmachinecertificate-Methode ruft das Computer Zertifikat des DRM-Subsystems auf dem Client Computer ab.
ms.assetid: 38b8e812-e997-4a63-b906-ebd26a5556be
keywords:
- Getmachinecertificate-Methode Windows Media-Format
- Getmachinecertificate-Methode, Windows Media-Format, iwmdrmsecurity-Schnittstelle
- Iwmdrmsecurity-Schnittstelle Windows Media-Format, getmachinecertificate-Methode
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
ms.openlocfilehash: 8d6c66c54ab9528a458910def5978ec83b191654
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371088"
---
# <a name="iwmdrmsecuritygetmachinecertificate-method"></a>Iwmdrmsecurity:: getmachinecertificate-Methode

Die **getmachinecertificate** -Methode ruft das Computer Zertifikat des DRM-Subsystems auf dem Client Computer ab.

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

*dwcertifialisietype* \[ in\]
</dt> <dd>

Der Typ des abzurufenden Zertifikats. Legen Sie auf einen der Werte in der folgenden Tabelle fest.



| Wert                        | BESCHREIBUNG                                                                           |
|------------------------------|---------------------------------------------------------------------------------------|
| WMDRM \_ - \_ Zertifikattyp \_ v1 | Das Zertifikat wird im von Legacy Komponenten verwendeten Format abgerufen.            |
| WMDRM \_ - \_ Zertifikattyp \_ v2 | Das Zertifikat wird in dem Format abgerufen, das von den Windows Vista-Komponenten verwendet wird. |



 

</dd> <dt>

*rgbversion \[ 4 \]* ausgehend \[\]
</dt> <dd>

Array von vier Bytes, die die Version des DRM-Subsystems auf dem Client Computer angeben.

</dd> <dt>

*ppbcertificate* \[ vorgenommen\]
</dt> <dd>

Adresse einer Variablen, die einen Zeiger auf die Zertifikat Daten empfängt. Legen Sie diese Einstellung auf **null** fest, damit die Methode die Puffergröße bereitstellt, die zum Speichern des Zertifikats in *pcbcertificate* erforderlich ist.

</dd> <dt>

*pcbcertificate* \[ in, out\]
</dt> <dd>

Größe des Zertifikats in Bytes. Wenn *ppbcertificate* den Wert **null** hat, wird dieser Wert auf die Größe des Zertifikats festgelegt. Wenn *ppbcertificate* nicht **null** ist, muss dieser Wert auf die Größe des Puffers festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmdrmsecurity-Schnittstelle**](iwmdrmsecurity.md)
</dt> </dl>

 

 





