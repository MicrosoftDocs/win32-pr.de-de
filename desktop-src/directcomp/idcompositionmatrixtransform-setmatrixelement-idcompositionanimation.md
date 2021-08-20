---
title: IDCompositionMatrixTransform SetMatrixElement(int, int, IDCompositionAnimation ) -Methode
description: Animiert den Wert eines Elements der Matrix dieser 2D-Transformation.
ms.assetid: 16A9E136-5F0C-4F34-A127-BF06C4530499
keywords:
- SetMatrixElement-Methode DirectComposition
- SetMatrixElement-Methode DirectComposition, IDCompositionMatrixTransform-Schnittstelle
- IDCompositionMatrixTransform-Schnittstelle DirectComposition , SetMatrixElement-Methode
topic_type:
- apiref
api_name:
- IDCompositionMatrixTransform.SetMatrixElement
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6c5a0813243f3d04a729f000c9e42a1eb1ade6406273a1217ca067d8e2f1c3a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043218"
---
# <a name="idcompositionmatrixtransformsetmatrixelementint-int-idcompositionanimation-method"></a>IDCompositionMatrixTransform::SetMatrixElement(int, int, IDCompositionAnimation \* ) -Methode

Animiert den Wert eines Elements der Matrix dieser 2D-Transformation.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetMatrixElement(
  [in] int                    row,
  [in] int                    column,
  [in] IDCompositionAnimation *animation
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*row* \[ In\]
</dt> <dd>

Der Zeilenindex des elements, das geändert werden soll. Dieser Wert muss zwischen 0 und 2 (einschließlich) liegen.

</dd> <dt>

*-Spalte* \[ In\]
</dt> <dd>

Der Spaltenindex des elements, das geändert werden soll. Dieser Wert muss zwischen 0 und 1 (einschließlich) liegen.

</dd> <dt>

*Animation* \[ In\]
</dt> <dd>

Eine Animation, die darstellt, wie sich der Wert des angegebenen Elements im Laufe der Zeit ändert. Dieser Parameter darf nicht NULL sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, wird S \_ OK zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben. Eine Liste der Fehlercodes finden Sie unter [DirectComposition-Fehlercodes.](directcomposition-error-codes.md)

## <a name="remarks"></a>Hinweise

Diese Methode erstellt eine Kopie der angegebenen Animation. Wenn das Objekt, auf das vom *Animationsparameter* verwiesen wird, nach dem Aufruf dieser Methode geändert wird, wirkt sich die Änderung nicht auf das Element aus, es sei denn, diese Methode wird erneut aufgerufen. Wenn das Element zuvor animiert wurde, ersetzt der Aufruf dieser Methode die vorherige Animation durch die neue Animation.

Diese Methode schlägt fehl, wenn *die Animation* ein ungültiger Zeiger ist oder nicht von der gleichen [**IDCompositionDevice-Schnittstelle**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) wie die betroffene Transformation erstellt wurde. Die Schnittstelle darf keine benutzerdefinierte Implementierung sein. nur von Microsoft DirectComposition erstellte Schnittstellen können mit dieser Methode verwendet werden.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDCompositionMatrixTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform)
</dt> </dl>

 

 