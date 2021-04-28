---
description: Sicherheit (Windows 7 und Windows Server 2008 R2 Application Quality Cookbook)
ms.assetid: 87331C1D-F468-4CA4-92BD-D4E5D4E930BC
title: Sicherheit (Windows 7 und Windows Server 2008 R2 Application Quality Cookbook)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f320f4cb561079380e19a969eba95f3f6b321fb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116228"
---
# <a name="security-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a><span data-ttu-id="b37f0-103">Sicherheit (Windows 7 und Windows Server 2008 R2 Application Quality Cookbook)</span><span class="sxs-lookup"><span data-stu-id="b37f0-103">Security (Windows 7 and Windows Server 2008 R2 Application Quality Cookbook)</span></span>

<span data-ttu-id="b37f0-104">Ab Windows Internet Explorer 7 wird Windows Internet Explorer in einem Sicherheitskontext namens *Geschützter Modus* ausgeführt, wenn Benutzer sie unter dem Betriebssystem Windows Vista oder einer neueren Version ausführen.</span><span class="sxs-lookup"><span data-stu-id="b37f0-104">Starting with Windows Internet Explorer 7, Windows Internet Explorer runs in a security context called *Protected Mode* when users run it on the Windows Vista operating system or a later version.</span></span> <span data-ttu-id="b37f0-105">Dieser Modus wird Internet Explorer in einer Einstellung mit niedrigeren Berechtigungen als eine Standardbenutzeranwendung ausgeführt, sodass bestimmte Funktionen eingeschränkt sind, insbesondere ActiveX-Steuerelemente und bestimmte Arten von Plug-Ins. Weitere Informationen zum geschützten Modus in Internet Explorer und seinen Auswirkungen auf die Kompatibilität finden Sie unter [Understanding and Working in Protected Mode Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/) in der MSDN Library.</span><span class="sxs-lookup"><span data-stu-id="b37f0-105">This mode runs Internet Explorer in a lower-privilege setting than a standard user application so certain functionality is limited, especially ActiveX controls and certain types of plug-ins. For more information about Protected Mode in Internet Explorer and its impact on compatibility, see [Understanding and Working in Protected Mode Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/) in the MSDN Library.</span></span>

<span data-ttu-id="b37f0-106">Standardmäßig ermöglicht Windows Internet Explorer 8 auch die Verhinderung der Datenausführung (Data Execution Prevention, DEP), wodurch Anwendungen das Ausführen von beliebigem Code bei Onlineangriffen vermeiden können.</span><span class="sxs-lookup"><span data-stu-id="b37f0-106">By default, Windows Internet Explorer 8 also enables Data Execution Prevention (DEP), which helps applications avoid running arbitrary code in online attacks.</span></span> <span data-ttu-id="b37f0-107">Einige Add-Ons verwenden diese Sicherheitsfunktion jedoch möglicherweise nicht (z. B. alle Add-Ons, die nicht nur codeausgeführt werden sollen, der sich im Arbeitsspeicher befindet, der speziell als ausführbare Datei markiert wurde, z. B. Anwendungen, die mit einer älteren Version des ATL-Frameworks (ActiveX Template Library) erstellt wurden).</span><span class="sxs-lookup"><span data-stu-id="b37f0-107">However, some add-ons might not use this security feature (for example, any add-ons that are not designed to run only code that is located in memory that has been specifically marked as executable, such as applications that are built by using an older version of the ActiveX Template Library (ATL) framework).</span></span>

<span data-ttu-id="b37f0-108">Internet Explorer 8 schützt Benutzer auch vor potenziellen Sicherheitsrisiken, die Skripts verwenden.</span><span class="sxs-lookup"><span data-stu-id="b37f0-108">Internet Explorer 8 also protects users against potential security vulnerabilities that use scripts.</span></span> <span data-ttu-id="b37f0-109">Beispielsweise können Sie nur durch explizite Benutzerinteraktion von einer URL in einer weniger vertrauenswürdigen Zone zu einer URL in einer vertrauenswürdigeren Zone navigieren.</span><span class="sxs-lookup"><span data-stu-id="b37f0-109">For example, you cannot navigate from a URL in a less trusted zone to a URL in a more trusted zone except through explicit user interaction.</span></span> <span data-ttu-id="b37f0-110">Sie können auch bestimmte Elemente der Benutzeroberfläche des Browsers (z. B. die Adressleiste) nicht in einer nicht vertrauenswürdigen Zone (Internetzone) ausblenden.</span><span class="sxs-lookup"><span data-stu-id="b37f0-110">You also cannot hide certain elements of the browser’s user interface (such as the address bar) in an un-trusted (Internet) zone.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b37f0-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b37f0-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b37f0-112">Entwurfsupdates, die sich auf die Kompatibilität zwischen Browsern auswirken</span><span class="sxs-lookup"><span data-stu-id="b37f0-112">Design Updates that Impact Compatibility between Browsers</span></span>](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 
