---
UID: NE:directml.DML_AXIS_DIRECTION
title: DML_AXIS_DIRECTION
description: Definiert Konstanten, die die Richtung eines Vorgangs entlang der angegebenen Achse für den Operator angeben (z. b. die Summe, das Auswählen der Top-k-Elemente, das Auswählen des minimalen Elements).
ms.topic: reference
tech.root: directml
ms.date: 10/28/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DML_AXIS_DIRECTION
- directml/DML_AXIS_DIRECTION
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
- DML_AXIS_DIRECTION
ms.openlocfilehash: 18cd2189f88378245be0824e0a68e5f618008bc7
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106366531"
---
# <a name="dml_axis_direction-enumeration-directmlh"></a>DML_AXIS_DIRECTION-Enumeration (directml. h)

Definiert Konstanten, die die Richtung eines Vorgangs entlang der angegebenen Achse für den Operator angeben (z. b. die Summe, das Auswählen der Top-k-Elemente, das Auswählen des minimalen Elements).

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). Siehe auch [Versionsverlauf der directml](../dml-version-history.md).

## <a name="syntax"></a>Syntax
```cpp
typedef enum DML_AXIS_DIRECTION {
  DML_AXIS_DIRECTION_INCREASING,
  DML_AXIS_DIRECTION_DECREASING
} ;
```

## <a name="constants"></a>Konstanten

| Name | BESCHREIBUNG |
| ---- |:---- |
| DML_AXIS_DIRECTION_INCREASING | Gibt die ansteigende Reihenfolge an (vom unteren Index zum hohen Index). |
| DML_AXIS_DIRECTION_DECREASING | Gibt die abnehmende Reihenfolge an (vom hohen Index zum unteren Index). |


## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |