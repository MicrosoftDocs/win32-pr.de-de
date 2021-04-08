---
description: Die issubpicturestreamaktivierte-Methode ruft einen Wert ab, der angibt, ob der angegebene subbildstream im aktuellen Titel aktiviert ist.
ms.assetid: c6436f77-ca94-464f-9336-f485f5d5d199
title: Issubpicturestreamaktivierte Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 818b4ff18dac87ea3346a1a503764b2e5e9cd02a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860428"
---
# <a name="issubpicturestreamenabled-method"></a>Issubpicturestreamaktivierte Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `IsSubpictureStreamEnabled` Methode ruft einen Wert ab, der angibt, ob der angegebene teilbildstream im aktuellen Titel aktiviert ist.

``` syntax
[ bEnabled = ] MSWebDVD.IsSubpictureStreamEnabled(iStream)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*IStream*
</dt> <dd>

Gibt den subbildstream als Ganzzahl an.



| Wert   | BESCHREIBUNG              |
|---------|--------------------------|
| 0 bis 31 | subbildstream        |
| 63      | gedämpfter Datenstrom mit niedriger Bitrate |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen booleschen Wert zurück, der angibt, ob der angegebene Audiostream im aktuellen Titel verfügbar ist. "True" bedeutet, dass Sie verfügbar ist.

## <a name="remarks"></a>Bemerkungen

Obwohl eine CD bis zu 32 unter bildstreams enthalten kann, ist jeder Stream nicht notwendigerweise für jeden Titel verfügbar. Überprüfen Sie vor dem Festlegen der [**currentsubpicturestream**](currentsubpicturestream-property.md) -Eigenschaft immer, ob ein Datenstrom für einen Titel verfügbar ist.

 

 



