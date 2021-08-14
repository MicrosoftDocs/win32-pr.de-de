---
description: 'InkOverlay.NewInAirPackets-Ereignis: Tritt auf, wenn ein In-Air-Paket erkannt wird.'
ms.assetid: 10dc1909-bfbc-4ea0-b77a-e33149205107
title: InkOverlay.NewInAirPackets-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7198fe2d105421654bfba037049e46a592d603bd94409350e97b794882ab4de2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118219168"
---
# <a name="inkoverlaynewinairpackets-event"></a>InkOverlay.NewInAirPackets-Ereignis

Tritt ein, wenn ein In-Air-Paket erkannt wird.

## <a name="syntax"></a>Syntax


```C++
void NewInAirPackets(
  [in]      IInkCursor *Cursor,
  [in]      long       PacketCount,
  [in, out] VARIANT    *PacketData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Cursor* \[ In\]
</dt> <dd>

Das [**IInkCursor-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das das [**NewInAirPackets-Ereignis**](inkcollector-newinairpackets.md) generiert hat.

</dd> <dt>

*PacketCount* \[ In\]
</dt> <dd>

Die Anzahl der empfangenen In-Air-Pakete.

</dd> <dt>

*PacketData* \[ in, out\]
</dt> <dd>

Ein Array, das die ausgewählten Daten für das Paket enthält.

Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der COM-Bibliothek.](using-the-com-library.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Ein In-Air-Paket wird erstellt, wenn ein Benutzer einen Stift in der Nähe des Tabletts verschiebt und sich der Cursor im Fenster des Freihandsammlerobjekts befindet oder der Benutzer eine Maus innerhalb des zugeordneten Fensters des Freihandsammlerobjekts bewegt. [**NewInAirPackets-Ereignisse**](inkcollector-newinairpackets.md) werden schnell generiert, und der Ereignishandler muss schnell sein oder die Leistung beeinträchtigt werden.

Diese Ereignismethode wird in den \_ \_ Dispatch-Only-Schnittstellen IInkCollectorEvents, IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ ICENewInAirPackets definiert.

Das [**NewInAirPackets-Ereignis**](inkcollector-newinairpackets.md) wird ausgelöst, auch wenn sie sich im Auswahl- oder Löschmodus befinden, nicht nur beim Einfügen von Ink. Dies erfordert, dass Sie den Bearbeitungsmodus überwachen (den Sie festlegen müssen) und den Modus kennen, bevor Sie das Ereignis interpretieren. Der Vorteil dieser Anforderung ist eine größere Innovationsfähigkeit auf der Plattform durch ein höheres Bewusstsein für Plattformereignisse.

Verwenden Sie die [**DesiredPacketDescription-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) des Ink-Collectorobjekts, um festzulegen, welche Eigenschaften in diesem Array enthalten sind. Das Array, das der *PacketData-Parameter* zurückgibt, enthält die Daten für diese Eigenschaften.

> [!Note]  
> Obwohl Sie die Paketdaten ändern können, werden diese Änderungen nicht beibehalten oder verwendet.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**InkOverlay-Klasse**](inkoverlay-class.md)
</dt> <dt>

[**DesiredPacketDescription-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription)
</dt> <dt>

[**NewPackets-Ereignis**](inkcollector-newpackets.md)
</dt> <dt>

[**IInkCursor-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




