---
description: Gibt den Namen der Zertifizierungsstelle an.
ms.assetid: 224c2a51-8a25-4b66-b86b-c87531475145
title: 'Iscrdenr:: setcaname-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setCAName
- SCrdEnr.setCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 46dcd9294337c088b9e1b0ab68bddefe4308ed27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350048"
---
# <a name="iscrdenrsetcaname-method"></a>Iscrdenr:: setcaname-Methode

Die **setcaname** -Methode gibt den Namen der [*Zertifizierungs*](../secgloss/c-gly.md) Stelle an.

## <a name="syntax"></a>Syntax


```C++
HRESULT setCAName(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName,
  [in] BSTR bstrCAName
);
```


```VB

SCrdEnr.setCAName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByVal bstrCAName _
)
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Ein Wert, der angibt, ob der Name auf den ZS-Namen oder den Computernamen der Zertifizierungsstelle verweist. Wenn es sich bei diesem Wert um den Computer \_ \_ Namen der Zertifizierungsstelle \_ \_ (definiert als 0x01) handelt, bezieht sich der Name auf den Computernamen der Zertifizierungsstelle. Andernfalls bezieht sich der Name auf den Zertifizierungsstellen Namen.

</dd> <dt>

*bstraucerttemplatename* \[ in\]
</dt> <dd>

Name der Zertifikat Vorlage.

</dd> <dt>

*bstraucaname* \[ in\]
</dt> <dd>

Der ZS-Name, der mit der von *bstrincerttemplatename* angegebenen Zertifikat Vorlage verwendet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="vb"></a>VB

Der Rückgabewert ist ein **HRESULT**. Der Wert S \_ OK gibt an, dass der-Befehl erfolgreich ausgeführt wurde.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Methode, um eine Zertifizierungsstelle für eine Zertifikat Vorlage anzugeben.

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

[**Iscrdenr:: enumcaname**](iscrdenr-enumcaname.md)
</dt> <dt>

[**Iscrdenr:: getcaname**](iscrdenr-getcaname.md)
</dt> </dl>

 

 
