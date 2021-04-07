---
title: Fehler Codes in com
description: .
ms.assetid: ed430863-f416-4611-81b4-0c31d819944a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f082afbabf367179b02c0fb3b0fc979dcda664a4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725385"
---
# <a name="error-codes-in-com"></a><span data-ttu-id="f4460-103">Fehler Codes in com</span><span class="sxs-lookup"><span data-stu-id="f4460-103">Error Codes in COM</span></span>

<span data-ttu-id="f4460-104">Um den Erfolg oder Misserfolg anzuzeigen, geben com-Methoden und-Funktionen einen Wert vom Typ **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="f4460-104">To indicate success or failure, COM methods and functions return a value of type **HRESULT**.</span></span> <span data-ttu-id="f4460-105">Ein **HRESULT** ist eine 32-Bit-Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="f4460-105">An **HRESULT** is a 32-bit integer.</span></span> <span data-ttu-id="f4460-106">Das höchst wertige Bit des **HRESULT** signalisiert Erfolg oder Fehler.</span><span class="sxs-lookup"><span data-stu-id="f4460-106">The high-order bit of the **HRESULT** signals success or failure.</span></span> <span data-ttu-id="f4460-107">NULL (0) gibt den Erfolg an, und 1 gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="f4460-107">Zero (0) indicates success and 1 indicates failure.</span></span>

<span data-ttu-id="f4460-108">Dies erzeugt die folgenden numerischen Bereiche:</span><span class="sxs-lookup"><span data-stu-id="f4460-108">This produces the following numeric ranges:</span></span>

-   <span data-ttu-id="f4460-109">Erfolgs Codes: 0x0 – 0x7FFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="f4460-109">Success codes: 0x0–0x7FFFFFFF.</span></span>
-   <span data-ttu-id="f4460-110">Fehlercodes: 0x80000000 – 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="f4460-110">Error codes: 0x80000000–0xFFFFFFFF.</span></span>

<span data-ttu-id="f4460-111">Eine kleine Anzahl von com-Methoden gibt keinen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f4460-111">A small number of COM methods do not return an **HRESULT** value.</span></span> <span data-ttu-id="f4460-112">Beispielsweise geben die Methoden " [**adressf**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) " und " [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) " nicht signierte Long-Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="f4460-112">For example, the [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) and [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) methods return unsigned long values.</span></span> <span data-ttu-id="f4460-113">Jede com-Methode, die einen Fehlercode zurückgibt, bewirkt jedoch, dass ein **HRESULT** -Wert zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f4460-113">But every COM method that returns an error code does so by returning an **HRESULT** value.</span></span>

<span data-ttu-id="f4460-114">Um zu überprüfen, ob eine com-Methode erfolgreich ist, überprüfen Sie das höchst wertige Bit des zurückgegebenen **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f4460-114">To check whether a COM method succeeds, examine the high-order bit of the returned **HRESULT**.</span></span> <span data-ttu-id="f4460-115">Die Windows SDK-Header bieten zwei Makros, die dies vereinfachen: das Makro " [**erfolgreich**](/windows/desktop/api/winerror/nf-winerror-succeeded) " und das [**fehlgeschlagene**](/windows/desktop/api/winerror/nf-winerror-failed) Makro.</span><span class="sxs-lookup"><span data-stu-id="f4460-115">The Windows SDK headers provide two macros that make this easier: the [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) macro and the [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) macro.</span></span> <span data-ttu-id="f4460-116">Das Makro " **erfolgreich** " gibt **true** zurück, wenn ein **HRESULT** ein Erfolgs Code ist, und **false** , wenn es sich um einen Fehlercode handelt.</span><span class="sxs-lookup"><span data-stu-id="f4460-116">The **SUCCEEDED** macro returns **TRUE** if an **HRESULT** is a success code and **FALSE** if it is an error code.</span></span> <span data-ttu-id="f4460-117">Im folgenden Beispiel wird überprüft, ob [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="f4460-117">The following example checks whether [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) succeeds.</span></span>


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



<span data-ttu-id="f4460-118">Manchmal ist es bequemer, die umgekehrte Bedingung zu testen.</span><span class="sxs-lookup"><span data-stu-id="f4460-118">Sometimes it is more convenient to test the inverse condition.</span></span> <span data-ttu-id="f4460-119">Das [**fehlgeschlagene**](/windows/desktop/api/winerror/nf-winerror-failed) Makro bewirkt, dass das Gegenteil von [**erfolgreich war**](/windows/desktop/api/winerror/nf-winerror-succeeded).</span><span class="sxs-lookup"><span data-stu-id="f4460-119">The [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) macro does the opposite of [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded).</span></span> <span data-ttu-id="f4460-120">Sie gibt **true** für einen Fehlercode und **false** für einen Erfolgs Code zurück.</span><span class="sxs-lookup"><span data-stu-id="f4460-120">It returns **TRUE** for an error code and **FALSE** for a success code.</span></span>


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



<span data-ttu-id="f4460-121">Später in diesem Modul betrachten wir einige praktische Ratschläge, wie Sie Ihren Code für die Behandlung von com-Fehlern strukturieren.</span><span class="sxs-lookup"><span data-stu-id="f4460-121">Later in this module, we will look at some practical advice for how to structure your code to handle COM errors.</span></span> <span data-ttu-id="f4460-122">(Siehe [Fehlerbehandlung in com](error-handling-in-com.md).)</span><span class="sxs-lookup"><span data-stu-id="f4460-122">(See [Error Handling in COM](error-handling-in-com.md).)</span></span>

## <a name="next"></a><span data-ttu-id="f4460-123">Nächste</span><span class="sxs-lookup"><span data-stu-id="f4460-123">Next</span></span>

[<span data-ttu-id="f4460-124">Erstellen eines Objekts in com</span><span class="sxs-lookup"><span data-stu-id="f4460-124">Creating an Object in COM</span></span>](creating-an-object-in-com.md)

 

 