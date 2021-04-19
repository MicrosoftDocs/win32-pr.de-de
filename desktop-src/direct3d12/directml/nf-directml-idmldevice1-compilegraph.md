---
UID: NF:directml.IDMLDevice1.CompileGraph
title: 'IDMLDevice1:: compilegraph'
description: Kompiliert ein Diagramm von directml-Operatoren in ein Objekt, das an die GPU gesendet werden kann.
helpviewer_keywords:
- CompileGraph
- CompileGraph method
- CompileGraph method
- IDMLDevice1 interface
- IDMLDevice1 interface
- CompileGraph method
- IDMLDevice1.CompileGraph
- IDMLDevice1::CompileGraph
- direct3d12.idmldevice1_compileoperator
- directml/IDMLDevice1::CompileGraph
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
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
req.lib: DirectML.lib
req.dll: DirectML.dll
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDMLDevice1::CompileGraph
- directml/IDMLDevice1::CompileGraph
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- DirectML.dll
api_name:
- IDMLDevice1.CompileGraph
ms.openlocfilehash: 25dbc62fac9cd38d9728a295e336038441aee19f
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106361741"
---
# <a name="idmldevice1compilegraph-method-directmlh"></a>IDMLDevice1:: compilegraph-Methode (directml. h)

Kompiliert ein Diagramm von directml-Operatoren in ein Objekt, das an die GPU gesendet werden kann.

Ein kompilierter Operator stellt die effiziente, gebackte Form eines Operators dar, der für die Ausführung auf der GPU geeignet ist. Ein kompilierter Operator enthält Status (z. b. Shader und andere Objekte), die für die Ausführung erforderlich sind. Da ein kompilierter Operator die [idmlpable](/windows/win32/api/directml/nn-directml-idmlpageable) -Schnittstelle implementiert, können Sie bei Bedarf einen aus GPU-Speicher entfernen. Weitere Informationen finden Sie unter [IDMLDevice1:: evict](/windows/win32/api/directml/nf-directml-idmldevice-evict) und [IDMLDevice1:: makeresident](/windows/win32/api/directml/nf-directml-idmldevice-makeresident) .

Der kompilierte Operator verwendet weder noch die [idmloperator](/windows/win32/api/directml/nn-directml-idmloperator) -Objekte, die innerhalb der Diagramm Beschreibung bereitgestellt werden, nachdem diese Methode zurückgegeben wurde.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen Redistributable Package von directml verfügbar (siehe [Microsoft. ai. directml](https://www.nuget.org/packages/Microsoft.AI.DirectML/)). Siehe auch [Versionsverlauf der directml](../dml-version-history.md).

## <a name="syntax"></a>Syntax

```cpp
HRESULT CompileGraph(
  const DML_GRAPH_DESC *desc,
  DML_EXECUTION_FLAGS  flags,
  REFIID               riid,
  void                 **ppv
);
```

## <a name="parameters"></a>Parameter

`desc`

Typ: **[DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md)\***

Eine Beschreibung des zu kompilierenden Diagramms. Siehe [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md).

`flags`

Typ: [ **DML_EXECUTION_FLAGS**](/windows/win32/api/directml/ne-directml-dml_execution_flags)

Alle Flags zum Steuern der Ausführung dieses Operators.

`riid`

Typ: <b>refID</b>

Ein Verweis auf die Globally Unique Identifier (GUID) der Schnittstelle, die in <i>PPV</i>zurückgegeben werden soll. Dies wird als GUID von [idmlcompiledoperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator)erwartet.

`ppv`

Typ: <b>void * *</b>

Ein Zeiger auf einen Speicherblock, der einen Zeiger auf den kompilierten Operator empfängt. Dies ist die Adresse eines Zeigers auf einen [idmlcompiledoperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator), der den erstellten kompilierten Operator darstellt.


## <a name="return-value"></a>Rückgabewert

Typ: [ **HRESULT**](/windows/desktop/winprog/windows-data-types)

Wenn diese Methode erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Die Graph-API des directml-Operators bietet eine abstrakte Möglichkeit zur effizienten Verwendung von directml über verschiedene Hardware hinweg. Directml wendet Optimierungen auf tensorflow-Ebene an, z. b. die Auswahl des effizientesten tensorflow-Layouts basierend auf dem verwendeten Adapter. Außerdem werden Optimierungen angewendet, z. b. das Entfernen von Join-oder Split-Operatoren.

Es wird empfohlen, dass Sie vor dem Aufbau eines directml-Diagramms auf hoher Ebene Optimierungen anwenden. Beispielsweise das Zusammenfassen von-Operatoren mit batchnorm, Konstantenfaltung und allgemeiner Teil Ausdrucks Löschung. Die Optimierungen im Graph-Optimierer von directml dienen dazu, solche geräteunabhängigen Optimierungen zu ergänzen, die in der Regel generisch von Machine Learning-Frameworks verarbeitet werden.

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Zielplattform** | Windows |
| **Header** | directml. h |
| **Bibliothek** | Directml. lib |
| **DLL** | DirectML.dll |

## <a name="see-also"></a>Siehe auch

[IDMLDevice1](/windows/win32/api/directml/nn-directml-idmldevice)