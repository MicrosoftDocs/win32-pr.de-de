---
description: Gibt einen pccert- \_ Ketten kontextfrei, \_ der über die ChainContext-Eigenschaft abgerufen wurde.
ms.assetid: fa9a6171-58ff-400f-bdcc-ba32a0ae0441
title: 'Ichaincontext:: freecontext-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext.FreeContext
- ChainContext.FreeContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 413b119f250bfbd061301391fee7741362979f65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368578"
---
# <a name="ichaincontextfreecontext-method"></a>Ichaincontext:: freecontext-Methode

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.\]

Die **freecontext** -Methode gibt einen pccert- \_ Ketten kontextfrei, \_ der über die [**chainContext**](ichaincontext-chaincontext.md) -Eigenschaft abgerufen wurde.

## <a name="syntax"></a>Syntax


```VB
ChainContext.FreeContext()
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pchaincontext* \[ in\]
</dt> <dd>

Der zu veröffentlichende pccert- \_ Ketten \_ Kontext.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT**. Der Wert S \_ OK weist auf Erfolg hin. Jeder andere Wert gibt an, dass der Vorgang fehlgeschlagen ist.

## <a name="remarks"></a>Bemerkungen

Diese Methode gibt nicht den \_ \_ in einem [**Ketten**](chain.md) Objekt enthaltenen pccert-Ketten kontextfrei. Es sollte nur verwendet werden, um einen mit \_ \_ der [**chainContext**](ichaincontext-chaincontext.md) -Eigenschaft erworbenen pccert-Ketten kontextfrei zugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ichaincontext**](ichaincontext.md)
</dt> </dl>

 

 




