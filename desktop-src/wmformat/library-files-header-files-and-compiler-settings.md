---
title: Bibliotheksdateien, Header Dateien und Compilereinstellungen
description: Bibliotheksdateien, Header Dateien und Compilereinstellungen
ms.assetid: 7563bb3a-7bea-4e0c-8205-a16b276c8d1e
keywords:
- Windows Media-Format-SDK, DRM-Bibliotheksdateien
- Windows Media-Format-SDK, Bibliotheksdateien
- Windows Media-Format-SDK, DRM-Header Dateien
- Windows Media-Format-SDK, Header Dateien
- Windows Media-Format-SDK, DRM-Compilereinstellungen
- Windows Media-Format-SDK, Compilereinstellungen
- Digital Rights Management (DRM), Bibliotheksdateien
- DRM-Dateien (Digital Rights Management), Bibliotheksdateien
- Digital Rights Management (DRM), Header Dateien
- DRM-Dateien (Digital Rights Management), Header Dateien
- Digital Rights Management (DRM), Compilereinstellungen
- DRM (Digital Rights Management), Compilereinstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b0b10ea03cc08d5b689b74f9c647f7d0138fac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100739"
---
# <a name="library-files-header-files-and-compiler-settings"></a><span data-ttu-id="b4e01-115">Bibliotheksdateien, Header Dateien und Compilereinstellungen</span><span class="sxs-lookup"><span data-stu-id="b4e01-115">Library Files, Header Files, and Compiler Settings</span></span>

<span data-ttu-id="b4e01-116">Die Programmier Komponenten der erweiterten APIs des Windows Media DRM-Clients werden in der Header Datei "wmdrmsdk. h" definiert und in den Bibliotheken "wmdrmsdk. lib" und "mfuuid. lib" implementiert.</span><span class="sxs-lookup"><span data-stu-id="b4e01-116">The programming components of the Windows Media DRM Client Extended APIs are defined in the wmdrmsdk.h header file, and implemented in the wmdrmsdk.lib and mfuuid.lib libraries.</span></span>

<span data-ttu-id="b4e01-117">Für einige Funktionen der erweiterten APIs des Windows Media DRM-Clients ist es erforderlich, dass Sie eine geschützte Bibliothek von Microsoft erhalten.</span><span class="sxs-lookup"><span data-stu-id="b4e01-117">Some of the functionality of the Windows Media DRM Client Extended APIs requires that you obtain a protected library from Microsoft.</span></span> <span data-ttu-id="b4e01-118">Diese Bibliothek, die in dieser Dokumentation als stubbibliothek bezeichnet wird, ist für den Empfänger spezifisch und gibt die Anwendungs Sicherheitsstufe für Ihre Anwendungen an.</span><span class="sxs-lookup"><span data-stu-id="b4e01-118">This library, called the stub library in this documentation, is specific to the recipient and specifies the application security level for your applications.</span></span> <span data-ttu-id="b4e01-119">Die Stub-Bibliothek ersetzt wmdrmsdk. lib; Sie sollten niemals eine Verknüpfung mit beiden herstellen.</span><span class="sxs-lookup"><span data-stu-id="b4e01-119">The stub library replaces wmdrmsdk.lib; you should never link to both.</span></span>

<span data-ttu-id="b4e01-120">**Hinweis** Die DRM-stubbibliothek ist von der stubbibliothek getrennt, die vom Rest des Windows Media Format SDK verwendet wird, aber mit der gleichen Methode lizenziert ist.</span><span class="sxs-lookup"><span data-stu-id="b4e01-120">**Note** The DRM stub library is separate from the stub library used by the rest of the Windows Media Format SDK but is licensed using the same method.</span></span>

<span data-ttu-id="b4e01-121">**Hinweis** Die DRM-stubbibliothek muss nach der Bibliotheksdatei msvcrt. lib mit Ihrer Anwendung verknüpft werden, um Linker-Fehler zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="b4e01-121">**Note** The DRM stub library must be linked into your application after the library file msvcrt.lib to avoid linker errors.</span></span>

<span data-ttu-id="b4e01-122">Die Stub-Bibliothek enthält ein eingebettetes Zertifikat, das von Microsoft gesperrt werden kann, wenn Sie die Geschäftsbedingungen des Lizenzvertrags nicht einhalten.</span><span class="sxs-lookup"><span data-stu-id="b4e01-122">The stub library contains an embedded certificate which can be revoked by Microsoft if you fail to comply with the terms and conditions of the license agreement.</span></span>

<span data-ttu-id="b4e01-123">Bestimmte Methoden, die die stubbibliothek erfordern, werden in der-Dokumentation bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="b4e01-123">Specific methods that require the stub library are labeled in the documentation.</span></span> <span data-ttu-id="b4e01-124">Wenn Sie versuchen, eine solche Methode ohne Verknüpfung mit der stubbibliothek zu verwenden, wird ein Fehler vom Typ "NS \_ E \_ DRM- \_ stublib erforderlich" zurückgegeben \_ .</span><span class="sxs-lookup"><span data-stu-id="b4e01-124">If you try to use such a method without linking to the stub library, it will return an NS\_E\_DRM\_STUBLIB\_REQUIRED error.</span></span>

<span data-ttu-id="b4e01-125">Das DRM-Subsystem kann nicht in einem Debugbuild verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b4e01-125">The DRM subsystem can not be used in a debug build.</span></span> <span data-ttu-id="b4e01-126">Wenn dies versucht wird, geben Methoden der API den Fehler "NS \_ E \_ DRM- \_ Debugging \_ nicht \_ zulässig" zurück.</span><span class="sxs-lookup"><span data-stu-id="b4e01-126">If this is attempted, methods of the API will return the NS\_E\_DRM\_DEBUGGING\_NOT\_ALLOWED error.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b4e01-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b4e01-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4e01-128">**Einstieg**</span><span class="sxs-lookup"><span data-stu-id="b4e01-128">**Getting Started**</span></span>](drm-getting-started.md)
</dt> <dt>

[<span data-ttu-id="b4e01-129">**Bibliotheksdateien und Compilereinstellungen**</span><span class="sxs-lookup"><span data-stu-id="b4e01-129">**Library Files and Compiler Settings**</span></span>](library-files-and-compiler-settings.md)
</dt> <dt>

[<span data-ttu-id="b4e01-130">**Abrufen der erforderlichen DRM-Bibliothek**</span><span class="sxs-lookup"><span data-stu-id="b4e01-130">**Obtaining the Required DRM Library**</span></span>](obtaining-the-required-drm-library.md)
</dt> </dl>

 

 




