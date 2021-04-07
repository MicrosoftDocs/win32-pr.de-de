---
title: Ienumtfrenderingmarkup Skip-Methode
description: Die ienumtfrenderingmarkup Skip-Methode ruft die angegebene Anzahl von Elementen in der Enumerationsfolge von der aktuellen Position ab.
ms.assetid: d328dfe3-36ab-4daf-8809-ad6686ca5dae
keywords:
- Skip-Methode, Text Dienste-Framework
- Skip-Methode (Text Dienste-Framework), ienumtfrenderingmarkup-Schnittstelle
- Ienumtfrenderingmarkup Interface Text Services-Framework, Skip-Methode
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup.Skip
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3542893c739e6cfa2933d95bfed31f16957a0841
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718173"
---
# <a name="ienumtfrenderingmarkupskip-method"></a>Ienumtfrenderingmarkup:: Skip-Methode

Die **ienumtfrenderingmarkup:: Skip** -Methode ruft die angegebene Anzahl von Elementen in der Enumerationsfolge von der aktuellen Position ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT Skip(
  [in] ULONG ulCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ulcount* \[ in\]
</dt> <dd>

\[in \] gibt die Anzahl der zu über springenden Elemente an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                   | BESCHREIBUNG                                                                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | Die Methode war erfolgreich.<br/>                                                                              |
| <dl> <dt>**S \_ false**</dt> </dl> | Die Methode hat das Ende der Enumeration erreicht, bevor die angegebene Anzahl von Elementen übersprungen werden konnte.<br/> |



 

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Diese Methode befindet sich derzeit nicht in den öffentlichen Header Dateien. Um diese API verwenden zu können, müssen Sie den [Prototyp](prototypes.md)als Mittelpunkt kompilieren.

 

 

 





