---
description: Legt den Namen des Kryptografiedienstanbieters (Cryptographic Service Provider, CSP) fest oder ruft den Namen ab.
ms.assetid: 34fde7b0-747d-4592-a89a-207f82369f52
title: ISCrdEnr::CSPName-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.CSPName
- ISCrdEnr.get_CSPName
- ISCrdEnr.put_CSPName
- SCrdEnr.CSPName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 7a1b5b443807dfe7fa737cdfc5eb4da678845e53b555ffe6eebf1529583fdb35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005228"
---
# <a name="iscrdenrcspname-property"></a>ISCrdEnr::CSPName-Eigenschaft

Die **CSPName-Eigenschaft** legt den Namen des Kryptografiedienstanbieters [*(Cryptographic Service Provider,*](../secgloss/c-gly.md) CSP) fest oder ruft den Namen ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_CSPName(
   BSTR newVal
);

HRESULT get_CSPName(
   BSTR *pVal
);
```



## <a name="property-value"></a>Eigenschaftswert

Der Name des CSP.

## <a name="error-codes"></a>Fehlercodes

Wenn die Methode erfolgreich ist, gibt die Methode S \_ OK zurück.

Wenn bei der Methode ein Fehler auftritt, wird ein **HRESULT-Wert** zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).

## <a name="remarks"></a>Hinweise

Legen Sie diese Eigenschaft fest, um den Namen des CSP anzugeben, der mit dem Smartcard-Registrierungssteuersatz verwendet werden soll. Rufen Sie diese Eigenschaft ab, um den Namen des angegebenen CSP abzurufen. Wenn Sie keinen Wert für diese Eigenschaft angeben, wird die **CSPName-Eigenschaft** standardmäßig auf den Vornamen in der liste der verfügbaren CSPs festgelegt.

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

[**ISCrdEnr::CSPCount**](iscrdenr-cspcount.md)
</dt> <dt>

[**ISCrdEnr::enumCSPName**](iscrdenr-enumcspname.md)
</dt> </dl>

 

 
