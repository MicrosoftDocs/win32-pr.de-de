---
description: 'InkOverlay.NewInAirPackets-Ereignis: Tritt auf, wenn ein In-Air-Paket gesehen wird.'
ms.assetid: 10dc1909-bfbc-4ea0-b77a-e33149205107
title: InkOverlay.NewInAirPackets-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f39e568941b1af0727ad9c8464913325409b4604
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086708"
---
# <a name="inkoverlaynewinairpackets-event"></a>InkOverlay.NewInAirPackets-Ereignis

Tritt ein, wenn ein In-Air-Paket gesehen wird.

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

Das [**IInkCursor-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) das das [**NewInAirPackets-Ereignis generiert**](inkcollector-newinairpackets.md) hat.

</dd> <dt>

*PacketCount* \[ In\]
</dt> <dd>

Die Anzahl der empfangenen In-Air-Pakete.

</dd> <dt>

*PacketData* \[ in, out\]
</dt> <dd>

Ein Array, das die ausgewählten Daten für das Paket enthält.

Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der COM-Bibliothek](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Ein In-Air-Paket wird erstellt, wenn ein Benutzer einen Stift in die Nähe des Tablets verschiebt und sich der Cursor im Fenster des Freiformsammlerobjekts befindet oder der Benutzer eine Maus im zugeordneten Fenster des Freiformsammlerobjekts bewegt. [**NewInAirPackets-Ereignisse**](inkcollector-newinairpackets.md) werden schnell generiert, und der Ereignishandler muss schnell sein oder die Leistung beeinträchtigen.

Diese Ereignismethode wird in den \_ Dispatch-Schnittstellen IInkCollectorEvents, \_ IInkOverlayEvents und \_ IInkPictureEvents (dispinterfaces) mit der ID DISPID \_ ICENewInAirPackets definiert.

Das [**NewInAirPackets-Ereignis**](inkcollector-newinairpackets.md) wird auch dann ausgelöst, wenn es sich im Auswahl- oder Löschmodus befindet, nicht nur beim Einfügen von Ink. Dies erfordert, dass Sie den Bearbeitungsmodus überwachen (den Sie festlegen müssen) und den Modus kennen, bevor Sie das Ereignis interpretieren. Der Vorteil dieser Anforderung ist eine größere Innovationsfähigkeit auf der Plattform durch ein größeres Bewusstsein für Plattformereignisse.

Verwenden Sie zum Festlegen der in diesem Array enthaltenen Eigenschaften die [**DesiredPacketDescription-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) des Ink-Collectorobjekts. Das Array, das der *PacketData-Parameter* zurückgibt, enthält die Daten für diese Eigenschaften.

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

[**InkOverlay-Klasse**](inkoverlay-class.md)
</dt> <dt>

[**DesiredPacketDescription-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription)
</dt> <dt>

[**NewPackets-Ereignis**](inkcollector-newpackets.md)
</dt> <dt>

[**IInkCursor-Schnittstelle**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




