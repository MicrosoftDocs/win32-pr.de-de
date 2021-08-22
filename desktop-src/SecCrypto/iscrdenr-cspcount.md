---
description: Ruft die Anzahl der Kryptografiedienstanbieter (Cryptographic Service Providers, CSPs) ab.
ms.assetid: 7e0c1613-85ad-4f25-837e-d7b0f11e654a
title: ISCrdEnr::CSPCount-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.CSPCount
- ISCrdEnr.get_CSPCount
- SCrdEnr.CSPCount
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 5ae2a25bbdb6efb3eff9bd0a94049e0c5674e5ba7c32e3939500097f19959037
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005238"
---
# <a name="iscrdenrcspcount-property"></a>ISCrdEnr::CSPCount-Eigenschaft

Die **CSPCount-Eigenschaft** ruft die Anzahl der [*Kryptografiedienstanbieter (Cryptographic Service Providers,*](../secgloss/c-gly.md) CSPs) ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_CSPCount(
   LONG *pVal
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Anzahl der CSPs.

## <a name="error-codes"></a>Fehlercodes

Wenn die Methode erfolgreich ist, gibt die Methode S \_ OK zurück.

Wenn die Methode fehlschlägt, wird ein **HRESULT-Wert** zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte.](common-hresult-values.md)

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

[**ISCrdEnr::CSPName**](iscrdenr-cspname.md)
</dt> <dt>

[**ISCrdEnr::enumCSPName**](iscrdenr-enumcspname.md)
</dt> </dl>

 

 
