---
description: Umgang mit Ären im japanischen Kalender
ms.assetid: a1dabf7c-6521-492e-bdc0-27cfb07cfc20
title: Umgang mit Ären im japanischen Kalender
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eba757745bf0d90d119c821772c7fc23f3f8694b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867927"
---
# <a name="era-handling-for-the-japanese-calendar"></a><span data-ttu-id="f79db-103">Umgang mit Ären im japanischen Kalender</span><span class="sxs-lookup"><span data-stu-id="f79db-103">Era Handling for the Japanese Calendar</span></span>

<span data-ttu-id="f79db-104">Viele Kalender haben Zeiträume, z. b. AD/BC oder CE/BCE.</span><span class="sxs-lookup"><span data-stu-id="f79db-104">Many calendars have eras, such as AD/BC or CE/BCE.</span></span> <span data-ttu-id="f79db-105">Im japanischen Kalender werden Jahre durch Nengō, eine Kombination aus Jahr-und Zeit Namen, beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f79db-105">In the Japanese Calendar, years are described by nengō, a combination of the year number and era name.</span></span> <span data-ttu-id="f79db-106">2009 ist z. b. Heisei 21.</span><span class="sxs-lookup"><span data-stu-id="f79db-106">For example, 2009 is Heisei 21.</span></span> <span data-ttu-id="f79db-107">In der Vergangenheit haben sich die Namen japanischer Zeiträume häufig geändert, aber jetzt ändern sich die japanischen Zeiträume nur in der kaiserlichen Nachfolge.</span><span class="sxs-lookup"><span data-stu-id="f79db-107">In the past, Japanese era names changed frequently, but now the Japanese eras change only on imperial succession.</span></span> <span data-ttu-id="f79db-108">Windows und Microsoft .net haben in der Vergangenheit vier moderne Zeiträume unter dieser Richtlinie unterstützt: Meiji, Taishō, Shōwa und heiist.</span><span class="sxs-lookup"><span data-stu-id="f79db-108">Windows and Microsoft .NET have historically supported the four modern eras under this policy: Meiji, Taishō, Shōwa and Heisei.</span></span>

<span data-ttu-id="f79db-109">Mit Windows 7, Windows Server 2008 R2 und dem .NET Framework 4 erkennt Microsoft, dass weitere Zeiträume in Zukunft hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="f79db-109">With Windows 7, Windows Server 2008 R2, and the .NET Framework 4, Microsoft recognizes that additional eras may be added in the future.</span></span> <span data-ttu-id="f79db-110">In diesen Versionen von Windows werden die ERA-Daten in der Registrierung unter dem Schlüssel gespeichert:</span><span class="sxs-lookup"><span data-stu-id="f79db-110">On these versions of Windows the era data is stored in the registry under the key:</span></span><dl> <span data-ttu-id="f79db-111">HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ nls \\ Kalenders \\ Japanese \\ Eras</span><span class="sxs-lookup"><span data-stu-id="f79db-111">HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\Nls\\Calendars\\Japanese\\Eras</span></span>  
</dl>

<span data-ttu-id="f79db-112">Gegebenenfalls können dem Schlüssel durch den normalen Windows Update Prozess weitere Zeiträume hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="f79db-112">If necessary, additional eras can be added to that key through the normal Windows Update process.</span></span> <span data-ttu-id="f79db-113">Dieser Schlüssel kann mithilfe des Registrierungs-Editors (Regedit.exe) angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f79db-113">This key can be viewed using the registry editor (Regedit.exe).</span></span> <span data-ttu-id="f79db-114">Ein Beispiel für den in Windows 7 gelieferten Schlüssel und die folgenden Werte sind:</span><span class="sxs-lookup"><span data-stu-id="f79db-114">An example of the key and values shipped in Windows 7 is:</span></span>

``` syntax
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Nls\Calendars\Japanese\Eras]
"1868 01 01"="明治_明_Meiji_M"
"1912 07 30"="大正_大_Taisho_T"
"1926 12 25"="昭和_昭_Showa_S"
"1989 01 08"="平成_平_Heisei_H"
```

<span data-ttu-id="f79db-115">Der Name jedes ERA-Werts ist das Datum, an dem der Zeitraum im gregorianischen Kalender beginnt.</span><span class="sxs-lookup"><span data-stu-id="f79db-115">The name of each era value is the date the era begins in the Gregorian calendar.</span></span> <span data-ttu-id="f79db-116">Der Wert enthält den Zeit Namen in Japanisch, den abgekürzten Namen in Japanisch, den Namen in englischer Sprache und einen abgekürzten Namen in englischer Sprache:</span><span class="sxs-lookup"><span data-stu-id="f79db-116">The value contains the era name in Japanese, the abbreviated name in Japanese, the name in English, and an abbreviated name in English:</span></span><dl> <span data-ttu-id="f79db-117">"yyyy mm dd" = "je \_ AJE \_ EE \_ AEE"</span><span class="sxs-lookup"><span data-stu-id="f79db-117">"YYYY MM DD"="JE\_AJE\_EE\_AEE"</span></span>  
</dl>where

-   <span data-ttu-id="f79db-118">"Yyyy mm dd" ist das gregorianische Datum des Zeitraums in Jahr, Monat, Tag, wobei Jahr vier Ziffern, Tag 2 Ziffern und Monat auch 2 Ziffern sind.</span><span class="sxs-lookup"><span data-stu-id="f79db-118">"YYYY MM DD" is the Gregorian date of the start of the era in year, month, day form where year is 4 digits, day is 2 digits and month is also 2 digits.</span></span> <span data-ttu-id="f79db-119">Die einzelnen Teile des Datums werden durch ein Leerzeichen voneinander getrennt.</span><span class="sxs-lookup"><span data-stu-id="f79db-119">A space separates each part of the date.</span></span>
-   <span data-ttu-id="f79db-120">"Je" ist der japanische Name des Zeitraums, gefolgt von einem Unterstrich.</span><span class="sxs-lookup"><span data-stu-id="f79db-120">"JE" is the Japanese name of the era, and is followed by an underscore.</span></span>
-   <span data-ttu-id="f79db-121">"AJE" ist der abgekürzte Name des Zeitraums, in Japanisch und gefolgt von einem Unterstrich.</span><span class="sxs-lookup"><span data-stu-id="f79db-121">"AJE" is the abbreviated name of the era, in Japanese, and is followed by an underscore.</span></span>
-   <span data-ttu-id="f79db-122">"Ee" ist der englische Name des japanischen Zeitraums, gefolgt von einem Unterstrich.</span><span class="sxs-lookup"><span data-stu-id="f79db-122">"EE" is the English name of the Japanese era, and is followed by an underscore.</span></span>
-   <span data-ttu-id="f79db-123">"AEE" ist der abgekürzte englische Name des japanischen Zeitraums.</span><span class="sxs-lookup"><span data-stu-id="f79db-123">"AEE" is the abbreviated English name of the Japanese era.</span></span>

<span data-ttu-id="f79db-124">Ein Aspekt für Anwendungsentwickler ist die Möglichkeit, dass zusätzliche Zeiträume Windows Update oder auf andere Weise hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="f79db-124">One consideration for application developers is the possibility that additional eras will be added by Windows Update or other means.</span></span> <span data-ttu-id="f79db-125">In diesem Fall kann es sein, dass die Anwendung mehr als die erwarteten vier Zeiträume für den japanischen Kalender trifft.</span><span class="sxs-lookup"><span data-stu-id="f79db-125">In that case the application may encounter more than the expected four eras for the Japanese calendar.</span></span> <span data-ttu-id="f79db-126">Für Testzwecke können Tester der Registrierung einen zusätzlichen Zeitraum hinzufügen. Dies sollte jedoch nur auf Testcomputer beschränkt werden, da sich dies auf das Verhalten des gesamten Computers auswirkt.</span><span class="sxs-lookup"><span data-stu-id="f79db-126">For testing purposes testers may add an additional era to the registry; however, that should be restricted to test machines only, as it impacts the behavior of the entire machine.</span></span>

<span data-ttu-id="f79db-127">Ein Beispiel für einen solchen Schlüssel, der für Tests verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f79db-127">An example of such a key that could be used for test follows.</span></span> <span data-ttu-id="f79db-128">Diese Änderung kann mit dem Registrierungs-Editor vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="f79db-128">This change can be made with the registry editor.</span></span> <span data-ttu-id="f79db-129">(Dies ist ein Beispiel für die Test Verwendung, und es ist nicht dafür vorgesehen, zukünftige Ergänzungen vorherzusagen.)</span><span class="sxs-lookup"><span data-stu-id="f79db-129">(This is an example for test use only, and is not intended to predict any future additions.)</span></span>

``` syntax
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Nls\Calendars\Japanese\Eras]
"2020 09 01"="仮名_仮_Test Era_X"
```

<span data-ttu-id="f79db-130">Beachten Sie, dass sich dies nur auf Computern mit Windows 7 und höher oder .NET Framework 4 und höher auswirkt.</span><span class="sxs-lookup"><span data-stu-id="f79db-130">Note that this only impacts machines running Windows 7 and later or .NET Framework 4 and later.</span></span> <span data-ttu-id="f79db-131">Anwendungsentwicklern wird empfohlen, Ihre Anwendungen mit solchen zusätzlichen Testperioden zu testen, um sicherzustellen, dass Ihre Anwendungen weiterhin funktionieren, wenn zu einem späteren Zeitpunkt weitere Zeiträume hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="f79db-131">Application developers are encouraged to test their applications with such additional test eras to ensure that their applications will continue to work if additional eras are added at some future date.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f79db-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f79db-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f79db-133">Abrufen von Zeit-und Datumsinformationen</span><span class="sxs-lookup"><span data-stu-id="f79db-133">Retrieving Time and Date Information</span></span>](retrieving-time-and-date-information.md)
</dt> <dt>

[<span data-ttu-id="f79db-134">Kalender Bezeichner</span><span class="sxs-lookup"><span data-stu-id="f79db-134">Calendar Identifiers</span></span>](calendar-identifiers.md)
</dt> </dl>

 

 



