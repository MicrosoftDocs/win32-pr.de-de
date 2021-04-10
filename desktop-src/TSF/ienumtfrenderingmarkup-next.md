---
title: Ienumtfrenderingmarkup Next-Methode
description: Die ienumtfrenderingmarkup Next-Methode ruft die angegebene Anzahl von Elementen in der Enumerationsfolge von der aktuellen Position ab.
ms.assetid: a3aec919-2c65-4e65-9430-d73fdaf5d28e
keywords:
- Next-Methode Text Services-Framework
- Next Method Text Services Framework, ienumtfrenderingmarkup-Schnittstelle
- Ienumtfrenderingmarkup Interface Text Services-Framework, Next-Methode
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup.Next
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0989d35a2fa7c521d5ea103fbe40a73d012a3997
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039239"
---
# <a name="ienumtfrenderingmarkupnext-method"></a>Ienumtfrenderingmarkup:: Next-Methode

Die **ienumtfrenderingmarkup:: Next** -Methode ruft die angegebene Anzahl von Elementen in der Enumerationsfolge von der aktuellen Position ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT Next(
  [out] ULONG ulCount,
  [out]       ppElement,
  [out] ULONG *pcFetched
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ulcount* \[ vorgenommen\]
</dt> <dd>

\[Out \] gibt die Anzahl der abzurufenden Elemente an.

</dd> <dt>

*ppelement* \[ vorgenommen\]
</dt> <dd>

\[Out- \] Zeiger auf ein Array von [tf \_ renderingmarkup](/windows/desktop/TSF/tf-renderingmarkup) -Strukturen. Dieses Array muss mindestens eine *ulcount* -Elementgröße aufweisen.

</dd> <dt>

*pcfetch* \[ vorgenommen\]
</dt> <dd>

\[Out- \] Zeiger auf einen Ulong-Wert, der die Anzahl der tatsächlich erhaltenen Elemente empfängt. Dieser Wert kann kleiner als die Anzahl der angeforderten Elemente sein. Dieser Parameter kann **NULL** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                        | BESCHREIBUNG                                                                                                         |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Die Methode war erfolgreich.<br/>                                                                               |
| <dl> <dt>**S \_ false**</dt> </dl>      | Die Methode hat das Ende der Enumeration erreicht, bevor die angegebene Anzahl von Elementen abgerufen werden konnte.<br/> |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Mindestens ein Parameter ist ungültig.<br/>                                                                      |



 

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Diese Methode befindet sich derzeit nicht in den öffentlichen Header Dateien. Um diese API verwenden zu können, müssen Sie den [Prototyp](prototypes.md)als Mittelpunkt kompilieren.

 

 

