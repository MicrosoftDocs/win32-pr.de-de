---
description: Ruft den Namen des Betreffs aus dem Signaturzertifikat ab.
ms.assetid: e50b1e12-ec89-4d58-aa57-dc24aa2409ef
title: ISCrdEnr::getSigningCertificateName-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getSigningCertificateName
- SCrdEnr.getSigningCertificateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 29933856eb644e638e9e58c8da0b0e3d6234e4f0175925c8a1fb5b48b126e3ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622400"
---
# <a name="iscrdenrgetsigningcertificatename-method"></a>ISCrdEnr::getSigningCertificateName-Methode

Die **getSigningCertificateName-Methode** ruft den Namen des Betreffs aus dem Signaturzertifikat ab.

Diese Methode kann auch verwendet werden, um das Zertifikat in einem Dialogfeld anzuzeigen. Diese Methode ruft die [*CryptoAPI-Funktion*](../secgloss/c-gly.md) [**CertGetNameString auf.**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa)

## <a name="syntax"></a>Syntax


```C++
HRESULT getSigningCertificateName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrSigningCertName
);
```


```VB

SCrdEnr.getSigningCertificateName( _
  ByVal dwFlags, _
  ByRef pbstrSigningCertName _
)
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Ein -Wert, der bestimmt, ob das Zertifikat in einem Dialogfeld angezeigt wird. Wenn dieser Wert SCARD \_ ENROLL \_ NO DISPLAY \_ CERT (definiert als \_ 0x01) ist,  wird das Signaturzertifikat nicht angezeigt. Alle anderen Werte führen dazu, dass das Signaturzertifikat im Dialogfeld Zertifikat angezeigt wird.

</dd> <dt>

*pbstrSigningCertName* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die den Namen des Signaturzertifikats zurückgibt. Das Signaturzertifikat wird verwendet, um die [*Zertifikatanforderung zu signieren.*](../secgloss/c-gly.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="c"></a>C++

Wenn die Methode erfolgreich ist, gibt die Methode S \_ OK zurück.

Wenn bei der Methode ein Fehler auftritt, wird ein **HRESULT-Wert** zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).

### <a name="vb"></a>VB

Eine Zeichenfolge, die den Namen des Signaturzertifikats darstellt. Das Signaturzertifikat wird verwendet, um die [*Zertifikatanforderung zu signieren.*](../secgloss/c-gly.md)

## <a name="remarks"></a>Hinweise

Die **getSigningCertificateName-Methode** gibt den Betreffnamen des Zertifikats zurück, das Sie (oder ein anderer Administrator) in einem vorherigen erfolgreichen Aufruf von [**ISCrdEnr::selectSigningCertificate**](iscrdenr-selectsigningcertificate.md) oder [**ISCrdEnr::setSigningCertificate ausgewählt haben.**](iscrdenr-setsigningcertificate.md) Diese Methode ruft die [**CertGetNameString-Funktion**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) auf, um den Betreffnamen gemäß der Sequenz abzurufen, die für den CERT NAME SIMPLE DISPLAY TYPE-Wert des dwType-Parameters von \_ \_ \_ \_ **CertGetNameString** *beschrieben* ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCrdEnr ist als 753988a1-1357-436d-9cf5-f089bdd67d64 definiert.<br/>             |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr::selectSigningCertificate**](iscrdenr-selectsigningcertificate.md)
</dt> </dl>

 

 
