---
description: Die Funktion "Expertenstatus" gibt den Prozentsatz des Abschlusses der Expertenanalyse der Erfassungs Datei an.
ms.assetid: 6dbaa6d3-6068-4a28-9d9f-bcc7a25da407
title: Funktion "expertphestatus" (Netmon. h)
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
ms.openlocfilehash: ac707a774b667b96a4d612e9eaf7da2c779c0327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128356"
---
# <a name="expertindicatestatus-function"></a>Funktion "expertindikatestatus"

Die Funktion " **Expertenstatus** " gibt den Prozentsatz des Abschlusses der Analyse der Erfassungs Datei des Experten an.

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

*hexpertkey* \[ in\]
</dt> <dd>

Eindeutige expertenkennung. Netzwerkmonitor übergibt *hexpertkey* an den Experten, wenn die Funktion [Run](run.md) aufgerufen wird.

</dd> <dt>

*Status* \[ in\]
</dt> <dd>

Aktueller Status der Analyse. Geben Sie einen der folgenden Werte für " [Expertenstatus" umeration](expertstatusenumeration.md) an.



| Wert                                                                                                                                                                                 | Bedeutung                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="EXPERTSTATUS_INACTIVE"></span><span id="expertstatus_inactive"></span><dl> <dt>**Profil Status \_ inaktiv**</dt> </dl> | Der Experte wurde nie gestartet. <br/>                                          |
| <span id="EXPERTSTATUS_STARTING"></span><span id="expertstatus_starting"></span><dl> <dt>**Profil Status wird \_ gestartet**</dt> </dl> | Der Experte wird gestartet. <br/>                                            |
| <span id="EXPERTSTATUS_RUNNING"></span><span id="expertstatus_running"></span><dl> <dt>**Profil Status wird \_ ausgeführt**</dt> </dl>    | Der Experte wird normal ausgeführt. <br/>                                    |
| <span id="EXPERTSTATUS_PROBLEM"></span><span id="expertstatus_problem"></span><dl> <dt>**expertstatus- \_ Problem**</dt> </dl>    | Ein im unter Status Parameter angegebenes Problem hat den Experten beendet. <br/> |
| <span id="EXPERTSTATUS_ABORTED"></span><span id="expertstatus_aborted"></span><dl> <dt>**der Expertenstatus wurde \_ abgebrochen.**</dt> </dl>    | Netzwerkmonitor den Experten beendet. <br/>                                |
| <span id="EXPERTSTATUS_DONE"></span><span id="expertstatus_done"></span><dl> <dt>**Profil Status \_ abgeschlossen**</dt> </dl>             | Der Experte hat die Analyse erfolgreich abgeschlossen. <br/>                     |



 

</dd> <dt>

*Unter Status* \[ in\]
</dt> <dd>

Erweiterung oder Erläuterung der Informationen, die vom *Status* Parameter bereitgestellt werden.

</dd> <dt>

*szText* \[ in\]
</dt> <dd>

Optionaler Text Status Indikator.

Dieser Parameterwert kann **null** sein.

</dd> <dt>

*Prozentuabgeschlossen* \[ vorgenommen\]
</dt> <dd>

Der Prozentsatz der Erfassungsdaten, die der Experte verarbeitet hat.

Wenn der Experte die Analyse einer Erfassungs Datei erfolgreich abgeschlossen hat, legt das System den Prozentsatz auf 100 fest. Jede Zahl, die größer als 99 ist, wird ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Funktion nicht erfolgreich ist, wird der Rückgabewert nmerr- \_ Experte \_ beendet. der Experte muss sofort bereinigen und zurückkehren, ohne die Erfassung abzuschließen.

## <a name="remarks"></a>Bemerkungen

Die Funktion "-Funktion" kann nur von Experten aufgerufen werden **, die die** Exportfunktion " [Run](run.md) " oder " [configure](configure.md) " implementieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothek<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |
