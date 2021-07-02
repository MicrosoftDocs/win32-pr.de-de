---
description: In diesem Thema werden die Konstanten identifiziert, die von WinHTTP verwendet werden.
ms.assetid: 460f1463-57a8-47eb-9957-17976757bd7f
title: WinHTTP-Konstanten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e37b0e4de7aa3df5e155933bea2be25386c1637
ms.sourcegitcommit: 8e3d8594fa073a9c43eb5dcc7babea03ea30f10f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2021
ms.locfileid: "113175005"
---
# <a name="winhttp-constants"></a>WinHTTP-Konstanten

WinHTTP verwendet die folgenden Konstanten:

<dl>

<dt>

[**Fehlermeldungen**](error-messages.md)
</dt> <dd>

Fehlermeldungen, die für die WinHTTP-Funktionen spezifisch sind. Diese Funktionen geben ggf. auch Windows Fehlermeldungen zurück. Der Wert, der jeder Konstante entspricht, ist der Wert der Konstante für die API-Funktionen (Application Programming Interface) und die unteren 16 Bits der Fehlernummer für das [**WinHttpRequest-Objekt.**](winhttprequest.md)

</dd> <dt>

[**HTTP-Statuscodes**](http-status-codes.md)
</dt> <dd>

Konstanten und entsprechende Werte, die HTTP-Statuscodes angeben, die von Servern im Internet zurückgegeben werden.

</dd> <dt>

[**Optionsflags**](option-flags.md)
</dt> <dd>

Von [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) und [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)unterstützte Optionsflags. Alle gültigen Optionsflags haben einen Wert größer oder gleich WINHTTP \_ FIRST OPTION und kleiner oder gleich \_ WINHTTP LAST \_ \_ OPTION.

</dd> <dt>

[**\_INTERNETPORT**](internet-port.md)
</dt> <dd>

Ein WORD-Wert, der den Port angibt.

</dd> <dt>

[**INTERNET \_ SCHEME**](internet-scheme.md)
</dt> <dd>

Von WinHTTP unterstützte Internetschemas.

</dd>

<dt>

[**Abfrageinformationsflags**](query-info-flags.md)
</dt>
<dd>

Attribute und Modifizierer, die von [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)verwendet werden.
</dd>

<dt>

**WINHTTP_EXTENDED_HEADER_FLAG_UNICODE**
</dt>
<dd>

Hat den Wert 0x00000001. Gibt [WinHttpAddRequestHeadersEx](/windows/win32/api/winhttp/nf-winhttp-winhttpaddrequestheadersex) an, dass die übergebenen Zeichenfolgen Unicode-Zeichenfolgen sind.
</dd>

<dt>

**WINHTTP_READ_DATA_EX_FLAG_FILL_BUFFER**
</dt>
<dd>

Hat den Wert 0x00000000000000001ull. Weist [WinHttpReadDataEx](/windows/win32/api/winhttp/nf-winhttp-winhttpreaddataex) an, den Aufruf erst abzuschließen, wenn der bereitgestellte Datenpuffer gefüllt wurde oder die Antwort abgeschlossen ist. Wenn Sie dieses Flag übergeben, entspricht das Verhalten von **WinHttpReadDataEx** dem verhalten von [WinHttpReadData.](/windows/win32/api/winhttp/nf-winhttp-winhttpreaddata)
</dd>

</dl>
