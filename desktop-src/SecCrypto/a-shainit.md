---
description: Initiiert das hashdown eines Datenstroms.
ms.assetid: 0EA7C98E-777C-4B2A-AF35-04F90BA3D024
title: A_SHAInit-Funktion (SHA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- A_SHAInit
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 831c86b02c946896014fa9eec02270f2e963e484
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364431"
---
# <a name="a_shainit-function"></a>Eine \_ shainit-Funktion

Initiiert das hashdown eines Datenstroms.

## <a name="syntax"></a>Syntax


```C++
void RSA32API A_SHAInit(
  _Inout_ A_SHA_CTX *Context
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Kontext* \[ in, out\]
</dt> <dd>

Der SHA-Kontext.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Funktion ähnelt shainit stark, wird aber direkt aus der Bibliothek aufgerufen, anstatt über die kryptografieinfrastruktur weitergeleitet zu werden. Weitere Informationen finden Sie unter [Windows-ntkryptografieanbieter](/previous-versions/tn-archive/cc723484(v=technet.10)).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>SHA. h</dt> </dl>     |
| Bibliothek<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |
| DLL<br/>     | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
