---
description: 'InkCollector.NewPackets-Ereignis: Tritt auf, wenn der Ink-Collector ein Paket empfängt.'
ms.assetid: 2682e7ba-dabd-497e-aea4-6d3f837f4f10
title: InkCollector.NewPackets-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bab9d13dd2f33689700ef4a9aee2ed5059403e8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110118"
---
# <a name="inkcollectornewpackets-event"></a>InkCollector.NewPackets-Ereignis

Tritt ein, wenn der Ink-Collector ein Paket empfängt.

## <a name="syntax"></a>Syntax


```C++
void NewPackets(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in]      long           PacketCount,
  [in, out] VARIANT        *PacketData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Cursor* \[ In\]
</dt> <dd>

Das [**IInkCursor-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das das [**NewInAirPackets-Ereignis**](inkcollector-newinairpackets.md) generiert hat.

</dd> <dt>

*Strich* \[ In\]
</dt> <dd>

Gibt das [**IInkStrokeDisp-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) an.

</dd> <dt>

*PacketCount* \[ In\]
</dt> <dd>

Die Anzahl der empfangenen Pakete für ein [**IInkStrokeDisp-Objekt.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)

</dd> <dt>

*PacketData* \[ in, out\]
</dt> <dd>

Diese Methode gibt ein Array zurück, das die ausgewählten Daten für das Paket enthält.

Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der COM-Bibliothek.](using-the-com-library.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Pakete werden empfangen, während ein Strich erfasst wird. Paketereignisse treten schnell auf, und ein **NewPackets-Ereignishandler** muss schnell sein oder die Leistung beeinträchtigt werden.

Die TThis-Ereignismethode wird in den \_ \_ Dispatch-Only-Schnittstellen IInkCollectorEvents, IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ ICENewPackets definiert.

Dieses Ereignis sollte sorgfältig verwendet werden, da es negative Auswirkungen auf die Ink-Leistung haben kann, wenn zu viel Code in den Ereignishandlern ausgeführt wird.

Verwenden Sie die [**DesiredPacketDescription-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) des Ink-Collectorobjekts, um festzulegen, welche Eigenschaften in diesem Array enthalten sind. Das Array, das der *PacketData-Parameter* zurückgibt, enthält die Daten für diese Eigenschaften.

> [!Note]  
> Obwohl Sie die Paketdaten ändern können, werden diese Änderungen nicht beibehalten oder verwendet.

 

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Desktop-Apps der Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**InkCollector-Klasse**](inkcollector-class.md)
</dt> <dt>

[**NewInAirPackets-Ereignis**](inkcollector-newinairpackets.md)
</dt> <dt>

[**IInkCursor-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[**IInkStrokeDisp-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

 




