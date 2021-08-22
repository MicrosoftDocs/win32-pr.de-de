---
description: Die ExpertIndicateStatus-Funktion gibt den Prozentsatz des Abschlusses der Expertenanalyse der Erfassungsdatei an.
ms.assetid: 6dbaa6d3-6068-4a28-9d9f-bcc7a25da407
title: ExpertIndicateStatus-Funktion (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertIndicateStatus
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: f9f40e339b450496ec4b0aff1f3e951c4d7468fa22f7b2ff3dd2f84de6b92354
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012268"
---
# <a name="expertindicatestatus-function"></a>ExpertIndicateStatus-Funktion

Die **ExpertIndicateStatus-Funktion** gibt den Prozentsatz des Abschlusses der Analyse der Erfassungsdatei durch den Experten an.

## <a name="syntax"></a>Syntax


```C++
DWORD WINAPI ExpertIndicateStatus(
  _In_  HEXPERTKEY              hExpertKey,
  _In_  EXPERTSTATUSENUMERATION Status,
  _In_  DWORD                   SubStatus,
  _In_  char                    *sztext,
  _Out_ long                    PercentDone
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hExpertKey* \[ In\]
</dt> <dd>

Eindeutiger Expertenbezeichner. Netzwerkmonitor *hExpertKey* an den Experten übergeben, wenn er die [Run-Funktion](run.md) aufruft.

</dd> <dt>

*Status* \[ In\]
</dt> <dd>

Aktueller Status der Analyse. Geben Sie einen der folgenden [EXPERTSTATUSENUMERATION-Werte](expertstatusenumeration.md) an.



| Wert                                                                                                                                                                                 | Bedeutung                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="EXPERTSTATUS_INACTIVE"></span><span id="expertstatus_inactive"></span><dl> <dt>**EXPERTSTATUS \_ INACTIVE**</dt> </dl> | Der Experte hat nie begonnen. <br/>                                          |
| <span id="EXPERTSTATUS_STARTING"></span><span id="expertstatus_starting"></span><dl> <dt>**EXPERTSTATUS \_ WIRD GESTARTET**</dt> </dl> | Der Experte beginnt. <br/>                                            |
| <span id="EXPERTSTATUS_RUNNING"></span><span id="expertstatus_running"></span><dl> <dt>**EXPERTSTATUS \_ WIRD AUSGEFÜHRT**</dt> </dl>    | Der Experte wird normal ausgeführt. <br/>                                    |
| <span id="EXPERTSTATUS_PROBLEM"></span><span id="expertstatus_problem"></span><dl> <dt>**\_EXPERTSTATUS-PROBLEM**</dt> </dl>    | Ein im SubStatus-Parameter angegebenes Problem hat den Experten beendet. <br/> |
| <span id="EXPERTSTATUS_ABORTED"></span><span id="expertstatus_aborted"></span><dl> <dt>**EXPERTSTATUS \_ ABGEBROCHEN**</dt> </dl>    | Netzwerkmonitor hat den Experten beendet. <br/>                                |
| <span id="EXPERTSTATUS_DONE"></span><span id="expertstatus_done"></span><dl> <dt>**EXPERTSTATUS \_ DONE**</dt> </dl>             | Der Experte hat die Analyse erfolgreich abgeschlossen. <br/>                     |



 

</dd> <dt>

*SubStatus* \[ In\]
</dt> <dd>

Erweiterung oder Erläuterung der vom *Status-Parameter bereitgestellten* Informationen.

</dd> <dt>

*sztext* \[ In\]
</dt> <dd>

Optionaler Textstatusindikator.

Dieser Parameterwert kann NULL **sein.**

</dd> <dt>

*PercentDone* \[ out\]
</dt> <dd>

Prozentsatz der Erfassungsdaten, die der Experte verarbeitet hat.

Wenn der Experte die Analyse einer Erfassungsdatei erfolgreich abgeschlossen hat, legt das System den Prozentsatz auf 100 fest. Jede Zahl, die größer als 99 ist, wird ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.

Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert NMERR EXPERT TERMINATE. Der Experte muss sofort bereinigt und zurückkehren, \_ ohne die Erfassung abschließen zu \_ müssen.

## <a name="remarks"></a>Hinweise

Die **ExpertIndicateStatus-Funktion** kann nur von Experten aufgerufen werden, die die [Exportfunktion Ausführen](run.md) [oder Konfigurieren](configure.md) implementieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |
