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
# <a name="winhttp-constants"></a><span data-ttu-id="fea40-103">WinHTTP-Konstanten</span><span class="sxs-lookup"><span data-stu-id="fea40-103">WinHTTP Constants</span></span>

<span data-ttu-id="fea40-104">WinHTTP verwendet die folgenden Konstanten:</span><span class="sxs-lookup"><span data-stu-id="fea40-104">WinHTTP uses the following constants:</span></span>

<dl>

<dt>

[<span data-ttu-id="fea40-105">**Fehlermeldungen**</span><span class="sxs-lookup"><span data-stu-id="fea40-105">**Error Messages**</span></span>](error-messages.md)
</dt> <dd>

<span data-ttu-id="fea40-106">Fehlermeldungen, die für die WinHTTP-Funktionen spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="fea40-106">Error messages specific to the WinHTTP functions.</span></span> <span data-ttu-id="fea40-107">Diese Funktionen geben ggf. auch Windows Fehlermeldungen zurück.</span><span class="sxs-lookup"><span data-stu-id="fea40-107">These functions also return Windows error messages where appropriate.</span></span> <span data-ttu-id="fea40-108">Der Wert, der jeder Konstante entspricht, ist der Wert der Konstante für die API-Funktionen (Application Programming Interface) und die unteren 16 Bits der Fehlernummer für das [**WinHttpRequest-Objekt.**](winhttprequest.md)</span><span class="sxs-lookup"><span data-stu-id="fea40-108">The value that corresponds to each constant is the value of the constant for the application programming interface (API) functions and the lower 16 bits of the error number for the [**WinHttpRequest**](winhttprequest.md) object.</span></span>

</dd> <dt>

[<span data-ttu-id="fea40-109">**HTTP-Statuscodes**</span><span class="sxs-lookup"><span data-stu-id="fea40-109">**HTTP Status Codes**</span></span>](http-status-codes.md)
</dt> <dd>

<span data-ttu-id="fea40-110">Konstanten und entsprechende Werte, die HTTP-Statuscodes angeben, die von Servern im Internet zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="fea40-110">Constants and corresponding values that indicate HTTP status codes returned by servers on the Internet.</span></span>

</dd> <dt>

[<span data-ttu-id="fea40-111">**Optionsflags**</span><span class="sxs-lookup"><span data-stu-id="fea40-111">**Option Flags**</span></span>](option-flags.md)
</dt> <dd>

<span data-ttu-id="fea40-112">Von [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) und [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)unterstützte Optionsflags.</span><span class="sxs-lookup"><span data-stu-id="fea40-112">Option flags supported by [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) and [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption).</span></span> <span data-ttu-id="fea40-113">Alle gültigen Optionsflags haben einen Wert größer oder gleich WINHTTP \_ FIRST OPTION und kleiner oder gleich \_ WINHTTP LAST \_ \_ OPTION.</span><span class="sxs-lookup"><span data-stu-id="fea40-113">All valid option flags have a value greater than or equal to WINHTTP\_FIRST\_OPTION and less than or equal to WINHTTP\_LAST\_OPTION.</span></span>

</dd> <dt>

[<span data-ttu-id="fea40-114">**\_INTERNETPORT**</span><span class="sxs-lookup"><span data-stu-id="fea40-114">**INTERNET\_PORT**</span></span>](internet-port.md)
</dt> <dd>

<span data-ttu-id="fea40-115">Ein WORD-Wert, der den Port angibt.</span><span class="sxs-lookup"><span data-stu-id="fea40-115">A WORD value indicating the port.</span></span>

</dd> <dt>

[<span data-ttu-id="fea40-116">**INTERNET \_ SCHEME**</span><span class="sxs-lookup"><span data-stu-id="fea40-116">**INTERNET\_SCHEME**</span></span>](internet-scheme.md)
</dt> <dd>

<span data-ttu-id="fea40-117">Von WinHTTP unterstützte Internetschemas.</span><span class="sxs-lookup"><span data-stu-id="fea40-117">Internet schemes supported by WinHTTP.</span></span>

</dd>

<dt>

[<span data-ttu-id="fea40-118">**Abfrageinformationsflags**</span><span class="sxs-lookup"><span data-stu-id="fea40-118">**Query Info Flags**</span></span>](query-info-flags.md)
</dt>
<dd>

<span data-ttu-id="fea40-119">Attribute und Modifizierer, die von [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fea40-119">Attributes and modifiers used by [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span></span>
</dd>

<dt>

<span data-ttu-id="fea40-120">**WINHTTP_EXTENDED_HEADER_FLAG_UNICODE**</span><span class="sxs-lookup"><span data-stu-id="fea40-120">**WINHTTP_EXTENDED_HEADER_FLAG_UNICODE**</span></span>
</dt>
<dd>

<span data-ttu-id="fea40-121">Hat den Wert 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="fea40-121">Has a value of 0x00000001.</span></span> <span data-ttu-id="fea40-122">Gibt [WinHttpAddRequestHeadersEx](/windows/win32/api/winhttp/nf-winhttp-winhttpaddrequestheadersex) an, dass die übergebenen Zeichenfolgen Unicode-Zeichenfolgen sind.</span><span class="sxs-lookup"><span data-stu-id="fea40-122">Indicates to [WinHttpAddRequestHeadersEx](/windows/win32/api/winhttp/nf-winhttp-winhttpaddrequestheadersex) that the strings passed in are Unicode strings.</span></span>
</dd>

<dt>

<span data-ttu-id="fea40-123">**WINHTTP_READ_DATA_EX_FLAG_FILL_BUFFER**</span><span class="sxs-lookup"><span data-stu-id="fea40-123">**WINHTTP_READ_DATA_EX_FLAG_FILL_BUFFER**</span></span>
</dt>
<dd>

<span data-ttu-id="fea40-124">Hat den Wert 0x00000000000000001ull.</span><span class="sxs-lookup"><span data-stu-id="fea40-124">Has a value of 0x0000000000000001ull.</span></span> <span data-ttu-id="fea40-125">Weist [WinHttpReadDataEx](/windows/win32/api/winhttp/nf-winhttp-winhttpreaddataex) an, den Aufruf erst abzuschließen, wenn der bereitgestellte Datenpuffer gefüllt wurde oder die Antwort abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="fea40-125">Instructs [WinHttpReadDataEx](/windows/win32/api/winhttp/nf-winhttp-winhttpreaddataex) not to complete the call until the provided data buffer has been filled, or the response is complete.</span></span> <span data-ttu-id="fea40-126">Wenn Sie dieses Flag übergeben, entspricht das Verhalten von **WinHttpReadDataEx** dem verhalten von [WinHttpReadData.](/windows/win32/api/winhttp/nf-winhttp-winhttpreaddata)</span><span class="sxs-lookup"><span data-stu-id="fea40-126">Passing this flag makes the behavior of **WinHttpReadDataEx** equivalent to that of [WinHttpReadData](/windows/win32/api/winhttp/nf-winhttp-winhttpreaddata).</span></span>
</dd>

</dl>
