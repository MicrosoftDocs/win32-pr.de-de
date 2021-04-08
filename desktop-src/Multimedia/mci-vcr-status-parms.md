---
title: MCI_VCR_STATUS_PARMS Struktur (VCR. h)
description: Die Struktur der MCI- \_ VCR- \_ Status \_ Parameter enthält Parameter für den MCI- \_ Status Befehl für Video-Kassetten-Recorder.
ms.assetid: 5d7cbb64-a81d-4bdd-8f07-8c20dd7b9ef5
keywords:
- MCI_VCR_STATUS_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_STATUS_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0b197acfa0e170a9ab199cd6d6c51a64e14c320
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949485"
---
# <a name="mci_vcr_status_parms-structure"></a>Struktur des MCI \_ VCR- \_ Status \_ Parametern

Die Struktur der **MCI- \_ VCR- \_ Status \_** Parameter enthält Parameter für den [**MCI- \_ Status**](mci-status.md) Befehl für Video-Kassetten-Recorder.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMCI_VCR_STATUS_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwReturn;
  DWORD     dwItem;
  DWORD     dwTrack;
  DWORD     dwNumber;
} MCI_VCR_STATUS_PARMS;
```



## <a name="members"></a>Member

<dl> <dt>

**dwcallback**
</dt> <dd>

Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .

</dd> <dt>

**dwreturn**
</dt> <dd>

Wert, der vom [**MCI- \_ Status**](mci-status.md) Befehl zurückgegeben wird. Der Rückgabewert variiert je nach Abfrage des Befehls. Weitere Informationen finden Sie in der Beschreibung des Befehls " [**MCI- \_ Status**](mci-status-parms.md) ".

</dd> <dt>

**dwitem**
</dt> <dd>

Der Typ der angeforderten Informationen.

</dd> <dt>

**dwtrack**
</dt> <dd>

Audiobild oder Videotitel, das Informationen während der nächsten Aufzeichnung speichert. Dieser Member wird verwendet, um Informationen zurückzugeben, wenn der [**MCI- \_ Status**](mci-status-parms.md) Befehl den Video-oder audioaufzeichnungs Status fragt.

</dd> <dt>

**dwnumber**
</dt> <dd>

Logischer Tuner, dem der aktuelle Channel zugeordnet ist. Dieser Member wird verwendet, um Informationen zurückzugeben, wenn der [**MCI- \_ Status**](mci-status.md) Befehl die aktuelle Channelnummer fragt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VCR. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**MCI-Strukturen**](mci-structures.md)
</dt> <dt>

[**MCI- \_ Status**](mci-status.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

