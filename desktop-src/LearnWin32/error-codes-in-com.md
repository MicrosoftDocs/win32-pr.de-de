---
title: Fehlercodes in COM
description: Fehlercodes in COM
ms.assetid: ed430863-f416-4611-81b4-0c31d819944a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 733cbe0799a22b0f0c01ee9cb226ad7e0b8660da
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103958"
---
# <a name="error-codes-in-com"></a><span data-ttu-id="3759a-103">Fehlercodes in COM</span><span class="sxs-lookup"><span data-stu-id="3759a-103">Error Codes in COM</span></span>

<span data-ttu-id="3759a-104">Com-Methoden und -Funktionen geben einen Wert vom Typ **HRESULT** zurück, um einen Erfolg oder Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="3759a-104">To indicate success or failure, COM methods and functions return a value of type **HRESULT**.</span></span> <span data-ttu-id="3759a-105">Ein **HRESULT** ist eine 32-Bit-Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="3759a-105">An **HRESULT** is a 32-bit integer.</span></span> <span data-ttu-id="3759a-106">Das hochgeordnete Bit des **HRESULT** signalisiert Erfolg oder Fehler.</span><span class="sxs-lookup"><span data-stu-id="3759a-106">The high-order bit of the **HRESULT** signals success or failure.</span></span> <span data-ttu-id="3759a-107">Null (0) gibt den Erfolg an, und 1 gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="3759a-107">Zero (0) indicates success and 1 indicates failure.</span></span>

<span data-ttu-id="3759a-108">Dadurch werden die folgenden numerischen Bereiche erzeugt:</span><span class="sxs-lookup"><span data-stu-id="3759a-108">This produces the following numeric ranges:</span></span>

-   <span data-ttu-id="3759a-109">Erfolgscodes: 0x0-0x7FFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="3759a-109">Success codes: 0x0–0x7FFFFFFF.</span></span>
-   <span data-ttu-id="3759a-110">Fehlercodes: 0x80000000–0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="3759a-110">Error codes: 0x80000000–0xFFFFFFFF.</span></span>

<span data-ttu-id="3759a-111">Eine kleine Anzahl von COM-Methoden gibt keinen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="3759a-111">A small number of COM methods do not return an **HRESULT** value.</span></span> <span data-ttu-id="3759a-112">Beispielsweise geben die [**Methoden AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) und [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) lange Werte ohne Vorzeichen zurück.</span><span class="sxs-lookup"><span data-stu-id="3759a-112">For example, the [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) and [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) methods return unsigned long values.</span></span> <span data-ttu-id="3759a-113">Jede COM-Methode, die einen Fehlercode zurückgibt, gibt jedoch einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="3759a-113">But every COM method that returns an error code does so by returning an **HRESULT** value.</span></span>

<span data-ttu-id="3759a-114">Um zu überprüfen, ob eine COM-Methode erfolgreich ist, untersuchen Sie das obere Bit des zurückgegebenen **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="3759a-114">To check whether a COM method succeeds, examine the high-order bit of the returned **HRESULT**.</span></span> <span data-ttu-id="3759a-115">Die Windows SDK-Header stellen zwei Makros bereit, die dies vereinfachen: das [**SUCCEEDED-Makro**](/windows/desktop/api/winerror/nf-winerror-succeeded) und das [**FAILED-Makro.**](/windows/desktop/api/winerror/nf-winerror-failed)</span><span class="sxs-lookup"><span data-stu-id="3759a-115">The Windows SDK headers provide two macros that make this easier: the [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) macro and the [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) macro.</span></span> <span data-ttu-id="3759a-116">Das **SUCCEEDED-Makro** gibt **TRUE** zurück, wenn ein **HRESULT** ein Erfolgscode ist, und **FALSE,** wenn es sich um einen Fehlercode handelt.</span><span class="sxs-lookup"><span data-stu-id="3759a-116">The **SUCCEEDED** macro returns **TRUE** if an **HRESULT** is a success code and **FALSE** if it is an error code.</span></span> <span data-ttu-id="3759a-117">Im folgenden Beispiel wird überprüft, ob [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="3759a-117">The following example checks whether [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) succeeds.</span></span>


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
    COINIT_DISABLE_OLE1DDE);

if (SUCCEEDED(hr))
{
    // The function succeeded.
}
else
{
    // Handle the error.
}
```



<span data-ttu-id="3759a-118">Manchmal ist es praktischer, die umgekehrte Bedingung zu testen.</span><span class="sxs-lookup"><span data-stu-id="3759a-118">Sometimes it is more convenient to test the inverse condition.</span></span> <span data-ttu-id="3759a-119">Das [**FAILED-Makro**](/windows/desktop/api/winerror/nf-winerror-failed) führt das Gegenteil von [**SUCCEEDED aus.**](/windows/desktop/api/winerror/nf-winerror-succeeded)</span><span class="sxs-lookup"><span data-stu-id="3759a-119">The [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) macro does the opposite of [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded).</span></span> <span data-ttu-id="3759a-120">Sie gibt **TRUE** für einen Fehlercode und **FALSE** für einen Erfolgscode zurück.</span><span class="sxs-lookup"><span data-stu-id="3759a-120">It returns **TRUE** for an error code and **FALSE** for a success code.</span></span>


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
    COINIT_DISABLE_OLE1DDE);

if (FAILED(hr))
{
    // Handle the error.
}
else
{
    // The function succeeded.
}
```



<span data-ttu-id="3759a-121">Später in diesem Modul werden einige praktische Hinweise zur Strukturierung Ihres Codes zur Handhabung von COM-Fehlern behandelt.</span><span class="sxs-lookup"><span data-stu-id="3759a-121">Later in this module, we will look at some practical advice for how to structure your code to handle COM errors.</span></span> <span data-ttu-id="3759a-122">(Siehe [Fehlerbehandlung in COM](error-handling-in-com.md).)</span><span class="sxs-lookup"><span data-stu-id="3759a-122">(See [Error Handling in COM](error-handling-in-com.md).)</span></span>

## <a name="next"></a><span data-ttu-id="3759a-123">Nächste</span><span class="sxs-lookup"><span data-stu-id="3759a-123">Next</span></span>

[<span data-ttu-id="3759a-124">Erstellen eines Objekts in COM</span><span class="sxs-lookup"><span data-stu-id="3759a-124">Creating an Object in COM</span></span>](creating-an-object-in-com.md)

 

 
