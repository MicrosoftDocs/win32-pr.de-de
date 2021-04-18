---
description: Die lineinitializeexoption- \_ Konstanten geben an, welcher Ereignis Benachrichtigungs Mechanismus beim Initialisieren einer Sitzung verwendet werden soll.
ms.assetid: 77674a45-7133-4518-af47-a9d58392b80b
title: LINEINITIALIZEEXOPTION_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86543c367877d74562cc0af13261881b7df19982
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371460"
---
# <a name="lineinitializeexoption_-constants"></a>Lineinitializeexoption- \_ Konstanten

Die **lineinitializeexoption \_** -Konstanten geben an, welcher Ereignis Benachrichtigungs Mechanismus beim Initialisieren einer Sitzung verwendet werden soll.

<dl> <dt>

<span id="LINEINITIALIZEEXOPTION_CALLHUBTRACKING"></span><span id="lineinitializeexoption_callhubtracking"></span>**lineinitializeexoption \_ callhubtracking**
</dt> <dd> <dl> <dt>



Die Anwendung möchte den Ereignis Benachrichtigungs Mechanismus für den callhub-Nachverfolgung verwenden. Diese Konstante ist nur für Anwendungen verfügbar, die eine TAPI-Version von 3,0 oder höher aushandeln.


</dt> </dl> </dd> <dt>

<span id="LINEINITIALIZEEXOPTION_USECOMPLETIONPORT"></span><span id="lineinitializeexoption_usecompletionport"></span>**lineinitializeexoption \_ usecompletionport**
</dt> <dd> <dl> <dt>



Die Anwendung möchte den Ereignis Benachrichtigungs Mechanismus für den Abschluss Port verwenden. Dieses Flag ist nur für Anwendungen verfügbar, die eine TAPI-Version von 2,0 oder höher aushandeln.


</dt> </dl> </dd> <dt>

<span id="LINEINITIALIZEEXOPTION_USEEVENT"></span><span id="lineinitializeexoption_useevent"></span>**lineinitializeexoption \_ useevent**
</dt> <dd> <dl> <dt>



Die Anwendung möchte den Ereignis Benachrichtigungs Mechanismus Ereignishandler verwenden. Dieses Flag ist nur für Anwendungen verfügbar, die eine TAPI-Version von 2,0 oder höher aushandeln.


</dt> </dl> </dd> <dt>

<span id="LINEINITIALIZEEXOPTION_USEHIDDENWINDOW"></span><span id="lineinitializeexoption_usehiddenwindow"></span>**lineinitializeexoption \_ usehiddenwindow**
</dt> <dd> <dl> <dt>



Die Anwendung möchte den Ereignis Benachrichtigungs Mechanismus für ausgeblendete Fenster verwenden. Dieses Flag ist nur für Anwendungen verfügbar, die eine TAPI-Version von 2,0 oder höher aushandeln.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Weitere Informationen zum Betrieb dieser Optionen finden Sie unter [**lineinitializeex**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




