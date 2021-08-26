---
description: Verschiebt ein MDIForm-, Formular- oder -Steuerelement.
ms.assetid: 963e6533-f571-4043-bdd8-2596df6b5b35
title: IExkeeper::Move-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IExtender.Move
api_type:
- COM
api_location:
- Ole2disp.dll
- Oleaut32.dll
ms.openlocfilehash: 13002457952490588fa9e9ad40e7f66e7d31465b74f9757a3193ccaed1e8bf7e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002100"
---
# <a name="iextendermove-method"></a>IExkeeper::Move-Methode

Verschiebt ein MDIForm-, Formular- oder -Steuerelement.

## <a name="syntax"></a>Syntax


```C++
void Move(
  [in] object left,
  [in] object top,
  [in] object width,
  [in] object height
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*links* \[ In\]
</dt> <dd>

Der linke Rand des Formulars oder Steuerelements.

</dd> <dt>

*top* \[ In\]
</dt> <dd>

Der obere Rand des Formulars oder Steuerelements.

</dd> <dt>

*width* \[ In\]
</dt> <dd>

Die Breite des Formulars oder Steuerelements.

</dd> <dt>

*height* \[ In\]
</dt> <dd>

Die Höhe des Formulars oder Steuerelements.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ole2disp.dll; </dt> <dt>Oleaut32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IExkeeper**](iextender.md)
</dt> </dl>

 

 




