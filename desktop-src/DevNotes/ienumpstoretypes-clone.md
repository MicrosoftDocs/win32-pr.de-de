---
description: Erstellt einen zusätzlichen Enumerator, der den gleichen Enumerationszustand wie der aktuelle enthält.
ms.assetid: b4027520-62cc-40d4-b9fd-01fa9c652a54
title: IEnumPStoreTypes::Clone-Methode (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes.Clone
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: b1f93fed0e6631dff0eac0d5bf149138d189abed73bae7301df2561970376104
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002220"
---
# <a name="ienumpstoretypesclone-method"></a>IEnumPStoreTypes::Clone-Methode

\[Protected Storage (Pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar. Sie ist nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista verfügbar, aber in nachfolgenden Versionen möglicherweise nicht verfügbar. Pstore verwendet eine ältere Implementierung des Datenschutzes. Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den [**Funktionen CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData bereitgestellt**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) wird.\]

Erstellt einen zusätzlichen Enumerator, der den gleichen Enumerationszustand wie der aktuelle enthält.

## <a name="syntax"></a>Syntax


```C++
HRESULT Clone(
  [out] IEnumPStoreItems **ppenum
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppenum* \[ out\]
</dt> <dd>

Ein Zeiger auf einen [**IEnumPStoreItems-Zeiger.**](ienumpstoreitems.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein **HRESULT-Wert.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IEnumPStoreItems**](ienumpstoreitems.md)
</dt> <dt>

[**IEnumPStoreTypes**](ienumpstoretypes.md)
</dt> </dl>

 

 
