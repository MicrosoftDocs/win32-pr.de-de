---
description: Gibt ein Signaturzertifikat an (wird auch als Registrierungs-Agent-Zertifikat bezeichnet).
ms.assetid: db2437a9-46f6-48c3-9630-82ec556df645
title: 'Iscrdenr:: setsigningcertificate-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setSigningCertificate
- SCrdEnr.setSigningCertificate
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: dd00ba19872cb0ba2b21981c79e8f7be03aa4937
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350172"
---
# <a name="iscrdenrsetsigningcertificate-method"></a>Iscrdenr:: setsigningcertificate-Methode

Mit der **setsigningcertificate** -Methode wird ein Signaturzertifikat (auch als Registrierungs- *Agent-Zertifikat* bezeichnet) angegeben.

Vor der Registrierung im Namen von Benutzern müssen Sie ein Signaturzertifikat auswählen oder festlegen. Der diesem Signaturzertifikat zugeordnete [*private Schlüssel*](../secgloss/p-gly.md) wird verwendet, um eine PKCS 7-Anforderung zu signieren \# . Die PKCS \# 7 enthält wiederum die PKCS 10-Anforderung des Benutzers \# (die mit dem privaten Schlüssel des Benutzers signiert ist).

## <a name="syntax"></a>Syntax


```C++
HRESULT setSigningCertificate(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName
);
```


```VB

SCrdEnr.setSigningCertificate( _
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

Der Name der Zertifikat Vorlage für das Signaturzertifikat. Sie können den Wert "anmelmentagent" verwenden, wenn Sie ein Registrierungs Agent-Zertifikat erhalten haben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="vb"></a>VB

Wenn die Methode erfolgreich ausgeführt wird, gibt die Methode S \_ OK zurück.

Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).

## <a name="remarks"></a>Bemerkungen

Vor der Registrierung im Namen eines Benutzers müssen Sie zuerst ein Signaturzertifikat abrufen. Sie können ein Signaturzertifikat mit dem Zertifikat-Manager-MMC-Snap-in abrufen. Die **setsigningcertificate** -Methode erhält nicht das Signaturzertifikat, sondern informiert die Smartcard-Registrierungs Steuerung, die zuvor das zu verwendende Signaturzertifikat abgerufen hat. Die **setsigningcertificate** -Methode durchsucht den "My"-Speicher des Aufrufers nach dem neuesten Signaturzertifikat, das der von *bstrincerttemplatename* angegebenen Zertifikat Vorlage entspricht.

Eine Alternative zu **setsigningcertificate** ist **iscrdenr:: setsigningcertificate**.

Nachdem ein Signaturzertifikat festgelegt wurde, kann der zugehörige Name durch Aufrufen von [**iscrdenr:: getsigningcertifikatename**](iscrdenr-getsigningcertificatename.md)abgerufen werden.

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

 

 
