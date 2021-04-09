---
description: Legt den Namen des Kryptografiedienstanbieters (CSP) fest oder ruft ihn ab.
ms.assetid: 34fde7b0-747d-4592-a89a-207f82369f52
title: 'Iscrdenr:: cspname-Eigenschaft'
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
ms.openlocfilehash: 363f2f9120d3b0a202335d0e8e450464cbc1f118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050430"
---
# <a name="iscrdenrcspname-property"></a>Iscrdenr:: cspname-Eigenschaft

Die **cspname** -Eigenschaft legt den Namen des [*Kryptografiedienstanbieters*](../secgloss/c-gly.md) (CSP) fest oder ruft ihn ab.

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

Wenn die Methode erfolgreich ausgeführt wird, gibt die Methode S \_ OK zurück.

Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).

## <a name="remarks"></a>Bemerkungen

Legen Sie diese Eigenschaft fest, um den Namen des CSP anzugeben, der mit der Smartcard-Registrierungs Steuerung verwendet werden soll. Rufen Sie diese Eigenschaft ab, um den Namen des angegebenen CSP abzurufen. Wenn Sie für diese Eigenschaft keinen Wert angeben, wird die **cspname** -Eigenschaft standardmäßig auf den Vornamen in der Liste verfügbarer CSPs-Objekte festgelegt.

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

[**Iscrdenr:: cspcount**](iscrdenr-cspcount.md)
</dt> <dt>

[**Iscrdenr:: enumcspname**](iscrdenr-enumcspname.md)
</dt> </dl>

 

 
