---
title: Ienumtfrenderingmarkup-Klon Methode
description: Die ' ienumtfrenderingmarkup '-Klon Methode erstellt eine Kopie des Enumeratorobjekts.
ms.assetid: f1b0ccf9-36d1-4eff-af7c-d7fb4f0e9104
keywords:
- Klon Methode Text Services-Framework
- Klon Methode Text Dienste-Framework, ienumtfrenderingmarkup-Schnittstelle
- Ienumtfrenderingmarkup Interface Text Services-Framework, Klon Methode
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup.Clone
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f15d1bda18d2371f6518da4fa2884fac4df91b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340501"
---
# <a name="ienumtfrenderingmarkupclone-method"></a>Ienumtfrenderingmarkup:: Clone-Methode

Die **ienumtfrenderingmarkup:: Clone** -Methode erstellt eine Kopie des Enumeratorobjekts.

## <a name="syntax"></a>Syntax


```C++
HRESULT Clone(
  [out] IEnumTfRenderingMarkup **ppEnum
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppum* \[ vorgenommen\]
</dt> <dd>

\[\]ein Zeiger auf eine [ienumtfrenderingmarkup](/windows/desktop/TSF/ienumtfrenderingmarkup) -Schnittstelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                        | BESCHREIBUNG                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Die Methode war erfolgreich.<br/>          |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>       | Es ist ein unbekannter Fehler aufgetreten.<br/>      |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Mindestens ein Parameter ist ungültig.<br/> |



 

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Diese Methode befindet sich derzeit nicht in den öffentlichen Header Dateien. Um diese API verwenden zu können, müssen Sie den [Prototyp](prototypes.md)als Mittelpunkt kompilieren.

 

 

