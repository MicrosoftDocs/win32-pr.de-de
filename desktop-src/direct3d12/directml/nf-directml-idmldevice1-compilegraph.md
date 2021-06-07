---
UID: NF:directml.IDMLDevice1.CompileGraph
title: IDMLDevice1::CompileGraph
description: Kompiliert ein Diagramm von DirectML-Operatoren in ein Objekt, das an die GPU gesendet werden kann.
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
ms.openlocfilehash: 8a9b4ce9bd8f8bd8b1d6f2a6bbd144009eb0d79d
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417175"
---
# <a name="idmldevice1compilegraph-method-directmlh"></a>IDMLDevice1::CompileGraph-Methode (directml.h)

Kompiliert ein Diagramm von DirectML-Operatoren in ein Objekt, das an die GPU gesendet werden kann.

Ein kompilierter Operator stellt die effiziente, gebackene Form eines Operators dar, der für die Ausführung auf der GPU geeignet ist. Ein kompilierter Operator enthält den Zustand (z. B. Shader und andere Objekte), der für die Ausführung erforderlich ist. Da ein kompilierter Operator die [IDMLPageable-Schnittstelle](/windows/win32/api/directml/nn-directml-idmlpageable) implementiert, können Sie eine schnittstelle aus dem GPU-Speicher aus dem GPU-Speicher ausziehen, wenn Sie möchten. Weitere Informationen finden Sie unter [IDMLDevice1::Evict](/windows/win32/api/directml/nf-directml-idmldevice-evict) und [IDMLDevice1::MakeResident.](/windows/win32/api/directml/nf-directml-idmldevice-makeresident)

Der kompilierte Operator verwendet die [IDMLOperator-Objekte,](/windows/win32/api/directml/nn-directml-idmloperator) die in der Graphbeschreibung angegeben sind, und verweist nicht darauf, nachdem diese Methode zurückgegeben wurde.

> [!IMPORTANT]
> Diese API ist als Teil des eigenständigen verteilbaren DirectML-Pakets verfügbar (siehe [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) Version 1.4 und höher). Siehe auch [DirectML-Versionsverlauf.](../dml-version-history.md)

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

Eine Beschreibung des zu kompilierenden Diagramms. Weitere Informationen finden Sie [unter DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md).

`flags`

Typ: [ **DML_EXECUTION_FLAGS**](/windows/win32/api/directml/ne-directml-dml_execution_flags)

Alle Flags zum Steuern der Ausführung dieses Operators.

`riid`

Typ: <b>REFIID</b>

Ein Verweis auf die GUID (Globally Unique Identifier) der Schnittstelle, die in <i>ppv</i>zurückgegeben werden soll. Es wird erwartet, dass dies die GUID von [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator)ist.

`ppv`

Typ: <b>void**</b>

Ein Zeiger auf einen Speicherblock, der einen Zeiger auf den kompilierten Operator empfängt. Dies ist die Adresse eines Zeigers auf einen [IDMLCompiledOperator,](/windows/win32/api/directml/nn-directml-idmlcompiledoperator)der den erstellten kompilierten Operator darstellt.


## <a name="return-value"></a>Rückgabewert

Typ: [ **HRESULT**](/windows/desktop/winprog/windows-data-types)

Wenn diese Methode erfolgreich ist, wird **S_OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Die Graph-API für DirectML-Operatoren bietet eine abstrakte Möglichkeit, DirectML effizient auf verschiedenen Hardwarekomponenten zu verwenden. DirectML wendet Optimierungen auf Tensorebene an, z. B. die Auswahl des effizientesten Tensorlayouts basierend auf dem verwendeten Adapter. Außerdem werden Optimierungen wie das Entfernen von Join- oder Split-Operatoren angewendet.

Es wird empfohlen, vor dem Erstellen eines DirectML-Graphen optimierungsorientierte Optimierungen anzuwenden. Beispiel: Zusammenführung von Convolution-Operatoren mit BatchNorm, Konstantenfaltung und gängiger Teilausdruckslöschung. Die Optimierungen im Graphoptimierer von DirectML sollen solche geräteunabhängigen Optimierungen ergänzen, die in der Regel generisch von Machine Learning-Frameworks verarbeitet werden.

## <a name="requirements"></a>Requirements (Anforderungen)
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Zielplattform** | Windows |
| **Header** | directml.h |
| **Bibliothek** | DirectML.lib |
| **Dll** | DirectML.dll |

## <a name="see-also"></a>Siehe auch

[IDMLDevice1](/windows/win32/api/directml/nn-directml-idmldevice)