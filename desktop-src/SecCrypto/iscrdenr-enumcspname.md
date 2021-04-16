---
description: Listet den Namen der verfügbaren Kryptografiedienstanbieter (CSPs) auf.
ms.assetid: d0dc8a8a-afff-4ccc-96e0-2c52913c3322
title: 'Iscrdenr:: enumcspname-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.enumCSPName
- SCrdEnr.enumCSPName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: e7bba587b56300cd02efd81758288d3b77c65a66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529993"
---
# <a name="iscrdenrenumcspname-method"></a>Iscrdenr:: enumcspname-Methode

Die **enumcspname** -Methode listet den Namen der verfügbaren [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) (CSPs) auf.

## <a name="syntax"></a>Syntax


```C++
HRESULT enumCSPName(
  [in]  DWORD     dwIndex,
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrCSPName
);
```


```VB

SCrdEnr.enumCSPName( _
  ByVal dwIndex, _
  ByVal dwFlags, _
  ByRef pbstrCSPName _
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

Für die zukünftige Verwendung reserviert. Legen Sie diesen Wert auf NULL fest.

</dd> <dt>

*pbstrincspname* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Zeichenfolge, die den Namen des enumerierten CSP zurückgibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="c"></a>C++

Wenn die Methode erfolgreich ausgeführt wird, gibt die Methode S \_ OK zurück.

Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).

### <a name="vb"></a>VB

Eine Zeichenfolge, die den Namen des enumerierten CSP darstellt.

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

[**Iscrdenr:: cspname**](iscrdenr-cspname.md)
</dt> </dl>

 

 
