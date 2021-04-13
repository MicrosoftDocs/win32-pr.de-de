---
description: Ruft die Anzahl der Kryptografiedienstanbieter (CSPs) ab.
ms.assetid: 7e0c1613-85ad-4f25-837e-d7b0f11e654a
title: 'Iscrdenr:: cspcount-Eigenschaft'
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
ms.openlocfilehash: b2aea22db3c804ae4808996002b68efdcb6cf9a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348518"
---
# <a name="iscrdenrcspcount-property"></a>Iscrdenr:: cspcount-Eigenschaft

Die **cspcount** -Eigenschaft ruft die Anzahl der [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) (CSPs) ab.

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

Wenn die Methode erfolgreich ausgeführt wird, gibt die Methode S \_ OK zurück.

Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).

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

[**Iscrdenr:: cspname**](iscrdenr-cspname.md)
</dt> <dt>

[**Iscrdenr:: enumcspname**](iscrdenr-enumcspname.md)
</dt> </dl>

 

 
