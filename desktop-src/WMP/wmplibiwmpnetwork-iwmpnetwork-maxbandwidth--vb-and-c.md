---
title: Iwmpnetwork MaxBandwidth (Eigenschaft)
description: Mit der MaxBandwidth-Eigenschaft wird die maximal zulässige Bandbreite abgerufen oder festgelegt.
ms.assetid: ff7548d8-b80f-4cb4-bdd6-86d585fef329
keywords:
- MaxBandwidth-Eigenschaft, Windows Media Player
- MaxBandwidth-Eigenschaft, Windows Media Player, iwmpnetwork-Schnittstelle
- Iwmpnetwork Interface, Windows Media Player, MaxBandwidth (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPNetwork.maxBandwidth
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3620d609db0f1786da673923f54d726b3c99994a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371628"
---
# <a name="iwmpnetworkmaxbandwidth-property"></a>Iwmpnetwork:: MaxBandwidth (Eigenschaft)

Mit der **MaxBandwidth** -Eigenschaft wird die maximal zulässige Bandbreite abgerufen oder festgelegt.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 maxBandwidth {get; set;}
```


```VB

Public Property maxBandwidth As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System. Int32** -Wert, der die maximale Bandbreite ist.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft hat keinen Standardwert. Der Wert kann bei der Wiedergabe von Windows Media Player angegeben werden, die Änderung wird jedoch erst wirksam, wenn das aktuelle Medien Element freigegeben wird, indem ein anderes geöffnet wird, oder durch Aufrufen von **AxWindowsMediaPlayer. Close**. Windows Media Player versucht, eine möglichst hohe Bandbreite zu erzielen. Es findet keine absichtliche Verringerung der Bandbreite statt, wenn dieser Wert festgelegt ist.

Diese Einstellung ist nützlich, um die Menge der verwendeten Bandbreite zu reduzieren, insbesondere im Fall eines MBR-Streams (Multiple Bitrate). Ein MBR-Datenstrom enthält mehrere Datenströme mit unterschiedlichen Bitraten. In einigen Fällen kann es wünschenswert sein, einen Datenstrom mit einer niedrigeren Bitrate zu verwenden, als dies für den Client erforderlich ist. Wenn Sie in diesem Fall eine niedrigere Bitrate mit der **iwmpnetwork. MaxBandwidth** -Eigenschaft angeben, wird ein niedrigerer Bitrate-Stream ausgewählt. Ein MBR-Datenstrom kann beispielsweise Datenströme enthalten, die mit 20 kbit pro Sekunde (Kbit/s), 37 Kbit/s und 200 Kbit/s codiert Wenn Sie mithilfe von **iwmpnetwork. MaxBandwidth** eine Bitrate von 50.000 (50 KBit/s) angeben, wird der Datenstrom 37 Kbit/s anstelle des Datenstroms von 200 Kbit/s ausgewählt

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer. Close (VB und c#)**](axwmplib-axwindowsmediaplayer-close.md)
</dt> <dt>

[**Iwmpnetwork-Schnittstelle (VB und c#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





