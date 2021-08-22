---
description: Gibt einen PCCERT \_ CHAIN \_ CONTEXT frei, der über die ChainContext-Eigenschaft erworben wurde.
ms.assetid: fa9a6171-58ff-400f-bdcc-ba32a0ae0441
title: IChainContext::FreeContext-Methode
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
ms.openlocfilehash: 10a6d0576cefd1c28e8f05fe455b89be90dcd36386b4312ef1921511616bce2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005488"
---
# <a name="ichaincontextfreecontext-method"></a>IChainContext::FreeContext-Methode

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.\]

Die **FreeContext-Methode** gibt einen PCCERT \_ CHAIN CONTEXT \_ frei, der über die [**ChainContext-Eigenschaft erworben**](ichaincontext-chaincontext.md) wurde.

## <a name="syntax"></a>Syntax


```VB
ChainContext.FreeContext()
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pChainContext* \[ In\]
</dt> <dd>

Der PCCERT \_ CHAIN \_ CONTEXT, der freigegeben werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT.** Der Wert S \_ OK gibt den Erfolg an. Jeder andere Wert gibt an, dass der Vorgang fehlgeschlagen ist.

## <a name="remarks"></a>Hinweise

Diese Methode gibt den PCCERT CHAIN CONTEXT, der in einem Chain-Objekt enthalten \_ \_ [**ist, nicht**](chain.md) frei. Es sollte nur verwendet werden, um einen PCCERT CHAIN CONTEXT frei zu geben, \_ \_ der über die [**ChainContext-Eigenschaft erworben**](ichaincontext-chaincontext.md) wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2.0 oder höher auf Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IChainContext**](ichaincontext.md)
</dt> </dl>

 

 




