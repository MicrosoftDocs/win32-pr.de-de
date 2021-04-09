---
title: MCI_WHERE Befehl (MMSYSTEM. h)
description: Der Befehl "MCI where" ruft \_ das Clippingrechteck für das Videogerät ab.
ms.assetid: f64a7e49-4ee1-4836-ba9a-0bbdc47626b3
keywords:
- MCI_WHERE Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_WHERE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6619131319863d1159a3bdb8bb85d366243544a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956526"
---
# <a name="mci_where-command"></a>Befehl "MCI \_ where"

Der Befehl "MCI where" ruft \_ das Clippingrechteck für das Videogerät ab. Dieser Befehl wird von Digital Video-und Video Überlagerungs Geräten erkannt. Die **oberen** und **linken** Elemente der zurückgegebenen [Rect](/previous-versions//ms536136(v=vs.85)) enthalten den Ursprung des clippingrechtecks, und die **Rechte** und **unteren** Elemente enthalten die Breite und Höhe des clippingrechtecks. (Dies ist nicht die Standardverwendung des **rechten** und **unteren** Members.)

Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_WHERE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpQuery
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

<span id="lpQuery"></span><span id="lpquery"></span><span id="LPQUERY"></span>*lpquery*
</dt> <dd>

Zeiger auf eine [**generische MCI-Struktur von \_ \_ Parametern**](mci-generic-parms.md) . (Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Die folgenden zusätzlichen Flags werden mit dem **Digitalvideo** -Gerätetyp verwendet:

<dl> <dt>

<span id="MCI_DGV_WHERE_DESTINATION"></span><span id="mci_dgv_where_destination"></span>MCI \_ DGV \_ ( \_ Ziel)
</dt> <dd>

Ruft eine Beschreibung des rechteckigen Bereichs ab, der zum Anzeigen von Videos und Bildern im Client Bereich des aktuellen Fensters verwendet wird.

</dd> <dt>

<span id="MCI_DGV_WHERE_FRAME"></span><span id="mci_dgv_where_frame"></span>MCI \_ DGV, \_ wobei \_ Frame
</dt> <dd>

Ruft eine Beschreibung des rechteckigen Bereichs des Frame Puffers ab, in den Bilder aus dem Video Rechteck skaliert werden. Die Rechteck Koordinaten werden in den **RC** -Member der durch *lpquery* identifizierten Struktur platziert.

</dd> <dt>

<span id="MCI_DGV_WHERE_MAX"></span><span id="mci_dgv_where_max"></span>MCI \_ DGV \_ ( \_ Max.)
</dt> <dd>

Bei Verwendung mit MCI \_ DGV \_ Where \_ Destination oder MCI \_ DGV \_ Where \_ Source gibt das zurückgegebene Rechteck die maximale Breite und Höhe des angegebenen Bereichs an. Bei Verwendung mit MCI \_ DGV \_ Where \_ Window gibt das zurückgegebene Rechteck die Größe der gesamten Anzeige an.

</dd> <dt>

<span id="MCI_DGV_WHERE_SOURCE"></span><span id="mci_dgv_where_source"></span>MCI \_ DGV, \_ wobei \_ Quelle
</dt> <dd>

Ruft eine Beschreibung des rechteckigen Bereichs ab (aus dem Frame Puffer abgeleitet), der gestreckt wird, um das Ziel Rechteck auf der Anzeige zu erfüllen.

</dd> <dt>

<span id="MCI_DGV_WHERE_VIDEO"></span><span id="mci_dgv_where_video"></span>MCI- \_ DGV- \_ \_ Video
</dt> <dd>

Ruft eine Beschreibung des rechteckigen Bereichs ab, der von der Präsentations Quelle zum Ausfüllen des Frame Rechtecks im Frame Puffer abgeschnitten wurde. Die Rechteck Koordinaten werden in den **RC** -Member der durch *lpquery* identifizierten Struktur platziert.

</dd> <dt>

<span id="MCI_DGV_WHERE_WINDOW"></span><span id="mci_dgv_where_window"></span>MCI \_ DGV \_ Where- \_ Fenster
</dt> <dd>

Ruft eine Beschreibung des Anzeige Fensterrahmens ab.

</dd> <dt>


</dt> <dd></dd> </dl>

Für Digital Video-Geräte zeigt der *lpquery* -Parameter auf eine **MCI- \_ DGV \_ \_** -Struktur, in der die Parameter Struktur enthalten ist. Die MCI-DGV-Struktur, bei der die Struktur von **\_ \_ \_ Parametern** mit der Struktur des [**MCI- \_ DGV- \_ \_ para**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms) Metern identisch ist.

Die folgenden zusätzlichen Flags werden mit dem **Überlagerungs** Gerätetyp verwendet:

<dl> <dt>

<span id="MCI_OVLY_WHERE_DESTINATION"></span><span id="mci_ovly_where_destination"></span>MCI \_ OVLY \_ Where- \_ Ziel
</dt> <dd>

Ruft das Zielanzeige Rechteck ab. Die Rechteck Koordinaten werden in den **RC** -Member der durch *lpquery* identifizierten Struktur platziert.

</dd> <dt>

<span id="MCI_OVLY_WHERE_FRAME"></span><span id="mci_ovly_where_frame"></span>MCI \_ OVLY, \_ wobei \_ Frame
</dt> <dd>

Ruft das Überlagerungs Rahmen Rechteck ab. Die Rechteck Koordinaten werden in den **RC** -Member der durch *lpquery* identifizierten Struktur platziert.

</dd> <dt>

<span id="MCI_OVLY_WHERE_SOURCE"></span><span id="mci_ovly_where_source"></span>MCI \_ OVLY \_ Where \_ Source
</dt> <dd>

Ruft das Quell Rechteck ab. Die Rechteck Koordinaten werden in den **RC** -Member der durch *lpquery* identifizierten Struktur platziert.

</dd> <dt>

<span id="MCI_OVLY_WHERE_VIDEO"></span><span id="mci_ovly_where_video"></span>MCI \_ OVLY \_ Where- \_ Video
</dt> <dd>

Ruft das Video Rechteck ab. Die Rechteck Koordinaten werden in den **RC** -Member der durch *lpquery* identifizierten Struktur platziert.

</dd> </dl>

Bei Video Überlagerungs Geräten zeigt der *lpquery* -Parameter auf eine [**MCI \_ OVLY \_ Rect \_**](mci-ovly-rect-parms.md) -Parameter Struktur.

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

 

