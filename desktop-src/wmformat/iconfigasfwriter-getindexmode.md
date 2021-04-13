---
title: Iconfigasfwriter getindexmode-Methode
description: Die getindexmode-Methode ruft den aktuellen temporalen Index Modus ab.
ms.assetid: beb874ea-d0d5-4323-a817-47984911da4c
keywords:
- Getindexmode-Methode Windows Media-Format
- Getindexmode-Methode, Windows Media-Format, iconfigasfwriter-Schnittstelle
- Iconfigasfwriter-Schnittstelle Windows Media-Format, getindexmode-Methode
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetIndexMode
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb701f591579d3113e79b0b9b74167ac8de3d75f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390572"
---
# <a name="iconfigasfwritergetindexmode-method"></a>Iconfigasfwriter:: getindexmode-Methode

Die **getindexmode** -Methode ruft den aktuellen temporalen Index Modus ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetIndexMode(
  [out] BOOL *pbIndexFile
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbindexfile* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable vom Typ **bool** , der die Einstellung für den temporalen Indexmodus empfängt. Der Wert **true** gibt an, dass der WM-ASF-Writer so konfiguriert ist, dass Temporale indizierte Dateien geschrieben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück. Wenn ein Fehler auftritt, wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Methode, um zu bestimmen, ob der [WM-ASF-Writer](wm-asf-writer-filter.md) momentan zum Schreiben temporärindizierter ASF-Dateien konfiguriert ist. Weitere Informationen über Temporale indizierte und Frame indizierte Dateien finden Sie in den Hinweisen zu [**iconfigasfwriter:: setindexmode**](iconfigasfwriter-setindexmode.md).

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iconfigasfwriter-Schnittstelle**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 