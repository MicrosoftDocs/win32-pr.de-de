---
description: Die getkaraokechannelzuweisungs-Methode ruft einen Wert ab, der angibt, wie die Karaoke-Kanäle den Referenten zugewiesen werden.
ms.assetid: 08e35fa6-fa1b-4f9f-8f56-d953c4422226
title: Getkaraokechannelzuweisungs-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dafe1217e08f3dc4f55aeec42424b1ebf9d86d22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860546"
---
# <a name="getkaraokechannelassignment-method"></a>Getkaraokechannelzuweisungs-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `GetKaraokeChannelAssignment` Methode ruft einen Wert ab, der angibt, wie die Karaoke-Kanäle den Referenten zugewiesen werden.

``` syntax
[ iAssignment = ] MSWebDVD.GetKaraokeChannelAssignment(iStream)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*IStream*
</dt> <dd>

Gibt den Audiodatenstrom als Ganzzahl an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt eine ganze Zahl zurück, die die Lautsprecher Zuweisung für den angegebenen Stream angibt.



| Rückgabecode | Beschreibung                                                             |
|-------------|-------------------------------------------------------------------------|
| 2           | Der Stream wird dem linken und rechten Referenten zugewiesen.                  |
| 3           | Der Stream wird dem linken, rechten und mittleren Referenten zugewiesen.         |
| 4           | Der Stream wird dem linken, rechten und audio1-Sprecher zugewiesen.         |
| 5           | Der Stream wird dem linken, rechten, mittleren und audio1-Sprecher zugewiesen. |
| 6           | Der Stream wird dem linken, rechten und Audio2-Sprecher zugewiesen.         |
| 7           | Der Stream wird dem linken, rechten, mittleren und Audio2-Sprecher zugewiesen. |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Karaokeaudiopressentiments ationmode**](karaokeaudiopresentationmode-property.md)
</dt> </dl>

 

 



