---
description: Die DbgHelp-Bibliothek wird von DbgHelp.dll.
ms.assetid: 8ef1740d-c791-4fbd-8297-7207a987c09d
title: DbgHelp-Versionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5adb00c6442f7ba36f5aeb86e0255e175131492124d08fbf865e57a9721a7893
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119343860"
---
# <a name="dbghelp-versions"></a>DbgHelp-Versionen

Die DbgHelp-Bibliothek wird von DbgHelp.dll. Obwohl diese DLL in allen unterstützten Versionen von Windows enthalten ist, ist sie selten die neueste verfügbare Version von DbgHelp. Darüber hinaus verfügt die version von DbgHelp, die in Windows erhältlich ist, über eingeschränkte Funktionalität im Gegensatz zu den anderen Releases. Insbesondere fehlt die Unterstützung für Symbolserver und Quellserver.

Die aktuellen Versionen von DbgHelp.dll, SymSrv.dll und SrcSrv.dll sind als Teil des Pakets [Debugtools für](https://developer.microsoft.com/windows/downloads/windows-10-sdk) Windows verfügbar. Die Weiterverteilungsrichtlinien für diese enthaltenen DLLs wurden speziell entwickelt, um es Personen so einfach wie möglich zu machen, diese Dateien in ihre eigenen Pakete und Releases einzuteilen.

> [!Caution]  
> Benutzer sollten nie versuchen, die Debugtools für [Windows-Versionen](https://developer.microsoft.com/windows/downloads/windows-10-sdk) von DbgHelp.dll in den Windows-Systemverzeichnissen zu installieren, da sie in diesem Szenario nicht getestet werden und das System wahrscheinlich destabilisieren. Es gibt separate X64- und X86-Versionen des Debugpakets, und beide sind für Personen erforderlich, die beide Plattformen unterstützen möchten.

Um die neueste Version von DbgHelp.dll zu erhalten, wechseln Sie zu Debugtools für [https://developer.microsoft.com/windows/downloads/windows-10-sdk](https://developer.microsoft.com/windows/downloads/windows-10-sdk) Windows. Informationen zur richtigen Installation finden Sie unter Aufrufen der [DbgHelp-Bibliothek.](calling-the-dbghelp-library.md)

> [!Note]  
> Die DbgHelp.dll, die im Windows ist nicht verteilbar.

Viele Versionen von DbgHelp enthalten zusätzliche Funktionen. Um sicherzustellen, dass die richtige Version von DbgHelp für Ihre Anwendung verfügbar ist, lesen Sie die Anforderungsinformationen in der spezifischen API-Referenzdokumentation.
