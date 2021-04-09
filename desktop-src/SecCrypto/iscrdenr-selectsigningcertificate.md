---
description: Zeigt das Dialogfeld Zertifikat auswählen an, in dem ein Signaturzertifikat (auch als Registrierungs-Agent-Zertifikat bezeichnet) ausgewählt werden kann.
ms.assetid: b8198f65-4ffb-4dfa-8286-e62ef483ab16
title: 'Iscrdenr:: selectsigningcertificate-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.selectSigningCertificate
- SCrdEnr.selectSigningCertificate
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: a4ef3be0ef16797597f57c12e90736ba50109601
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868207"
---
# <a name="iscrdenrselectsigningcertificate-method"></a>Iscrdenr:: selectsigningcertificate-Methode

Die **selectsigningcertificate** -Methode zeigt das Dialogfeld **Zertifikat auswählen** an, in dem ein Signaturzertifikat (auch als Registrierungs- *Agent-Zertifikat* bezeichnet) ausgewählt werden kann.

Vor der Registrierung im Namen von Benutzern müssen Sie ein Signaturzertifikat auswählen. Der diesem Signaturzertifikat zugeordnete [*private Schlüssel*](../secgloss/p-gly.md) wird verwendet, um eine PKCS 7-Anforderung zu signieren \# . Die PKCS \# 7 enthält wiederum die PKCS 10-Anforderung des Benutzers \# (die mit dem privaten Schlüssel des Benutzers signiert ist).

## <a name="syntax"></a>Syntax


```C++
HRESULT selectSigningCertificate(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName
);
```


```VB

SCrdEnr.selectSigningCertificate( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName _
)
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Für die zukünftige Verwendung reserviert. Legen Sie diesen Wert auf NULL fest.

</dd> <dt>

*bstraucerttemplatename* \[ in\]
</dt> <dd>

Eine Zeichenfolge, die den Namen der Zertifikat Vorlage für das Signaturzertifikat darstellt. Sie können den Wert "anmelmentagent" verwenden, wenn Sie ein Registrierungs Agent-Zertifikat erhalten haben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="vb"></a>VB

Wenn die Methode erfolgreich ausgeführt wird, gibt die Methode **S \_ OK** zurück.

Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).

## <a name="remarks"></a>Bemerkungen

Vor der Registrierung im Namen eines Benutzers müssen Sie zuerst ein Signaturzertifikat abrufen. Sie können ein Signaturzertifikat mit dem Zertifikat-Manager-MMC-Snap-in abrufen. Von der **selectsigningcertificate** -Methode wird das Signaturzertifikat nicht abgerufen, aber es wird ein Dialogfeld mit zuvor abzurufenden Signatur Zertifikaten angezeigt, sodass Sie auswählen können, welches Zertifikat zum Signieren der Anforderungen zum Registrieren im Auftrag verwendet wird.

Eine Alternative zu **selectsigningcertificate** ist [**iscrdenr:: setsigningcertificate**](iscrdenr-setsigningcertificate.md).

Nachdem ein Signaturzertifikat ausgewählt wurde, kann der zugehörige Name durch Aufrufen von [**iscrdenr:: getsigningcertifikatename**](iscrdenr-getsigningcertificatename.md)abgerufen werden.

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

[**Iscrdenr:: getsigningcertificename**](iscrdenr-getsigningcertificatename.md)
</dt> </dl>

 

 
