---
title: MCI_LIST Befehl (Mmsystem.h)
description: Der Befehl MCI LIST erhält Informationen über die Anzahl und die \_ Typen von Eingaben, die für das Gerät verfügbar sind. Digital-Video- und VCR-Geräte erkennen diesen Befehl.
ms.assetid: 1977fbfa-cae4-4afe-9fc5-ac68177574ca
keywords:
- MCI_LIST-Befehl Windows Multimedia
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
ms.openlocfilehash: f9bd3aa35875791d6fa916d9d6831bdcb83a6db43be6e5859ce582243606f666
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138636"
---
# <a name="mci_list-command"></a>MCI \_ LIST-Befehl

Der Befehl MCI LIST erhält Informationen über die Anzahl und die \_ Typen von Eingaben, die für das Gerät verfügbar sind. Digital-Video- und VCR-Geräte erkennen diesen Befehl.

Um diesen Befehl zu senden, rufen Sie die [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) mit den folgenden Parametern auf.


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

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*
</dt> <dd>

Gerätebezeichner des MCI-Geräts, das die Befehlsnachricht empfangen soll.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI \_ WAIT oder MCI \_ TEST. Informationen zu diesen Flags finden Sie unter [Die Warte-, Benachrichtigungs- und Testflags](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpList"></span><span id="lplist"></span><span id="LPLIST"></span>*lpList*
</dt> <dd>

Zeiger auf eine [**MCI \_ GENERIC \_ PARMS-Struktur.**](mci-generic-parms.md) (Geräte mit erweiterten Befehlssätzen ersetzen diese Struktur möglicherweise durch eine gerätespezifische Struktur.)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn erfolgreich, andernfalls ein Fehler.

## <a name="remarks"></a>Hinweise

Die folgenden zusätzlichen Flags gelten für den **DigitalVideo-Gerätetyp:**

<dl> <dt>

<span id="MCI_DGV_LIST_ALG"></span><span id="mci_dgv_list_alg"></span>MCI \_ DGV \_ LIST \_ ALG
</dt> <dd>

Das **lpstrAlgorithm-Member** der durch *lpList* identifizierten Struktur enthält eine Adresse eines Puffers, der den Namen eines Algorithmus enthält. Der Name wird verwendet, um die Einem Algorithmus zugeordneten Typen von Qualitätsdeskriptoren abzurufen.

</dd> <dt>

<span id="MCI_DGV_LIST_COUNT"></span><span id="mci_dgv_list_count"></span>MCI \_ DGV \_ LIST \_ COUNT
</dt> <dd>

Gibt die Anzahl der Optionen des angegebenen Typs zurück.

</dd> <dt>

<span id="MCI_DGV_LIST_ITEM"></span><span id="mci_dgv_list_item"></span>MCI \_ \_ DGV-LISTENELEMENT \_
</dt> <dd>

Eine Konstante, die den Listentyp angibt, ist im **dwItem-Member** der struktur enthalten, die durch *lpList identifiziert wird.* Dieses Flag ist erforderlich. Verwenden Sie eine der folgenden Konstanten, um den Listentyp anzugeben:

</dd> <dt>

<span id="MCI_DGV_LIST_AUDIO_ALG"></span><span id="mci_dgv_list_audio_alg"></span>MCI \_ DGV \_ LIST \_ AUDIO \_ ALG
</dt> <dd>

Der Befehl sollte Namen von Audioalgorithmen abrufen.

</dd> <dt>

<span id="MCI_DGV_LIST_AUDIO_QUALITY"></span><span id="mci_dgv_list_audio_quality"></span>MCI \_ DGV \_ LIST \_ AUDIO \_ QUALITY
</dt> <dd>

Der Befehl sollte Audioqualitätsstufen abrufen. Die zurückgegebenen Ebenen sind dem Algorithmus zugeordnet, auf den das **lpstrAlgorithm-Member** der durch lpList identifizierten *Struktur verweist.* Wenn dieser Member mit der Zeichenfolge "current" angegeben wird, werden die dem aktuellen Algorithmus zugeordneten Qualitäten zurückgegeben.

</dd> <dt>

<span id="MCI_DGV_LIST_AUDIO_STREAM"></span><span id="mci_dgv_list_audio_stream"></span>MCI \_ DGV \_ LIST \_ AUDIO \_ STREAM
</dt> <dd>

Der Befehl sollte Namen von Audiostreams abrufen.

</dd> <dt>

<span id="MCI_DGV_LIST_STILL_AL"></span><span id="mci_dgv_list_still_al"></span>MCI \_ DGV \_ LIST \_ STILL \_ AL
</dt> <dd>

Der Befehl sollte Namen von still-Algorithmen abrufen.

</dd> <dt>

<span id="MCI_DGV_LIST_STILL_QUALITY"></span><span id="mci_dgv_list_still_quality"></span>MCI \_ DGV \_ LIST \_ STILL \_ QUALITY
</dt> <dd>

Der Befehl sollte Qualitätsstufen abrufen. Die zurückgegebenen Ebenen sind dem Algorithmus zugeordnet, auf den das **lpstrAlgorithm-Member** der durch lpList identifizierten *Struktur verweist.* Wenn dieser Member mit der Zeichenfolge "current" angegeben wird, werden die dem aktuellen Algorithmus zugeordneten Qualitäten zurückgegeben.

</dd> <dt>

<span id="MCI_DGV_LIST_VIDEO_ALG"></span><span id="mci_dgv_list_video_alg"></span>MCI \_ DGV \_ LIST \_ VIDEO \_ ALG
</dt> <dd>

Der Befehl sollte Die Namen von Videoalgorithmen abrufen.

</dd> <dt>

<span id="MCI_DGV_LIST_VIDEO_QUALITY"></span><span id="mci_dgv_list_video_quality"></span>MCI \_ DGV \_ LIST \_ VIDEO \_ QUALITY
</dt> <dd>

Der Befehl sollte Videoqualitätsstufen abrufen. Die zurückgegebenen Ebenen sind dem Algorithmus zugeordnet, auf den das **lpstrAlgorithm-Member** der durch lpList identifizierten *Struktur verweist.* Wenn dieser Member mit der Zeichenfolge "current" angegeben wird, werden die dem aktuellen Algorithmus zugeordneten Qualitäten zurückgegeben.

</dd> <dt>

<span id="MCI_DGV_LIST_VIDEO_SOURCE"></span><span id="mci_dgv_list_video_source"></span>MCI \_ DGV \_ LIST \_ VIDEO \_ SOURCE
</dt> <dd>

Der Befehl sollte Informationen zu den Videoquellen zurückgeben. Bei Verwendung mit MCI \_ DGV \_ LIST COUNT gibt der Befehl die Anzahl der \_ Videoquellen zurück. Bei Verwendung mit MCI \_ DGV \_ LIST NUMBER gibt der Befehl den Typ einer \_ Videoquelle zurück. MCI definiert die folgenden Typen:

-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ GENERIC
-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ NTSC
-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ PAL
-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ RGB
-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ SECAM
-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ SVIDEO

Es kann mehrere Quellen für jeden zurückgegebenen Typ geben. Der generische Quelltyp wird verwendet, wenn mehr als ein Signaltyp für diesen Connector zulässig ist.

</dd> <dt>

<span id="MCI_DGV_LIST_VIDEO_STREAM"></span><span id="mci_dgv_list_video_stream"></span>MCI \_ DGV \_ LIST \_ VIDEO \_ STREAM
</dt> <dd>

Der Befehl sollte Die Namen von Videostreams abrufen.

</dd> <dt>

<span id="MCI_DGV_LIST_NUMBER"></span><span id="mci_dgv_list_number"></span>MCI \_ \_ DGV-LISTENNUMMER \_
</dt> <dd>

Ein Index wird im **dwNumber-Member** der struktur angegeben, die durch *lpList identifiziert wird.* Der Index muss eine ganze Zahl zwischen 1 und dem Wert sein, der für das MCI \_ DGV \_ LIST \_ COUNT-Flag zurückgegeben wird.

</dd> </dl>

Für Digitalvideogeräte verweist *lpList* auf eine [**MCI \_ DGV \_ LIST \_ PARMS-Struktur.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_list_parmsa)

Die folgenden zusätzlichen Flags gelten für den **vcr-Gerätetyp:**

<dl> <dt>

<span id="MCI_VCR_LIST_AUDIO_SOURCE"></span><span id="mci_vcr_list_audio_source"></span>MCI \_ VCR \_ LIST \_ AUDIO \_ SOURCE
</dt> <dd>

Auflisten von Audioeingaben oder -typen.

</dd> <dt>

<span id="MCI_VCR_LIST_COUNT"></span><span id="mci_vcr_list_count"></span>ANZAHL DER \_ MCI-VCR-LISTEN \_ \_
</dt> <dd>

Legt das **dwReturn-Member** der durch *lpList* identifizierten Struktur auf die Gesamtzahl der Video- oder Audioeingaben fest.

</dd> <dt>

<span id="MCI_VCR_LIST_NUMBER"></span><span id="mci_vcr_list_number"></span>MCI \_ \_ VCR-LISTENNUMMER \_
</dt> <dd>

Legt den **dwReturn-Member** der durch *lpList* identifizierten Struktur auf den Typ der Video- oder Audioeingabe fest, die vom **dwNumber-Member angegeben** wird.

</dd> <dt>

<span id="MCI_VCR_LIST_VIDEO_SOURCE"></span><span id="mci_vcr_list_video_source"></span>VIDEOQUELLE \_ DER MCI-VCR-LISTE \_ \_ \_
</dt> <dd>

Auflisten von Videoeingaben oder -typen

</dd> </dl>

Für VCR-Geräte *verweist lpList* auf eine [**MCI \_ VCR \_ LIST \_ PARMS-Struktur.**](mci-vcr-list-parms.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Mmsystem.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[MCI-Befehle](mci-commands.md)
</dt> </dl>

 

