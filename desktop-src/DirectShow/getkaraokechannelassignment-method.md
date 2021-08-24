---
description: Die GetKaraokeChannelAssignment-Methode ruft einen Wert ab, der angibt, wie die Kanäle den Sprechern zugewiesen werden.
ms.assetid: 08e35fa6-fa1b-4f9f-8f56-d953c4422226
title: GetKaraokeChannelAssignment-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 010e8112ece9b3fc66831055995ebf46657d4216942ac3b9dee05b1b68d18761
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812550"
---
# <a name="getkaraokechannelassignment-method"></a>GetKaraokeChannelAssignment-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `GetKaraokeChannelAssignment` -Methode ruft einen Wert ab, der angibt, wie den Sprechern die Senderkanäle zugewiesen werden.

``` syntax
[ iAssignment = ] MSWebDVD.GetKaraokeChannelAssignment(iStream)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*Istream*
</dt> <dd>

Gibt den Audiostream als ganze Zahl an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt eine ganze Zahl zurück, die die Sprecherzuweisung für den angegebenen Stream angibt.



| Rückgabecode | Beschreibung                                                             |
|-------------|-------------------------------------------------------------------------|
| 2           | Der Stream wird dem linken und rechten Lautsprecher zugewiesen.                  |
| 3           | Der Stream wird dem linken, rechten und mittleren Lautsprecher zugewiesen.         |
| 4           | Der Stream wird den Sprechern links, rechts und audio1 zugewiesen.         |
| 5           | Der Stream wird dem linken, rechten, mittleren und audio1-Lautsprecher zugewiesen. |
| 6           | Der Stream wird den Sprechern links, rechts und audio2 zugewiesen.         |
| 7           | Der Stream wird dem linken, rechten, mittleren und audio2-Lautsprecher zugewiesen. |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SollaudioPresentationMode**](karaokeaudiopresentationmode-property.md)
</dt> </dl>

 

 



