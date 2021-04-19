---
description: Listet den Namen der Zertifizierungsstellen (CAS) für einen angegebenen Namen für die Zertifikat Vorlage auf.
ms.assetid: 82cc3346-a8b9-4abd-933a-c212a37a373e
title: 'Iscrdenr:: enumcaname-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.enumCAName
- SCrdEnr.enumCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: c23df2f74cdf3791f1280e38cbff8ddd48f924b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349658"
---
# <a name="iscrdenrenumcaname-method"></a>Iscrdenr:: enumcaname-Methode

Mit der **enumcaname** -Methode wird der Name der [*Zertifizierungs*](../secgloss/c-gly.md) stellen (CAS) für einen angegebenen Zertifikat Vorlagen Namen aufgelistet.

## <a name="syntax"></a>Syntax


```C++
HRESULT enumCAName(
  [in]  DWORD     dwIndex,
  [in]  DWORD     dwFlags,
  [in]  BSTR     bstrCertTemplateName,
  [out] BSTR *pbstrCAName
);
```


```VB

SCrdEnr.enumCAName( _
  ByVal dwIndex, _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByRef pbstrCAName _
)
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*dwIndex* \[ in\]
</dt> <dd>

Der null basierte Index für die enumerationssequenz.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Ein-Wert, der bestimmt, ob der Name auf den ZS-Namen oder den Computernamen der Zertifizierungsstelle verweist. Wenn es sich bei diesem Wert um den Computer \_ \_ Namen der Zertifizierungsstelle \_ \_ (definiert als 0x01) handelt, bezieht sich der Name auf den Computernamen der Zertifizierungsstelle. Andernfalls bezieht sich der Name auf den Zertifizierungsstellen Namen.

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

[**Iscrdenr:: getcacount**](iscrdenr-getcacount.md)
</dt> <dt>

[**Iscrdenr:: getcaname**](iscrdenr-getcaname.md)
</dt> <dt>

[**Iscrdenr:: setcaname**](iscrdenr-setcaname.md)
</dt> </dl>

 

 
