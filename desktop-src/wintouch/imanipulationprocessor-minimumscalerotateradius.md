---
title: IManipulationProcessor MinimumScaleRotateRadius (Eigenschaft)
description: Gibt an, wie groß die Entfernungs Kontakte in einer Skala oder Drehung sein müssen, um eine Manipulation zu initiieren.
ms.assetid: b4c49f41-c5ea-4c6a-872b-2d982e588b09
keywords:
- MinimumScaleRotateRadius-Eigenschaft, Windows-Fingereingabe
- MinimumScaleRotateRadius-Eigenschaft, Windows Touchscreen, IManipulationProcessor-Schnittstelle
- IManipulationProcessor Interface Windows-Fingereingabe, MinimumScaleRotateRadius (Eigenschaft)
topic_type:
- apiref
api_name:
- IManipulationProcessor.MinimumScaleRotateRadius
- IManipulationProcessor.get_MinimumScaleRotateRadius
- IManipulationProcessor.put_MinimumScaleRotateRadius
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location:
- manipulations.h
ms.openlocfilehash: 502d55e409f58127ddee94f5ba694a109c1ee1cb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718618"
---
# <a name="imanipulationprocessorminimumscalerotateradius-property"></a>IManipulationProcessor:: MinimumScaleRotateRadius (Eigenschaft)

Gibt an, wie groß die Entfernungs Kontakte in einer Skala oder Drehung sein müssen, um eine Manipulation zu initiieren.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_MinimumScaleRotateRadius(
  [in]  FLOAT MinimumScaleRotateRadius
);

HRESULT get_MinimumScaleRotateRadius(
  [out] FLOAT *MinimumScaleRotateRadius
);
```



## <a name="property-value"></a>Eigenschaftswert

Gibt den minimalen Abstand zwischen Kontakten an, um die Skalierung zu initiieren oder Gesten zu drehen.

## <a name="error-codes"></a>Fehlercodes

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Diese Eigenschaft wird in centipixels (hundert Sekunden) festgelegt.

 

Wenn dieser Wert festgelegt wird, ignoriert der Manipulations Prozessor Gesten, die zu klein sind. Dies ist hilfreich, wenn Sie verhindern möchten, dass ein Benutzer ein Objekt zu einem zu kleinen Radius bearbeitet. Wenn Sie z. b. einen Bearbeitungs Prozessor mit einem Kreis verwenden und sicherstellen möchten, dass ein RADIUS größer als 100 Pixel beibehalten wird, legen Sie diesen Wert auf 10000 fest.

## <a name="examples"></a>Beispiele


```C++
pManip->put_MinimumScaleRotateRadius(4000.0f);  
```



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor)
</dt> </dl>

 

 




