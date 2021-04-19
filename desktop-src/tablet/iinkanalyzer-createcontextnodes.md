---
description: Erstellt ein icontextnodes-Objekt.
ms.assetid: d6d37595-307b-4cbc-9d48-ad10f8b272dd
title: 'Iinkanalyzer:: kreatecontextnodes-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.CreateContextNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 07bdfc9a32fd4aec8e716cdd3c788c211c1adaec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359852"
---
# <a name="iinkanalyzercreatecontextnodes-method"></a>Iinkanalyzer:: anatecontextnodes-Methode

Erstellt ein [**icontextnodes**](icontextnodes.md) -Objekt.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateContextNodes(
  [out] IContextNodes **ppContextNodes
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppcontextnodes* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf das [**icontextnodes**](icontextnodes.md) -Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf *ppcontextnodes* , wenn Sie das-Objekt nicht mehr verwenden müssen.

 

Verwenden Sie diese Methode, um eine leere [**icontextnodes**](icontextnodes.md) -Auflistung zu erstellen, die mit [**iinkanalyzer**](iinkanalyzer.md)verknüpft ist. Die neue **icontextnodes** -Auflistung ist nicht Teil der Kontext Struktur des **iinkanalyzer** -Objekts.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iinkanalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Icontextnodes**](icontextnodes.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

