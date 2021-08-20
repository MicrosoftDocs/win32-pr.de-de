---
title: IEnumTfRenderingMarkup-Skip-Methode
description: Die Methode IEnumTfRenderingMarkup Skip ruft von der aktuellen Position die angegebene Anzahl von Elementen in der Enumerationssequenz ab.
ms.assetid: d328dfe3-36ab-4daf-8809-ad6686ca5dae
keywords:
- Skip-Methode Textdienstframework
- Überspringen der Methode Textdienstframework , IEnumTfRenderingMarkup-Schnittstelle
- IEnumTfRenderingMarkup-Schnittstelle Textdienstframework , Skip-Methode
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup.Skip
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5e0dddd637abdfd193586277d088a2ee3d03f883eb1f949d9f9d16c4cbc60ac3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117953201"
---
# <a name="ienumtfrenderingmarkupskip-method"></a>IEnumTfRenderingMarkup::Skip-Methode

Die **IEnumTfRenderingMarkup::Skip-Methode** ruft von der aktuellen Position die angegebene Anzahl von Elementen in der Enumerationssequenz ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT Skip(
  [in] ULONG ulCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ulCount* \[ In\]
</dt> <dd>

\[in \] Gibt die Anzahl der zu überspringenden Elemente an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                   | Beschreibung                                                                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | Die Methode war erfolgreich.<br/>                                                                              |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Die -Methode hat das Ende der -Enumeration erreicht, bevor die angegebene Anzahl von Elementen übersprungen werden konnte.<br/> |



 

## <a name="remarks"></a>Hinweise

> [!Note]  
> Diese Methode befindet sich derzeit nicht in den öffentlichen Headerdateien. Um diese API verwenden zu können, müssen Sie midl-kompilieren, um den [Prototyp](prototypes.md)zu kompilieren.

 

 

 





