---
title: IWMDRMLicense CreateSecureDecryptor-Methode (Wmdrmsdk.h)
description: Die CreateSecureDecryptor-Methode erstellt ein sicheres Entschlüsselungsobjekt. Die sichere Entschlüsselung unterscheidet sich von der normalen Entschlüsselungsmethode darin, dass sie den Inhalt entschlüsselt und dann gemäß den in den Parametern dieser Methode angegebenen Einstellungen erneut verschlüsselt.
ms.assetid: f3fe8d47-ec7b-4ba5-b5ae-6262cb455ffc
keywords:
- CreateSecureDecryptor-Methode windows Media Format
- CreateSecureDecryptor-Methode windows Media Format , IWMDRMLicense-Schnittstelle
- IWMDRMLicense-Schnittstelle windows Media Format , CreateSecureDecryptor-Methode
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
ms.openlocfilehash: 96c562dcafd72a72ecef340688fd709ecbe5446abae53403d403c9a70bdd6f2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118433669"
---
# <a name="iwmdrmlicensecreatesecuredecryptor-method"></a>IWMDRMLicense::CreateSecureDecryptor-Methode

Die **CreateSecureDecryptor-Methode** erstellt ein sicheres Entschlüsselungsobjekt. Die sichere Entschlüsselung unterscheidet sich von der normalen Entschlüsselungsmethode darin, dass sie den Inhalt entschlüsselt und dann gemäß den in den Parametern dieser Methode angegebenen Einstellungen erneut verschlüsselt.

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

*pbCertificate* \[ In\]
</dt> <dd>

Zertifikat der aufrufenden Anwendung.

</dd> <dt>

*cbCertificate* \[ In\]
</dt> <dd>

Größe des Zertifikats in Bytes.

</dd> <dt>

*dwCertificateType* \[ In\]
</dt> <dd>

Der Typ des Zertifikats. Legen Sie auf WMDRM \_ CERTIFICATE \_ TYPE XML \_ fest.

</dd> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Der Typ des Sitzungsschutzes, der für die erneute Codierung verwendet werden soll. Muss auf eine der Konstanten in der folgenden Tabelle festgelegt werden:



| Konstante                     | Beschreibung                                                                                                 |
|------------------------------|-------------------------------------------------------------------------------------------------------------|
| \_WMDRM-SCHUTZTYP \_ \_ RC4 | Verwendet RC4-Verschlüsselung für die Sitzungsverschlüsselung. Dies ist der einzige unterstützte Sitzungsschutz für diese Version. |



 

</dd> <dt>

*pbInitializationVector* \[ out\]
</dt> <dd>

Empfängt den Initialisierungsvektor. Der Initialisierungsvektor wird mithilfe des OAEP-Auffüllungsschemas mit dem öffentlichen RSA-Schlüssel im Zertifikat verschlüsselt. Legen Sie diese Einstellung auf **NULL** fest, um die erforderliche Puffergröße in *"pwInitializationVector"* zu erhalten.

</dd> <dt>

*pwInitializationVector* \[ in, out\]
</dt> <dd>

Bei der Eingabe die Größe des Puffers, der als *pbInitializationVector* übergeben wird. Bei der Ausgabe die Größe des verwendeten Teils des Puffers. Wenn Sie **NULL** für *pbInitializationVector* übergeben, wird dieser Wert bei der Ausgabe auf die erforderliche Puffergröße festgelegt.

</dd> <dt>

*ppDecryptor* \[ out\]
</dt> <dd>

Empfängt einen Zeiger auf die [**IWMDRMDecrypt-Schnittstelle**](iwmdrmdecrypt.md) des neu erstellten Objekts.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMDRMLicense-Schnittstelle**](iwmdrmlicense.md)
</dt> </dl>

 

 





