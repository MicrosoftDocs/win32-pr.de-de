---
description: Ruft den icontextlink am angegebenen Index ab.
ms.assetid: 46bb71b9-5ef3-4756-97f6-40e0aaa82826
title: 'Icontextlinks:: getcontextlink-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLinks.GetContextLink
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ecc0ed9ba457a7a91cb2e1b615ac7419ce5a94c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129509"
---
# <a name="icontextlinksgetcontextlink-method"></a>Icontextlinks:: getcontextlink-Methode

Ruft den [**icontextlink**](icontextlink.md) am angegebenen Index ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetContextLink(
  [in]  ULONG        ulIndex,
  [out] IContextLink **ppContextLink
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ulindex* \[ in\]
</dt> <dd>

Der null basierte Index des abzurufenden [**icontextlink**](icontextlink.md) -Objekts.

</dd> <dt>

*ppcontextlink* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf das [**icontextlink**](icontextlink.md) -Objekt am angegebenen Index.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, müssen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf \* *ppcontextlink* abrufen, wenn Sie den Kontext Link nicht mehr verwenden müssen.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Icontextlinks**](icontextlinks.md)
</dt> <dt>

[**Icontextnode**](icontextnode.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

