---
description: Die isaudiostreamaktivierte-Methode ruft einen Wert ab, der angibt, ob der angegebene Audiostream im aktuellen Titel aktiviert ist.
ms.assetid: df6c69a7-6eb0-4662-a3aa-f3f895b42cbc
title: Isaudiostreamaktivierte Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c92df59479e5729c392eb25b6c6c075a52b4835b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520395"
---
# <a name="isaudiostreamenabled-method"></a>Isaudiostreamaktivierte Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `IsAudioStreamEnabled` -Methode ruft einen Wert ab, der angibt, ob der angegebene Audiostream im aktuellen Titel aktiviert ist.

``` syntax
[bEnabled = ] MSWebDVD.IsAudioStreamEnabled(iStream)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*IStream*
</dt> <dd>

Gibt den Audiodatenstrom als ganzzahligen Wert zwischen 0 und 7 an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen booleschen Wert zurück, der angibt, ob der angegebene Audiodatenstrom für den aktuellen Titel verfügbar ist. "True" bedeutet, dass Sie verfügbar ist.

## <a name="remarks"></a>Bemerkungen

Obwohl eine CD bis zu acht unabhängige Audiodatenströme enthalten kann, ist jeder Stream nicht notwendigerweise für jeden Titel verfügbar. Beispielsweise kann ein hauptfilmtitel drei Audiodatenströme für Englisch, Spanisch und Japanisch enthalten, aber der Titel "Kommende Attraktionen" hat möglicherweise nur einen Audiostream in englischer Sprache. Überprüfen Sie vor dem Festlegen der [**currentaudiostream**](currentaudiostream-property.md) -Eigenschaft immer, ob ein Datenstrom für einen Titel verfügbar ist.

 

 



