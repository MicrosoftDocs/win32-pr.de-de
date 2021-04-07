---
title: Iconfigasfwriter setindexmode-Methode
description: Die setindexmode-Methode ermöglicht der Anwendung, zu steuern, ob die Datei temporell indiziert wird.
ms.assetid: 104e29f4-a1e5-4e26-a9ef-52ef52d6f5b2
keywords:
- Setindexmode-Methode Windows Media-Format
- Setindexmode-Methode Windows Media-Format, iconfigasfwriter-Schnittstelle
- Iconfigasfwriter-Schnittstelle Windows Media-Format, setindexmode-Methode
topic_type:
- apiref
api_name:
- IConfigAsfWriter.SetIndexMode
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 25d5f2b985aeca490323aecaef2595d52b99056c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039036"
---
# <a name="iconfigasfwritersetindexmode-method"></a>Iconfigasfwriter:: setindexmode-Methode

Die **setindexmode** -Methode ermöglicht der Anwendung, zu steuern, ob die Datei temporell indiziert wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetIndexMode(
  [in] BOOL bIndexFile
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bindexfile* \[ in\]
</dt> <dd>

Variable vom Typ **bool**; **True** gibt an, dass die Datei temporell indiziert wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück. Wenn ein Fehler auftritt, wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Standardmäßig erstellt der [WM-ASF-Writer](wm-asf-writer-filter.md) Temporale indizierte ASF-Dateien. Die Indizierung wird durchführt, wenn das Diagramm angehalten wird. Sie können dieses Verhalten deaktivieren, wenn Sie eine eigene Frame basierte Indizierung als nach Verarbeitungsschritt ausführen möchten. Um eine Frame indizierte Datei zu erstellen, rufen Sie **setindexmode**(false) auf, erstellen Sie die Datei, und verwenden Sie dann die SDK-Methoden des Windows Media-Formats direkt, um einen Frame basierten Index für die Datei zu erstellen.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iconfigasfwriter-Schnittstelle**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 