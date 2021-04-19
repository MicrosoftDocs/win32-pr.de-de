---
description: Verschiebt eine MDIForm, ein Formular oder ein Steuerelement.
ms.assetid: 963e6533-f571-4043-bdd8-2596df6b5b35
title: 'IExtender:: Move-Methode'
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
ms.openlocfilehash: 2c7ed806629f0e5e1bb0cdee5c76910728fd651d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358734"
---
# <a name="iextendermove-method"></a>IExtender:: Move-Methode

Verschiebt eine MDIForm, ein Formular oder ein Steuerelement.

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

*Links* \[ in\]
</dt> <dd>

Der linke Rand des Formulars oder Steuer Elements.

</dd> <dt>

nach *oben* \[ in\]
</dt> <dd>

Der obere Rand des Formulars oder Steuer Elements.

</dd> <dt>

*Breite* \[ in\]
</dt> <dd>

Die Breite des Formulars oder Steuer Elements.

</dd> <dt>

*Höhe* \[ in\]
</dt> <dd>

Die Höhe des Formulars oder Steuer Elements.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ole2disp.dll; </dt> <dt>Oleaut32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IExtender**](iextender.md)
</dt> </dl>

 

 




