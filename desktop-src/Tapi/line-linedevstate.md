---
description: Die TAPI LINE \_ LINEDEVSTATE-Nachricht wird gesendet, wenn sich der Zustand eines Zeilengeräts geändert hat. Die Anwendung kann lineGetLineDevStatus aufrufen, um den neuen Status der Zeile zu bestimmen.
ms.assetid: 15f616de-db47-4577-9a47-94f9292253dd
title: LINE_LINEDEVSTATE Meldung (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 261e7527354b84801437e48ffc13ba4dbad60ced0cca61be65eb96ce6417bb10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682387"
---
# <a name="line_linedevstate-message"></a>LINE \_ LINEDEVSTATE-Meldung

Die TAPI **LINE \_ LINEDEVSTATE-Nachricht** wird gesendet, wenn sich der Zustand eines Zeilengeräts geändert hat. Die Anwendung kann [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus) aufrufen, um den neuen Status der Zeile zu bestimmen.


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hDevice* 
</dt> <dd>

Ein Handle für das Zeilengerät. Dieser Parameter ist **NULL,** wenn *dwParam1* LINEDEVSTATE \_ REINIT ist.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Die Rückrufinstanz, die beim Öffnen der Zeile angegeben wird. Wenn der *dwParam1-Parameter* LINEDEVSTATE \_ REINIT ist, ist der *dwCallbackInstance-Parameter* ungültig und auf 0 (null) festgelegt.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Das Gerätestatuselement der Zeile, das geändert wurde. Der Parameter kann eine oder mehrere der [**LINEDEVSTATE-Konstanten \_ sein.**](linedevstate--constants.md)

</dd> <dt>

*dwParam2* 
</dt> <dd>

Die Interpretation dieses Parameters hängt vom Wert von *dwParam1* ab. Wenn *dwParam1* LINEDEVSTATE \_ RINGING ist, enthält *dwParam2* den Ringmodus, mit dem der Schalter die Zeile anweist, zu ringen. Gültige Ringmodi sind Zahlen im Bereich 1 bis **dwNumRingModes,** wobei **dwNumRingModes** eine Gerätefunktion für Linien ist.

Wenn *dwParam1* LINEDEVSTATE REINIT ist \_ und die Nachricht von TAPI als Ergebnis der Übersetzung einer neuen API-Nachricht in eine REINIT-Nachricht ausgegeben wurde, enthält *dwParam2* den *dwMsg-Parameter* der ursprünglichen Nachricht (z. B. [**LINE \_ CREATE**](line-create.md) oder LINE \_ LINEDEVSTATE). Wenn *dwParam2* 0 (null) ist, bedeutet dies, dass die REINIT-Nachricht eine "echte" REINIT-Nachricht ist, die erfordert, dass die Anwendung [**"lineShutdown"**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown) möglichst schnell aufruft.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Die Interpretation dieses Parameters hängt vom Wert von *dwParam1* ab. Wenn *dwParam1* LINEDEVSTATE \_ RINGING ist, enthält *dwParam3* die Ringanzahl für dieses Ringereignis. Die Ringanzahl beginnt bei 0 (null).

Wenn *dwParam1* LINEDEVSTATE REINIT ist \_ und die Nachricht durch TAPI als Ergebnis der Übersetzung einer neuen API-Nachricht in eine REINIT-Nachricht ausgegeben wurde, enthält dwParam3 den *dwParam1-Parameter* der ursprünglichen Nachricht (z. B. LINEDEVSTATE  \_ TRANSLATECHANGE oder einen anderen LINEDEVSTATE-Wert, \_ wenn *dwParam2* LINE \_ LINEDEVSTATE ist, oder den neuen Gerätebezeichner, wenn *dwParam2* [**LINE \_ CREATE**](line-create.md)ist).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Das Senden der **\_ LINEDEVSTATE-Nachricht** kann mit [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)gesteuert werden. Eine Anwendung kann Statuselementänderungen angeben, über die sie benachrichtigt werden soll. Standardmäßig ist alle Statusberichte deaktiviert, mit Ausnahme von LINEDEVSTATE \_ REINIT, die nicht deaktiviert werden können. Diese Meldung wird an alle Anwendungen gesendet, die über ein Handle für die Zeile verfügen, einschließlich der Anwendungen, die [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) aufgerufen haben, wobei der *dwPrivileges-Parameter* auf LINECALLPRIVILEGE \_ NONE, LINECALLPRIVILEGE \_ OWNER, LINECALLPRIVILEGE MONITOR oder zulässige Kombinationen dieser Parameter festgelegt \_ ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LINE \_ CLOSE**](line-close.md)
</dt> <dt>

[**LINE \_ CREATE**](line-create.md)
</dt> <dt>

[**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)
</dt> <dt>

[**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)
</dt> <dt>

[**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)
</dt> <dt>

[**lineInitialize**](/windows/desktop/api/Tapi/nf-tapi-lineinitialize)
</dt> <dt>

[**lineÖffnen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)
</dt> <dt>

[**lineShutdown**](/windows/desktop/api/Tapi/nf-tapi-lineshutdown)
</dt> <dt>

[**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps)
</dt> <dt>

[**lineUncompleteCall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall)
</dt> </dl>

 

 




