---
title: Idcompositionmatrixtransform setmatrixelement (int, int, idcompositionanimation)-Methode
description: Animiert den Wert eines Elements der Matrix dieser 2D-Transformation.
ms.assetid: 16A9E136-5F0C-4F34-A127-BF06C4530499
keywords:
- Setmatrixelement-Methode directcomposition
- Setmatrixelement-Methode directcomposition, idcompositionmatrixtransform-Schnittstelle
- Idcompositionmatrixtransform-Schnittstelle directcomposition, setmatrixelement-Methode
topic_type:
- apiref
api_name:
- IDCompositionMatrixTransform.SetMatrixElement
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5b4bf2a43e762b85b8b8cfd0c15468b3dc438221
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390750"
---
# <a name="idcompositionmatrixtransformsetmatrixelementint-int-idcompositionanimation-method"></a>Idcompositionmatrixtransform:: setmatrixelement (int, int, idcompositionanimation \* )-Methode

Animiert den Wert eines Elements der Matrix dieser 2D-Transformation.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetMatrixElement(
  [in] int                    row,
  [in] int                    column,
  [in] IDCompositionAnimation *animation
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Zeile* \[ in\]
</dt> <dd>

Der Zeilen Index des Elements, das geändert werden soll. Dieser Wert muss zwischen 0 und 2 (einschließlich) liegen.

</dd> <dt>

*Spalte* \[ in\]
</dt> <dd>

Der Spalten Index des Elements, das geändert werden soll. Dieser Wert muss zwischen 0 und 1 (einschließlich) liegen.

</dd> <dt>

*Animation* \[ in\]
</dt> <dd>

Eine Animation, die darstellt, wie sich der Wert des angegebenen Elements im Laufe der Zeit ändert. Dieser Parameter darf nicht NULL sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [directcomposition-Fehlercodes](directcomposition-error-codes.md) .

## <a name="remarks"></a>Bemerkungen

Diese Methode erstellt eine Kopie der angegebenen Animation. Wenn das Objekt, auf das der *Animations* Parameter verweist, nach dem Aufrufen dieser Methode geändert wird, wirkt sich die Änderung nicht auf das Element aus, es sei denn, diese Methode wird erneut aufgerufen. Wenn das Element zuvor animiert wurde, ersetzt das Aufrufen dieser Methode die vorherige Animation durch die neue Animation.

Diese Methode schlägt fehl, wenn *Animation* ein ungültiger Zeiger ist oder wenn Sie nicht von derselben [**idcompositiondevice**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) -Schnittstelle wie die betroffene Transformation erstellt wurde. Die Schnittstelle kann keine benutzerdefinierte Implementierung sein. mit dieser Methode können nur Schnittstellen verwendet werden, die von Microsoft directcomposition erstellt wurden.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Idcompositionmatrixtransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform)
</dt> </dl>

 

 