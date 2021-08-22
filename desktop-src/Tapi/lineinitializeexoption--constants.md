---
description: Die LINEINITIALIZEEXOPTION-Konstanten geben an, welcher \_ Ereignisbenachrichtigungsmechanismus beim Initialisieren einer Sitzung verwendet werden soll.
ms.assetid: 77674a45-7133-4518-af47-a9d58392b80b
title: LINEINITIALIZEEXOPTION_ Konstanten (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e92a1df7c4ea88cad126dcf5b542dbbdc33704814518dbc79cdf5d6bff5da402
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073040"
---
# <a name="lineinitializeexoption_-constants"></a>LINEINITIALIZEEXOPTION-Konstanten \_

Die **LINEINITIALIZEEXOPTION-Konstanten \_** geben an, welcher Ereignisbenachrichtigungsmechanismus beim Initialisieren einer Sitzung verwendet werden soll.

<dl> <dt>

<span id="LINEINITIALIZEEXOPTION_CALLHUBTRACKING"></span><span id="lineinitializeexoption_callhubtracking"></span>**LINEINITIALIZEEXOPTION \_ CALLHUBTRACKING**
</dt> <dd> <dl> <dt>



Die Anwendung möchte den Mechanismus zum Nachverfolgen von Anrufhub-Ereignisbenachrichtigungen verwenden. Diese Konstante wird nur für Anwendungen verfügbar gemacht, die eine TAPI-Version von 3.0 oder höher aushandeln.


</dt> </dl> </dd> <dt>

<span id="LINEINITIALIZEEXOPTION_USECOMPLETIONPORT"></span><span id="lineinitializeexoption_usecompletionport"></span>**LINEINITIALIZEEXOPTION \_ USECOMPLETIONPORT**
</dt> <dd> <dl> <dt>



Die Anwendung möchte den Ereignisbenachrichtigungsmechanismus Abschlussport verwenden. Dieses Flag wird nur für Anwendungen verfügbar gemacht, die eine TAPI-Version von 2.0 oder höher aushandeln.


</dt> </dl> </dd> <dt>

<span id="LINEINITIALIZEEXOPTION_USEEVENT"></span><span id="lineinitializeexoption_useevent"></span>**LINEINITIALIZEEXOPTION \_ USEEVENT**
</dt> <dd> <dl> <dt>



Die Anwendung möchte den Ereignisbenachrichtigungsmechanismus Ereignishand handle verwenden. Dieses Flag wird nur für Anwendungen verfügbar gemacht, die eine TAPI-Version von 2.0 oder höher aushandeln.


</dt> </dl> </dd> <dt>

<span id="LINEINITIALIZEEXOPTION_USEHIDDENWINDOW"></span><span id="lineinitializeexoption_usehiddenwindow"></span>**LINEINITIALIZEEXOPTION \_ USEHIDDENWINDOW**
</dt> <dd> <dl> <dt>



Die Anwendung möchte den Ereignisbenachrichtigungsmechanismus ausgeblendeter Fenster verwenden. Dieses Flag wird nur für Anwendungen verfügbar gemacht, die eine TAPI-Version von 2.0 oder höher aushandeln.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Weitere Informationen zum Betrieb dieser Optionen finden Sie unter [**lineInitializeEx.**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




