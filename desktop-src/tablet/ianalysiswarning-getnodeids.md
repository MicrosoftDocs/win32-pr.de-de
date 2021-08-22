---
description: Gibt die Bezeichner aller relevanten Kontextknoten zurück, die dieser Warnung zugeordnet sind.
ms.assetid: 8c418f48-3903-47c1-82e2-085de39574d4
title: IAnalysisWarning::GetNodeIds-Methode (IACom.h)
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
ms.openlocfilehash: 97e6f4fde66faef14402c815f6b95517a2bd19adfb90eac4e865383770bc753f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967479"
---
# <a name="ianalysiswarninggetnodeids-method"></a>IAnalysisWarning::GetNodeIds-Methode

Gibt die Bezeichner aller relevanten Kontextknoten zurück, die dieser Warnung zugeordnet sind.

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

Die Anzahl global eindeutiger Bezeichner (GUIDs) in *ppNodeIds*.

</dd> <dt>

*ppNodeIds* \[ out\]
</dt> <dd>

Ein Zeiger auf ein Array von GUIDs, das die Kontextknoten identifiziert, die dieser Analysewarnung zugeordnet sind, oder **NULL,** wenn der Warnung keine Kontextknoten zugeordnet sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Hinweise

Wenn *ppNodeIds als* NULL übergeben **wird,** gibt die **GetNodeIds-Methode** **S \_ OK** zurück, und die Anzahl der Rechtecke wird in *pulCount zurückgegeben.*

> [!Caution]  
> Um einen Arbeitsspeicherverlust zu vermeiden, verwenden Sie [**CoTaskMemFree,**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) um den Arbeitsspeicher von \* *ppNodeIds* frei zu geben, wenn Sie die Informationen nicht mehr benötigen.

 

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie sie die [**IContextNode-Objekte**](icontextnode.md) in [**IAnalysisWarning**](ianalysiswarning.md), und nur die Anzahl der `warning` **IContextNode-Objekte erhalten.**


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
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IAnalysisWarning**](ianalysiswarning.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IInkAnalyzer::FindNode-Methode**](iinkanalyzer-findnode.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

