---
title: MCI_VCR_STATUS_PARMS -Struktur (Vcr.h)
description: Die MCI \_ VCR STATUS PARMS-Struktur enthält Parameter für den \_ \_ MCI \_ STATUS-Befehl für Video-Cassette-Aufzeichnungen.
ms.assetid: 5d7cbb64-a81d-4bdd-8f07-8c20dd7b9ef5
keywords:
- MCI_VCR_STATUS_PARMS-Struktur Windows Multimedia
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
ms.openlocfilehash: 8569a278f697ed816085c4fc8f313502d2994215519fb2452f82e63ce31a80cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783920"
---
# <a name="mci_vcr_status_parms-structure"></a>MCI \_ VCR \_ STATUS \_ PARMS-Struktur

Die **MCI \_ VCR \_ STATUS \_ PARMS-Struktur** enthält Parameter für den [**MCI \_ STATUS-Befehl**](mci-status.md) für Video-Cassette-Aufzeichnungen.

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

**dwCallback**
</dt> <dd>

Das Wort mit niedriger Reihenfolge gibt ein Fensterhand handle an, das für das MCI \_ NOTIFY-Flag verwendet wird.

</dd> <dt>

**dwReturn**
</dt> <dd>

Der vom [**MCI-Befehl \_ STATUS zurückgegebene**](mci-status.md) Wert. Der Rückgabewert variiert je nach Abfrage des Befehls. Weitere Informationen finden Sie in der Beschreibung des [**Befehls MCI \_ STATUS.**](mci-status-parms.md)

</dd> <dt>

**dwItem**
</dt> <dd>

Typ der angeforderten Informationen.

</dd> <dt>

**dwTrack**
</dt> <dd>

Audio- oder Videospur, in der Informationen während der nächsten Aufzeichnung gespeichert werden. Dieser Member wird verwendet, um Informationen zurück zu geben, wenn der [**\_ MCI-Befehl STATUS**](mci-status-parms.md) den Status der Video- oder Audioaufzeichnung abfragt.

</dd> <dt>

**dwNumber**
</dt> <dd>

Logischer Tuner, dem der aktuelle Kanal zugeordnet ist. Dieses Member wird verwendet, um Informationen zurück zu geben, wenn der [**\_ MCI-Befehl STATUS**](mci-status.md) die aktuelle Kanalnummer anfragt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Legen Sie beim Zuweisen von Daten zu den Membern dieser Struktur die entsprechenden Flags im *fdwCommand-Parameter* der [**mciSendCommand-Funktion**](/previous-versions//dd757160(v=vs.85)) fest, um die Member zu überprüfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>Vcr.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Mci**](mci.md)
</dt> <dt>

[**MCI-Strukturen**](mci-structures.md)
</dt> <dt>

[**\_MCI-STATUS**](mci-status.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

