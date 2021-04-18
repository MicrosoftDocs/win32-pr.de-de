---
title: Iwmdrmlicense | atesecuredecryptor-Methode (wmdrmsdk. h)
description: Die Methode "kreatesecuredecryptor" erstellt ein sicheres Entschlüsselungs-Objekt. Der sichere entschlüsselungstyp unterscheidet sich vom normalen entschlüsselungstyp darin, dass er den Inhalt entschlüsselt und dann gemäß den in den Parametern dieser Methode angegebenen Einstellungen erneut verschlüsselt.
ms.assetid: f3fe8d47-ec7b-4ba5-b5ae-6262cb455ffc
keywords:
- "\"Kreatesecuredecryptor\"-Methode Windows Media-Format"
- Kreatesecuredecryptor-Methode Windows Media-Format, iwmdrmlicense-Schnittstelle
- Iwmdrmlicense-Schnittstelle Windows Media-Format, Methode "kreatesecuredecryptor"
topic_type:
- apiref
api_name:
- IWMDRMLicense.CreateSecureDecryptor
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ededb4c985e345c1e40563d02c87bfe447b8960f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358210"
---
# <a name="iwmdrmlicensecreatesecuredecryptor-method"></a>Iwmdrmlicense:: kreatesecuredecryptor-Methode

Die Methode " **kreatesecuredecryptor** " erstellt ein sicheres Entschlüsselungs-Objekt. Der sichere entschlüsselungstyp unterscheidet sich vom normalen entschlüsselungstyp darin, dass er den Inhalt entschlüsselt und dann gemäß den in den Parametern dieser Methode angegebenen Einstellungen erneut verschlüsselt.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateSecureDecryptor(
  [in]      BYTE          *pbCertificate,
  [in]      DWORD         cbCertificate,
  [in]      DWORD         dwCertificateType,
  [in]      DWORD         dwFlags,
  [out]     BYTE          *pbInitializationVector,
  [in, out] DWORD         *pcbInitializationVector,
  [out]     IWMDRMDecrypt **ppDecryptor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbcertificate* \[ in\]
</dt> <dd>

Zertifikat der aufrufenden Anwendung.

</dd> <dt>

*cbcertificate* \[ in\]
</dt> <dd>

Größe des Zertifikats in Bytes.

</dd> <dt>

*dwcertifialisietype* \[ in\]
</dt> <dd>

Der Typ des Zertifikats. Legen Sie auf WMDRM \_ Certificate \_ Type \_ XML fest.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Der Typ des Sitzungs Schutzes, der für die erneute Codierung verwendet werden soll. Muss auf eine der Konstanten in der folgenden Tabelle festgelegt werden:



| Konstante                     | BESCHREIBUNG                                                                                                 |
|------------------------------|-------------------------------------------------------------------------------------------------------------|
| WMDRM \_ - \_ Schutztyp \_ RC4 | Verwendet die RC4-Verschlüsselung für die Sitzungs Verschlüsselung. Dies ist der einzige unterstützte Sitzungs Schutz für diese Version. |



 

</dd> <dt>

*pbinitializationvector* \[ vorgenommen\]
</dt> <dd>

Empfängt den Initialisierungs Vektor. Der Initialisierungs Vektor ist RSA mit dem OAEP-Auffüll Schema verschlüsselt, wobei der öffentliche RSA-Schlüssel im Zertifikat gefunden wird. Legen Sie diesen Wert auf **null** fest, um die erforderliche Puffergröße in *pcbinitializationvector* zu erhalten.

</dd> <dt>

*pcbinitializationvector* \[ in, out\]
</dt> <dd>

Bei Eingabe die Größe des Puffers, der als *pbinitializationvector* übergeben wird. Bei Ausgabe die Größe des verwendeten Teils des Puffers. Wenn Sie **null** für *pbinitializationvector* übergeben, wird dieser Wert auf die erforderliche Puffergröße bei der Ausgabe festgelegt.

</dd> <dt>

*ppdecryptor* \[ vorgenommen\]
</dt> <dd>

Empfängt einen Zeiger auf die [**iwmdrmentschlüsseln**](iwmdrmdecrypt.md) -Schnittstelle des neu erstellten Objekts.

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

[**Iwmdrmlicense-Schnittstelle**](iwmdrmlicense.md)
</dt> </dl>

 

 





