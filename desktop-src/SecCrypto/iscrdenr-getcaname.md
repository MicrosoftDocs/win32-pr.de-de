---
description: Ruft den Namen der angegebenen Zertifizierungsstelle (Certification Authority, ca) für eine angegebene Zertifikat Vorlage ab.
ms.assetid: e921710a-7c74-4fda-91e1-fbad45889984
title: 'Iscrdenr:: getcaname-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCAName
- SCrdEnr.getCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: b62b0a7e871a29ff0a8edd28eb8cd5e18e97c1a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217997"
---
# <a name="iscrdenrgetcaname-method"></a>Iscrdenr:: getcaname-Methode

Die **getcaname** -Methode ruft den Namen der angegebenen Zertifizierungsstelle ( [*Certification Authority*](../secgloss/c-gly.md) , ca) für eine angegebene Zertifikat Vorlage ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT getCAName(
  [in]  DWORD     dwFlags,
  [in]  BSTR     bstrCertTemplateName,
  [out] BSTR *pbstrCAName
);
```


```VB

SCrdEnr.getCAName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByRef pbstrCAName _
)
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Ein-Wert, der bestimmt, ob der Name auf den ZS-Namen oder den Computernamen der Zertifizierungsstelle verweist. Wenn es sich bei diesem Wert um den Computer \_ \_ Namen der Zertifizierungsstelle \_ \_ (definiert als 0x01) handelt, verweist der Name auf den Computernamen der Zertifizierungsstelle; andernfalls bezieht sich der Name auf den Namen der Zertifizierungsstelle.

</dd> <dt>

*bstraucerttemplatename* \[ in\]
</dt> <dd>

Der Name der Zertifikat Vorlage.

</dd> <dt>

*pbstraucaname* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die den Namen der Zertifizierungsstelle zurückgibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="c"></a>C++

Wenn die Methode erfolgreich ausgeführt wird, gibt die Methode S \_ OK zurück.

Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).

### <a name="vb"></a>VB

Eine Zeichenfolge, die den Namen der Zertifizierungsstelle darstellt.

## <a name="remarks"></a>Bemerkungen

Der Standardname der Zertifizierungsstelle ist der Vorname in der Liste der verfügbaren Zertifizierungsstellen.

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

[**Iscrdenr:: getcacount**](iscrdenr-getcacount.md)
</dt> <dt>

[**Iscrdenr:: setcaname**](iscrdenr-setcaname.md)
</dt> </dl>

 

 
