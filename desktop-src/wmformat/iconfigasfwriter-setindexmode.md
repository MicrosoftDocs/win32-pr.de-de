---
title: IConfigAsfWriter SetIndexMode-Methode
description: Mit der SetIndexMode-Methode kann die Anwendung steuern, ob die Datei temporal indiziert wird.
ms.assetid: 104e29f4-a1e5-4e26-a9ef-52ef52d6f5b2
keywords:
- SetIndexMode-Methode windows Media Format
- SetIndexMode-Methode windows Media Format , IConfigAsfWriter-Schnittstelle
- IConfigAsfWriter-Schnittstelle windows Media Format , SetIndexMode-Methode
topic_type:
- apiref
api_name:
- IConfigAsfWriter.SetIndexMode
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b65fbd3d279b8a66c132d24476b09b0f897c5993ea9a97d86096cf856832f9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118433611"
---
# <a name="iconfigasfwritersetindexmode-method"></a>IConfigAsfWriter::SetIndexMode-Methode

Mit der **SetIndexMode-Methode** kann die Anwendung steuern, ob die Datei temporal indiziert wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetIndexMode(
  [in] BOOL bIndexFile
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bIndexFile* \[ In\]
</dt> <dd>

Variable vom Typ **BOOL**; **TRUE** gibt an, dass die Datei temporal indiziert wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, wird S \_ OK zurückgegeben. Wenn ein Fehler auftritt, wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Standardmäßig erstellt WM [ASF Writer](wm-asf-writer-filter.md) temporal indizierte ASF-Dateien. Die Indizierung wird ausgeführt, wenn das Diagramm beendet wird. Sie können dieses Verhalten deaktivieren, wenn Sie eine eigene framebasierte Indizierung als Nachbearbeitungsschritt durchführen möchten. Um eine frameindizierte Datei zu erstellen, rufen **Sie SetIndexMode**(FALSE) auf, erstellen Sie die Datei, und verwenden Sie dann die methoden Windows Media Format SDK direkt, um einen framebasierten Index für die Datei zu erstellen.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IConfigAsfWriter-Schnittstelle**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 