---
title: MCI_PUT Befehl (MMSYSTEM. h)
description: Mit dem Befehl MCI \_ Put werden die Quell-, Ziel-und Frame Rechtecke festgelegt. Dieser Befehl wird von Digital Video-und Video Überlagerungs Geräten erkannt.
ms.assetid: 9d81682b-6546-4e6d-a6df-e2de8c013b66
keywords:
- MCI_PUT Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_PUT
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8fa4af30aa2b3aa6f7cdd50f453bc8edca83334
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106538"
---
# <a name="mci_put-command"></a>Befehl "MCI \_ Put"

Mit dem Befehl MCI \_ Put werden die Quell-, Ziel-und Frame Rechtecke festgelegt. Dieser Befehl wird von Digital Video-und Video Überlagerungs Geräten erkannt.

Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PUT, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpDest
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*WDE viceid*
</dt> <dd>

Geräte Bezeichner des MCI-Geräts, das die Befehls Meldung empfangen soll.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

MCI- \_ Benachrichtigung, MCI- \_ Wartezeit oder, für Digital Video-Geräte, MCI- \_ Test. Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*lpdest*
</dt> <dd>

Zeiger auf eine [**generische MCI-Struktur von \_ \_ Parametern**](mci-generic-parms.md) . (Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Die folgenden zusätzlichen Flags werden mit dem **Digitalvideo** -Gerätetyp verwendet:

<dl> <dt>

<span id="MCI_DGV_PUT_CLIENT"></span><span id="mci_dgv_put_client"></span>MCI- \_ DGV- \_ Put- \_ Client
</dt> <dd>

Das für MCI \_ DGV- \_ Rect definierte Rechteck gilt für die Position des Client Fensters. Das angegebene Rechteck ist relativ zum übergeordneten Fenster des Anzeige Fensters. Das MCI- \_ DGV- \_ Put- \_ Fenster muss gleichzeitig mit diesem Flag festgelegt werden.

</dd> <dt>

<span id="MCI_DGV_PUT_DESTINATION"></span><span id="mci_dgv_put_destination"></span>MCI- \_ DGV- \_ Put- \_ Ziel
</dt> <dd>

Das Rechteck, das für MCI \_ DGV-Rect definiert ist, \_ gibt ein Ziel Rechteck an. Das Ziel Rechteck gibt den Teil des Client Fensters an, der dieser Gerätetreiber Instanz zugeordnet ist, in der das Bild oder das Video angezeigt wird.

</dd> <dt>

<span id="MCI_DGV_PUT_FRAME"></span><span id="mci_dgv_put_frame"></span>MCI- \_ DGV- \_ Put- \_ Frame
</dt> <dd>

Das für MCI \_ DGV- \_ Rect definierte Rechteck gilt für das Frame Rechteck. Das Rahmen Rechteck gibt den Teil des Frame Puffers an, der als Ziel der Videobilder aus dem Video Rechteck verwendet wird. Das Video sollte so skaliert werden, dass es in das Frame Puffer Rechteck passt.

Das Rechteck wird in den Rahmen Puffer Koordinaten angegeben. Das Standard Rechteck ist der vollständige Frame Puffer. Das Angeben dieses Rechtecks ermöglicht dem Gerät das Skalieren des Bilds beim digitsieren der Daten. Geräte, die das Abbild nicht skalieren können, lehnen diesen Befehl mit nicht unterstützter mcierr- \_ \_ Funktion ab Sie können das Flag MCI \_ getdevcaps \_ - \_ streckungs Flag mit dem [MCI \_ getdevcaps](mci-getdevcaps.md) -Befehl verwenden, um zu bestimmen, ob ein Gerät das Image skaliert. Ein Gerät gibt **false** zurück, wenn das Abbild nicht skaliert werden kann.

</dd> <dt>

<span id="MCI_DGV_PUT_SOURCE"></span><span id="mci_dgv_put_source"></span>MCI \_ DGV \_ Put- \_ Quelle
</dt> <dd>

Das für MCI \_ DGV- \_ Rect definierte Rechteck gibt ein Quell Rechteck an. Das Quell Rechteck gibt an, welcher Teil des Frame Puffers skaliert werden soll, um in das Ziel Rechteck zu passen.

</dd> <dt>

<span id="MCI_DGV_PUT_VIDEO"></span><span id="mci_dgv_put_video"></span>MCI \_ DGV \_ Put- \_ Video
</dt> <dd>

Das für MCI \_ DGV \_ Rect definierte Rechteck gilt für das Video Rechteck. Das Video Rechteck gibt an, welcher Teil der aktuellen Präsentations Quelle im Frame Puffer gespeichert wird. Das Rechteck wird mithilfe der natürlichen Koordinaten der Präsentations Quelle angegeben. Sie ermöglicht das anschneiden, das vor dem Speichern von Bildern und Videos im Frame Puffer auftritt. Das Standard Rechteck ist der vollständige aktive Scanbereich oder die vollständigen entkomprimierten Bilder und das Video.

</dd> <dt>

<span id="MCI_DGV_PUT_WINDOW"></span><span id="mci_dgv_put_window"></span>MCI- \_ DGV- \_ Put- \_ Fenster
</dt> <dd>

Das für MCI \_ DGV- \_ Rect definierte Rechteck gilt für das Anzeige Fenster. Dieses Rechteck ist relativ zum übergeordneten Fenster des Anzeige Fensters (in der Regel der Desktop). Wenn das Fenster nicht angegeben wird, wird standardmäßig die anfängliche Fenstergröße und-Position verwendet.

</dd> <dt>

<span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI- \_ DGV- \_ Rect
</dt> <dd>

Der **RC** -Member der durch *lpdest* identifizierten Struktur enthält ein gültiges Rechteck.

</dd> </dl>

Für Digital Video-Geräte verweist *lpdest* auf eine [**MCI \_ DGV \_ Put \_**](/previous-versions//dd743397(v=vs.85)) -Struktur.

Die folgenden zusätzlichen Flags werden mit dem **Überlagerungs** Gerätetyp verwendet:

<dl> <dt>

<span id="MCI_OVLY_PUT_DESTINATION"></span><span id="mci_ovly_put_destination"></span>MCI \_ OVLY \_ - \_ Ziel
</dt> <dd>

Das für MCI \_ OVLY \_ Rect definierte Rechteck gibt den Bereich des Client Fensters an, in dem ein Bild angezeigt wird. Das Rechteck enthält den Offset und den sichtbaren Block des Bilds relativ zum Fenster Ursprung. Wenn der Frame gestreckt wird, wird die Quelle auf das Ziel Rechteck gestreckt.

</dd> <dt>

<span id="MCI_OVLY_PUT_FRAME"></span><span id="mci_ovly_put_frame"></span>MCI \_ OVLY \_ - \_ Frame
</dt> <dd>

Das für MCI \_ OVLY \_ Rect definierte Rechteck gibt den Bereich des Video Puffers an, der zum Empfangen des Video Bilds verwendet wird. Das Rechteck enthält den Offset und den Umfang des Puffer Bereichs relativ zum Video Puffer Ursprung.

</dd> <dt>

<span id="MCI_OVLY_PUT_SOURCE"></span><span id="mci_ovly_put_source"></span>MCI \_ OVLY \_ - \_ Quelle
</dt> <dd>

Das für MCI \_ OVLY \_ Rect definierte Rechteck gibt den Bereich des Video Puffers an, der als Quelle des digitalen Bilds verwendet wird. Das Rechteck enthält den Offset und den Umfang des clippingrechtecks für den Video Puffer relativ zum Ursprung.

</dd> <dt>

<span id="MCI_OVLY_PUT_VIDEO"></span><span id="mci_ovly_put_video"></span>MCI \_ OVLY \_ - \_ Video
</dt> <dd>

Das für MCI \_ OVLY \_ Rect definierte Rechteck gibt den Bereich der Videoquellen Erfassung durch den Video Puffer an. Das Rechteck enthält den Offset und den Umfang des clippingrechtecks für die Videoquelle relativ zum Ursprung.

</dd> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI \_ OVLY \_ Rect
</dt> <dd>

Der **RC** -Member der durch *lpdest* identifizierten Struktur enthält ein gültiges Anzeige Rechteck. Wenn dieses Flag nicht angegeben wird, entspricht das Standard Rechteck den Koordinaten des Video Puffers oder Fensters, das abgeschnitten wird.

</dd> </dl>

Bei Video Überlagerungs Geräten verweist *lpdest* auf eine [**MCI \_ OVLY \_ Rect \_**](mci-ovly-rect-parms.md) -Struktur.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>MMSYSTEM. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[MCI-Befehle](mci-commands.md)
</dt> </dl>

 

