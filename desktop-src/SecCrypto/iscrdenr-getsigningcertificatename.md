---
description: Ruft den Antragsteller Namen aus dem Signaturzertifikat ab.
ms.assetid: e50b1e12-ec89-4d58-aa57-dc24aa2409ef
title: 'Iscrdenr:: getsigningcertifitorename-Methode'
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
ms.openlocfilehash: 8d9a8a84067e82a18e5066721f3e7f39d075c339
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393693"
---
# <a name="iscrdenrgetsigningcertificatename-method"></a>Iscrdenr:: getsigningcertifitorename-Methode

Die **getsigningcertifikatename** -Methode ruft den Antragsteller Namen aus dem Signaturzertifikat ab.

Diese Methode kann auch verwendet werden, um das Zertifikat in einem Dialogfeld anzuzeigen. Diese Methode ruft die [*CryptoAPI*](../secgloss/c-gly.md) -Funktion [**certgetnamestring**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa)auf.

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

*dwFlags* \[ in\]
</dt> <dd>

Ein-Wert, der bestimmt, ob das Zertifikat in einem Dialogfeld angezeigt wird. Wenn dieser Wert "SCard \_ ENROLL \_ No \_ Display \_ CERT (als 0x01 definiert)" lautet, wird das Signaturzertifikat nicht angezeigt. alle anderen Werte führen dazu, dass das Signaturzertifikat im Dialogfeld " **Zertifikat** " angezeigt wird.

</dd> <dt>

*pbstrausigningcertname* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die den Namen des Signatur Zertifikats zurückgibt. Das Signaturzertifikat wird verwendet, um die [*Zertifikat Anforderung*](../secgloss/c-gly.md)zu signieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="c"></a>C++

Wenn die Methode erfolgreich ausgeführt wird, gibt die Methode S \_ OK zurück.

Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).

### <a name="vb"></a>VB

Eine Zeichenfolge, die den Namen des Signatur Zertifikats darstellt. Das Signaturzertifikat wird verwendet, um die [*Zertifikat Anforderung*](../secgloss/c-gly.md)zu signieren.

## <a name="remarks"></a>Bemerkungen

Die **getsigningcertifikatename** -Methode gibt den Antragsteller Namen des Zertifikats, das Sie (oder ein anderer Administrator) ausgewählt haben, in einem vorherigen erfolgreichen [**iscrdenr:: selectsigningcertificate**](iscrdenr-selectsigningcertificate.md) -oder [**iscrdenr:: setsigningcertificate**](iscrdenr-setsigningcertificate.md)-Vorgang zurück. Diese Methode ruft die [**certgetnamestring**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) -Funktion auf, um den Antragsteller Namen entsprechend der für den "CERT \_ Name \_ Simple \_ Display Type" \_ -Wert des *dwType* -Parameters von **certgetnamestring** beschriebenen Sequenz abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ iscrdenr ist definiert als 753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iscrdenr**](iscrdenr.md)
</dt> <dt>

[**Iscrdenr:: selectsigningcertificate**](iscrdenr-selectsigningcertificate.md)
</dt> </dl>

 

 
