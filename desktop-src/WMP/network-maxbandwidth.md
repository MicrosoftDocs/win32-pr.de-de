---
title: Network. MaxBandwidth
description: Die MaxBandwidth-Eigenschaft gibt die maximal zulässige Bandbreite an oder ruft Sie ab.
ms.assetid: 303acf51-8d3a-4e58-8aa8-c0b6db1e4fbb
keywords:
- Windows Media Player "Network. MaxBandwidth"
topic_type:
- apiref
api_name:
- Network.maxBandwidth
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cbe8283c4cc756a4f88fad1240df3a757b53a2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365171"
---
# <a name="networkmaxbandwidth"></a>Network. MaxBandwidth

Die **MaxBandwidth** -Eigenschaft gibt die maximal zulässige Bandbreite an oder ruft Sie ab.

## <a name="syntax"></a>Syntax

*Player*. *Netzwerk*. **MaxBandwidth**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine Lese-/schreibzahl (**Long**). 

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft hat keinen Standardwert. Der Wert kann bei der Wiedergabe von Windows-Media Player angegeben werden, die Änderung wird jedoch erst wirksam, wenn das aktuelle Medien Element durch Öffnen eines weiteren oder durch Aufrufen von *Player* freigegeben wird. **Schließen** Sie. Windows Media Player versucht, eine möglichst hohe Bandbreite zu erzielen. Nur wenn der Wert festgelegt wird, wird die Bandbreiten Reduzierung durchgesetzt.

Diese Einstellung ist nützlich, um die Menge der verwendeten Bandbreite zu reduzieren, insbesondere im Fall eines MBR-Streams (Multiple Bitrate). Ein MBR-Datenstrom enthält mehrere Datenströme mit unterschiedlichen Bitraten. In einigen Fällen kann es wünschenswert sein, einen Datenstrom mit einer niedrigeren Bitrate zu verwenden, als dies für den Client erforderlich ist. Wenn Sie in diesem Fall die **MaxBandwidth** -Eigenschaft festlegen, wird ein niedrigerer Bitrate-Stream ausgewählt.

Ein MBR-Datenstrom könnte beispielsweise Datenströme enthalten, die mit 20 kbit pro Sekunde (Kbit/s), 37 Kbit/s und 200 Kbit/s codiert Wenn Sie die **MaxBandwidth** -Eigenschaft auf 50.000 (50 KBit/s) festlegen, wird der Datenstrom 37 Kbit/s anstelle des Datenstroms der Größe 200 (

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Netzwerk Objekt**](network-object.md)
</dt> <dt>

[**Player. Close**](player-close.md)
</dt> </dl>

 

 





