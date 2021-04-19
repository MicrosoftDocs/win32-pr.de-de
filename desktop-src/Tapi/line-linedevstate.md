---
description: Die TAPI- \_ linienlinedevstate-Nachricht wird gesendet, wenn sich der Status eines Zeilen Geräts geändert hat. Die Anwendung kann linegetlinedevstatus aufrufen, um den neuen Status der Zeile zu ermitteln.
ms.assetid: 15f616de-db47-4577-9a47-94f9292253dd
title: LINE_LINEDEVSTATE Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 079e4494b7eb2e1bfe46b5470138e4e9f44fbb0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372352"
---
# <a name="line_linedevstate-message"></a>\_Linienlinedevstate-Meldung

Die TAPI **- \_ linienlinedevstate** -Nachricht wird gesendet, wenn sich der Status eines Zeilen Geräts geändert hat. Die Anwendung kann [**linegetlinedevstatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) aufrufen, um den neuen Status der Zeile zu ermitteln.


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hdevice* 
</dt> <dd>

Ein Handle für das liniengerät. Dieser Parameter ist **null** , wenn *dwParam1* linedevstate \_ REIT ist.

</dd> <dt>

*dwcallbackinstance* 
</dt> <dd>

Die beim Öffnen der Zeile angegebene Rückruf Instanz. Wenn der *dwParam1* -Parameter linedevstate \_ REIT ist, ist der *dwcallbackinstance* -Parameter ungültig und auf 0 (null) festgelegt.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Das Element des Zeilen Gerätestatus, das geändert wurde. Der-Parameter kann eine oder mehrere der [**linedevstate- \_ Konstanten**](linedevstate--constants.md)sein.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Die Interpretation dieses Parameters hängt vom Wert von *dwParam1* ab. Wenn *dwParam1* ein linedevstate- \_ Klingeln ist, enthält *dwParam2* den Ring Modus, mit dem der Schalter die Zeile an den Ring anweist. Gültige ringmodi sind Zahlen im Bereich von 1 bis **dwnumringmodi**, wobei **dwnumringmodes** eine Linien Geräte Funktion ist.

Wenn *dwParam1* "linedevstate" ist \_ und die Meldung von TAPI als Ergebnis der Übersetzung einer neuen API-Nachricht in eine REIT-Nachricht ausgegeben wurde, enthält *dwParam2* den *dwmsg* -Parameter der ursprünglichen Nachricht (z. b. [**line \_ Create**](line-create.md) oder line \_ linedevstate). Wenn *dwParam2* NULL ist, weist dies darauf hin, dass die REIT-Nachricht eine "Real"-REIT-Nachricht ist, die erfordert, dass die Anwendung [**LineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown) zu dem frühestmöglichen Zweck aufruft.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Die Interpretation dieses Parameters hängt vom Wert von *dwParam1* ab. Wenn *dwParam1* ein linedevstate- \_ Klingeln ist, enthält *dwParam3* die Ring Anzahl für dieses Ring Ereignis. Die Ring Anzahl beginnt bei 0 (null).

Wenn *dwParam1* linedevstate \_ REIT ist, und die Nachricht wurde von TAPI als Ergebnis der Übersetzung einer neuen API-Nachricht in eine REIT-Nachricht ausgegeben. anschließend enthält *dwParam3* den *dwParam1* -Parameter der ursprünglichen Nachricht (z. b. linedevstate \_ translatechange oder einen anderen Wert von linedevstate \_ , wenn *dwParam2* line \_ linedevstate ist, oder der neue Geräte Bezeichner, wenn *dwParam2* [**line \_ Create**](line-create.md)ist).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Das Senden der **\_ linienlinedevstate** -Nachricht kann mit [**linesetstatusmessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)gesteuert werden. Eine Anwendung kann Status Element Änderungen anzeigen, über die Sie benachrichtigt werden möchten. Standardmäßig ist die gesamte Status Berichterstattung deaktiviert, mit Ausnahme von linedevstate \_ , die nicht deaktiviert werden kann. Diese Nachricht wird an alle Anwendungen gesendet, die über ein Handle für die Zeile verfügen, einschließlich derjenigen, die [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) aufgerufen haben, wobei der *dwprivileges* -Parameter auf linecallprivilege \_ None, linecallprivilege \_ Owner, linecallprivilege \_ Monitor oder zulässige Kombinationen von diesen festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Zeilen \_ Schließen**](line-close.md)
</dt> <dt>

[**Zeilen \_ Erstellung**](line-create.md)
</dt> <dt>

[**Linedevcaps**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[**linegetdevcaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)
</dt> <dt>

[**linegetdevconfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)
</dt> <dt>

[**linegettranslatecaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)
</dt> <dt>

[**lineinitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[**linesetstatus-Meldungen**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)
</dt> <dt>

[**LineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> <dt>

[**Linetranslatecaps**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps)
</dt> <dt>

[**lineuncompletecall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall)
</dt> </dl>

 

 




