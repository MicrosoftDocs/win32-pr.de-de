---
description: Die DbgHelp-Bibliothek wird von DbgHelp.dll implementiert.
ms.assetid: 8ef1740d-c791-4fbd-8297-7207a987c09d
title: Dbghelp-Versionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811e92ba88bf38cb46274e2d2c716a620ea83b16
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747744"
---
# <a name="dbghelp-versions"></a>Dbghelp-Versionen

Die DbgHelp-Bibliothek wird von DbgHelp.dll implementiert. Obwohl diese DLL in allen unterstützten Versionen von Windows enthalten ist, ist sie selten die aktuellste Version von dbghelp verfügbar. Außerdem hat die in Windows enthaltene Version von dbghelp eine geringere Funktionalität wie die anderen Releases. insbesondere fehlt die Unterstützung für Symbol Server und Quell Server.

Die aktuellsten Versionen von DbgHelp.dll, SymSrv.dll und SrcSrv.dll sind als Teil des Pakets " [Debugtools für Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk) " verfügbar. Die weitergaberichtlinienerweiterungsrichtlinien für diese enthaltenen DLLs wurden speziell so konzipiert, dass die Benutzer diese Dateien in ihren eigenen Paketen und Releases einschließen können.

> [!Caution]  
> Benutzer sollten nie versuchen, die [Debugtools für Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk) -Versionen von DbgHelp.dll in den Windows-Systemverzeichnissen zu installieren, da Sie in diesem Szenario nicht getestet werden und wahrscheinlich das System destabilisieren. Es gibt separate x64-und x86-Versionen des debugpakets. beides ist für Benutzer erforderlich, die beide Plattformen unterstützen möchten.

Um die neueste Version von DbgHelp.dll zu erhalten, navigieren [https://developer.microsoft.com/windows/downloads/windows-10-sdk](https://developer.microsoft.com/windows/downloads/windows-10-sdk) Sie zu, und laden Sie die Debugtools für Windows herunter. Informationen zur ordnungsgemäßen Installation finden Sie unter [Aufrufen der DbgHelp-Bibliothek](calling-the-dbghelp-library.md) .

> [!Note]  
> Die DbgHelp.dll-Datei, die in Windows enthalten ist, ist nicht Verteil Bar.

Viele Versionen von dbghelp enthalten zusätzliche Funktionen. Um sicherzustellen, dass die richtige Version von dbghelp für Ihre Anwendung verfügbar ist, überprüfen Sie die Anforderungs Informationen in der spezifischen API-Referenz Dokumentation.
