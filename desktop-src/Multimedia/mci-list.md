---
title: MCI_LIST Befehl (MMSYSTEM. h)
description: Der MCI \_ -Listen Befehl ruft Informationen über die Anzahl und die Typen der Eingaben ab, die für das Gerät verfügbar sind. Dieser Befehl wird von Digital-Video-und VCR-Geräten erkannt.
ms.assetid: 1977fbfa-cae4-4afe-9fc5-ac68177574ca
keywords:
- MCI_LIST Befehl Windows-Multimedia
topic_type:
- apiref
api_name:
- MCI_LIST
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15d5a616085028132c83fd71c46f7d409bf48a14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519037"
---
# <a name="mci_list-command"></a>MCI- \_ Listen Befehl

Der MCI \_ -Listen Befehl ruft Informationen über die Anzahl und die Typen der Eingaben ab, die für das Gerät verfügbar sind. Dieser Befehl wird von Digital-Video-und VCR-Geräten erkannt.

Um diesen Befehl zu senden, wenden Sie die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion mit den folgenden Parametern an.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_LIST, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpList
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

MCI- \_ Benachrichtigung, MCI- \_ Wartezeit oder MCI- \_ Test. Weitere Informationen zu diesen Flags finden Sie [unter Wait-, notify-und testflags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpList"></span><span id="lplist"></span><span id="LPLIST"></span>*lplist*
</dt> <dd>

Zeiger auf eine [**generische MCI-Struktur von \_ \_ Parametern**](mci-generic-parms.md) . (Geräte mit erweiterten Befehlssätzen können diese Struktur durch eine gerätespezifische Struktur ersetzen.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls einen Fehler.

## <a name="remarks"></a>Bemerkungen

Die folgenden zusätzlichen Flags gelten für den **Digitalvideo** -Gerätetyp:

<dl> <dt>

<span id="MCI_DGV_LIST_ALG"></span><span id="mci_dgv_list_alg"></span>MCI \_ DGV \_ List \_ alg
</dt> <dd>

Der **lpstrinalgorithmus** -Member der durch *lplist* identifizierten Struktur enthält eine Adresse eines Puffers, der den Namen eines Algorithmus enthält. Der Name wird verwendet, um die einem Algorithmus zugeordneten Typen von Qualitäts Deskriptoren abzurufen.

</dd> <dt>

<span id="MCI_DGV_LIST_COUNT"></span><span id="mci_dgv_list_count"></span>MCI- \_ DGV- \_ Listen \_ Anzahl
</dt> <dd>

Gibt die Anzahl der Optionen des angegebenen Typs zurück.

</dd> <dt>

<span id="MCI_DGV_LIST_ITEM"></span><span id="mci_dgv_list_item"></span>MCI- \_ DGV- \_ Listen \_ Element
</dt> <dd>

Eine-Konstante, die angibt, dass der Listentyp im **dwitem** -Member der durch *lplist* identifizierten-Struktur enthalten ist. Dieses Flag ist erforderlich. Verwenden Sie eine der folgenden Konstanten, um den Auflistungstyp anzugeben:

</dd> <dt>

<span id="MCI_DGV_LIST_AUDIO_ALG"></span><span id="mci_dgv_list_audio_alg"></span>MCI \_ DGV \_ \_ -Liste Audio- \_ alg
</dt> <dd>

Der Befehl sollte Namen von audioalgorithmen abrufen.

</dd> <dt>

<span id="MCI_DGV_LIST_AUDIO_QUALITY"></span><span id="mci_dgv_list_audio_quality"></span>MCI \_ DGV \_ \_ -Liste \_ Audioqualität
</dt> <dd>

Der Befehl sollte audioqualitätsgrade abrufen. Die zurückgegebenen Ebenen werden dem Algorithmus zugeordnet, auf den der **lpstrinalgorithmus** -Member der durch *lplist* bezeichneten Struktur verweist. Wenn dieser Member mithilfe der Zeichenfolge "Current" angegeben wird, werden die dem aktuellen Algorithmus zugeordneten Qualitäten zurückgegeben.

</dd> <dt>

<span id="MCI_DGV_LIST_AUDIO_STREAM"></span><span id="mci_dgv_list_audio_stream"></span>MCI \_ \_ -DGV \_ -Listen-Audiodatenstrom \_
</dt> <dd>

Der Befehl sollte Namen von Audiodatenströmen abrufen.

</dd> <dt>

<span id="MCI_DGV_LIST_STILL_AL"></span><span id="mci_dgv_list_still_al"></span>MCI- \_ DGV- \_ Liste \_ immer noch \_ Al
</dt> <dd>

Der Befehl sollte Namen von immer noch Algorithmen abrufen.

</dd> <dt>

<span id="MCI_DGV_LIST_STILL_QUALITY"></span><span id="mci_dgv_list_still_quality"></span>MCI- \_ DGV- \_ Liste \_ immer noch \_ Qualität
</dt> <dd>

Der Befehl sollte Qualitätsstufen abrufen. Die zurückgegebenen Ebenen werden dem Algorithmus zugeordnet, auf den der **lpstrinalgorithmus** -Member der durch *lplist* bezeichneten Struktur verweist. Wenn dieser Member mithilfe der Zeichenfolge "Current" angegeben wird, werden die dem aktuellen Algorithmus zugeordneten Qualitäten zurückgegeben.

</dd> <dt>

<span id="MCI_DGV_LIST_VIDEO_ALG"></span><span id="mci_dgv_list_video_alg"></span>MCI- \_ DGV- \_ Liste \_ Video- \_ alg
</dt> <dd>

Der Befehl sollte Namen von Video Algorithmen abrufen.

</dd> <dt>

<span id="MCI_DGV_LIST_VIDEO_QUALITY"></span><span id="mci_dgv_list_video_quality"></span>MCI- \_ DGV- \_ Listen \_ Video \_ Qualität
</dt> <dd>

Der Befehl sollte Video Qualitäts Ebenen abrufen. Die zurückgegebenen Ebenen werden dem Algorithmus zugeordnet, auf den der **lpstrinalgorithmus** -Member der durch *lplist* bezeichneten Struktur verweist. Wenn dieser Member mithilfe der Zeichenfolge "Current" angegeben wird, werden die dem aktuellen Algorithmus zugeordneten Qualitäten zurückgegeben.

</dd> <dt>

<span id="MCI_DGV_LIST_VIDEO_SOURCE"></span><span id="mci_dgv_list_video_source"></span>MCI- \_ DGV- \_ Liste ( \_ Video \_ Quelle)
</dt> <dd>

Der Befehl sollte Informationen zu den Videoquellen zurückgeben. Bei Verwendung mit der MCI- \_ DGV- \_ Listen Anzahl \_ gibt der Befehl die Anzahl der Videoquellen zurück. Bei Verwendung mit der MCI- \_ DGV- \_ Listen \_ Nummer gibt der Befehl den Typ einer Videoquelle zurück. MCI definiert die folgenden Typen:

-   MCI \_ DGV \_ setvideo \_ src \_ generic
-   MCI \_ DGV \_ setvideo \_ src \_ NTSC
-   MCI \_ DGV \_ setvideo \_ src \_ PAL
-   MCI \_ DGV \_ setvideo \_ src \_ RGB
-   MCI \_ DGV \_ setvideo \_ src \_ SECAM
-   MCI \_ DGV \_ setvideo \_ src \_ SVideo

Möglicherweise gibt es mehrere Quellen für jeden Typ, die zurückgegeben werden. Der generische Quelltyp wird verwendet, wenn mehr als ein Typ von Signal für diesen Connector zulässig ist.

</dd> <dt>

<span id="MCI_DGV_LIST_VIDEO_STREAM"></span><span id="mci_dgv_list_video_stream"></span>MCI- \_ DGV- \_ Listen \_ \_ Videostream
</dt> <dd>

Der Befehl sollte Namen von Videostreams abrufen.

</dd> <dt>

<span id="MCI_DGV_LIST_NUMBER"></span><span id="mci_dgv_list_number"></span>MCI- \_ DGV- \_ Listen \_ Nummer
</dt> <dd>

Ein Index wird im **dwnumber** -Member der durch *lplist* identifizierten Struktur angegeben. Der Index muss eine ganze Zahl zwischen 1 und dem Wert sein, der für das MCI- \_ DGV- \_ Listen Anzahl-Flag zurückgegeben wird \_ .

</dd> </dl>

Für Digital Video-Geräte verweist die *lplist* auf eine [**MCI- \_ DGV- \_ Listen \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_list_parmsa) -Elementstruktur.

Die folgenden zusätzlichen Flags gelten für den **VCR** -Gerätetyp:

<dl> <dt>

<span id="MCI_VCR_LIST_AUDIO_SOURCE"></span><span id="mci_vcr_list_audio_source"></span>Audioquelle für MCI \_ VCR \_ \_ -Liste \_
</dt> <dd>

Listet Audioeingaben oder-Typen auf.

</dd> <dt>

<span id="MCI_VCR_LIST_COUNT"></span><span id="mci_vcr_list_count"></span>Anzahl der MCI- \_ VCR- \_ Listen \_
</dt> <dd>

Legt den **dwreturn** -Member der von *lplist* identifizierten-Struktur auf die Gesamtzahl von Video-oder Audioeingaben fest.

</dd> <dt>

<span id="MCI_VCR_LIST_NUMBER"></span><span id="mci_vcr_list_number"></span>MCI- \_ VCR- \_ Listen \_ Nummer
</dt> <dd>

Legt den **dwreturn** -Member der durch *lplist* identifizierten Struktur auf den Typ der Video-oder Audioeingabe fest, die vom **dwnumber** -Member angegeben wird.

</dd> <dt>

<span id="MCI_VCR_LIST_VIDEO_SOURCE"></span><span id="mci_vcr_list_video_source"></span>Video Quelle für MCI \_ VCR- \_ Liste \_ \_
</dt> <dd>

Listet Videoeingaben oder-Typen auf.

</dd> </dl>

Bei VCR-Geräten verweist *lplist* auf eine [**MCI- \_ VCR- \_ Listen \_**](mci-vcr-list-parms.md) -Element-Struktur.

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

 

