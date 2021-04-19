---
description: Die showjavaconsole-Funktion ist eine Debughilfe für Java-Entwickler. Applets (oder anderer Java-Code), die in Internet Explorer ausgeführt werden, können diese zum Anzeigen von Fehlermeldungen und anderen Informationen verwenden.
ms.assetid: 070dd833-f8cc-403e-afbf-325648760d5f
title: Showjavaconsole-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- extern
api_type:
- DllExport
api_location:
- Msjava.dll
ms.openlocfilehash: 522885bfdd07843549375977630d8d1a7c6776f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361921"
---
# <a name="showjavaconsole-function"></a><span data-ttu-id="e1121-104">Showjavaconsole-Funktion</span><span class="sxs-lookup"><span data-stu-id="e1121-104">ShowJavaConsole function</span></span>

<span data-ttu-id="e1121-105">Die **showjavaconsole** -Funktion ist eine Debughilfe für Java-Entwickler.</span><span class="sxs-lookup"><span data-stu-id="e1121-105">The **ShowJavaConsole** function is a debugging aid for Java developers.</span></span> <span data-ttu-id="e1121-106">Applets (oder anderer Java-Code), die in Internet Explorer ausgeführt werden, können diese zum Anzeigen von Fehlermeldungen und anderen Informationen verwenden.</span><span class="sxs-lookup"><span data-stu-id="e1121-106">Applets (or other Java code) running within Internet Explorer can use it to display error messages and other information.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1121-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1121-107">Syntax</span></span>


```C++
void extern ShowJavaConsole(void);
```



## <a name="parameters"></a><span data-ttu-id="e1121-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1121-108">Parameters</span></span>

<span data-ttu-id="e1121-109">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="e1121-109">This function has no parameters.</span></span>

<dl></dl>

## <a name="return-value"></a><span data-ttu-id="e1121-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e1121-110">Return value</span></span>

<span data-ttu-id="e1121-111">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e1121-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1121-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e1121-112">Remarks</span></span>

<span data-ttu-id="e1121-113">Wenn Sie **showjavaconsole** aufrufen, zeigt der Java Virtual Machine (VM) das Java-Konsolenfenster an.</span><span class="sxs-lookup"><span data-stu-id="e1121-113">Calling **ShowJavaConsole** causes the Java virtual machine (VM) to display the Java console window.</span></span> <span data-ttu-id="e1121-114">Das Java-Konsolenfenster selbst kann Debugausgaben aus Java-Code anzeigen, der im aufrufenden Prozess ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e1121-114">The Java console window itself can display debugging output from Java code running in the calling process.</span></span> <span data-ttu-id="e1121-115">Dies wird in der Regel nur von einer Anwendung verwendet, die die Java-VM gehostet.</span><span class="sxs-lookup"><span data-stu-id="e1121-115">Typically, this would be used only by an application hosting the Java VM.</span></span> <span data-ttu-id="e1121-116">Es gibt nur ein einzelnes Java-Konsolenfenster pro Prozess. mehrere Aufrufe der API führen zu einem Fenster, das angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e1121-116">There is only a single Java console window per process; multiple calls to the API result in the same window being displayed.</span></span> <span data-ttu-id="e1121-117">Anders ausgedrückt: Wenn das Konsolenfenster bereits angezeigt wird, geschieht nichts. Wenn das Fenster nicht angezeigt wird oder der Benutzer es geschlossen hat, wird das Fenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e1121-117">In other words, if the console window is already displayed, nothing happens; if the window has not been displayed, or the user has closed it, then the window pops up.</span></span>

<span data-ttu-id="e1121-118">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e1121-118">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1121-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e1121-119">Requirements</span></span>



| <span data-ttu-id="e1121-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e1121-120">Requirement</span></span> | <span data-ttu-id="e1121-121">Wert</span><span class="sxs-lookup"><span data-stu-id="e1121-121">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e1121-122">DLL</span><span class="sxs-lookup"><span data-stu-id="e1121-122">DLL</span></span><br/> | <dl> <span data-ttu-id="e1121-123"><dt>Msjava.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1121-123"><dt>Msjava.dll</dt></span></span> </dl> |



 

 
