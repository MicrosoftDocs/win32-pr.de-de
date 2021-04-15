---
description: Gibt die Bezeichner aller relevanten Kontext Knoten zurück, die dieser Warnung zugeordnet sind.
ms.assetid: 8c418f48-3903-47c1-82e2-085de39574d4
title: 'Ianalysiswarning:: GetNodeIds-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetNodeIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a38abd054e457ef9dbaf5dd93c38954b1ce6dcb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526540"
---
# <a name="ianalysiswarninggetnodeids-method"></a>Ianalysiswarning:: GetNodeIds-Methode

Gibt die Bezeichner aller relevanten Kontext Knoten zurück, die dieser Warnung zugeordnet sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetNodeIds(
  [in, out] ULONG *pulCount,
  [out]     GUID  **ppNodeIds
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pulCount* \[ in, out\]
</dt> <dd>

Die Anzahl der global eindeutigen Bezeichner (GUIDs) in *ppnodeids*.

</dd> <dt>

*ppnodeids* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf ein Array von GUIDs, das die dieser Analyse Warnung zugeordneten Kontext Knoten identifiziert, oder **null** , wenn der Warnung keine Kontext Knoten zugeordnet sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Wenn *ppnodeids* als **null**-Werte übermittelt wird, gibt die **GetNodeIds** -Methode **S \_ OK** zurück, und die Anzahl der Rechtecke wird in *pulCount* zurückgegeben.

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, verwenden Sie " [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) ", um den Arbeitsspeicher von \* *ppnodeids* freizugeben, wenn Sie die Informationen nicht mehr benötigen.

 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie Sie die [**icontextnode**](icontextnode.md) -Objekte, die sich in [**ianalysiswarning**](ianalysiswarning.md)befinden, `warning` sowie die Anzahl der **icontextnode** -Objekte erhalten.


```C++
// Get the count of the context nodes and their identifiers.
ULONG count = 0;
GUID* nodeIds = 0;
warning->GetNodeIds(&count, &nodeIds);

// Use nodeIds

::CoTaskMemFree(nodeIds);

// GetNodeIds just gets the count and returns S_OK
ULONG number = 0;
warning->GetNodeIds(&number, NULL); 
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ianalysiswarning**](ianalysiswarning.md)
</dt> <dt>

[**Icontextnode**](icontextnode.md)
</dt> <dt>

[**Iinkanalyzer:: FindNode-Methode**](iinkanalyzer-findnode.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

