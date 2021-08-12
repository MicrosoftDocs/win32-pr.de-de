---
title: Prozessinteroperabilität
description: Sie können Win32-basierte Anwendungen auf 64-Bit-Windows mithilfe einer Emulationsebene ausführen. Windows 10 auf ARM enthält eine x86-auf-ARM64-Emulationsebene. Weitere Informationen finden Sie unter Ausführen von 32-Bit-Anwendungen.
ms.assetid: a573f26c-7577-4ff0-b314-ae0a33274738
keywords:
- Prozessinteroperabilität 64-Bit-Windows-Programmierung
- 64-Bit-Windows-Interoperabilitätsprogrammierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c74e75af4299e9c249ea46b8eac2cdd47de10eb3f832aa88d6b313d20304afc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118561516"
---
# <a name="process-interoperability"></a>Prozessinteroperabilität

Sie können Win32-basierte Anwendungen auf 64-Bit-Windows mithilfe einer Emulationsebene ausführen. Windows 10 auf ARM enthält eine x86-auf-ARM64-Emulationsebene. Weitere Informationen finden Sie unter [Ausführen von 32-Bit-Anwendungen.](running-32-bit-applications.md)

Auf 64-Bit-Windows kann ein 64-Bit-Prozess keine 32-Bit-DLL (Dynamic Link Library) laden. Darüber hinaus kann ein 32-Bit-Prozess keine 64-Bit-DLL laden. 64-Bit-Windows unterstützt jedoch Remoteprozeduraufrufe (RPC) zwischen 64-Bit- und 32-Bit-Prozessen (sowohl auf demselben Computer als auch computerübergreifend). Auf 64-Bit-Windows kann ein Out-of-Process-32-Bit-COM-Server mit einem 64-Bit-Client kommunizieren, und ein Out-of-Process-64-Bit-COM-Server kann mit einem 32-Bit-Client kommunizieren. Wenn Sie also über eine 32-Bit-DLL verfügen, die nicht COM-fähige DLL ist, können Sie sie in einem OUT-of-Process-COM-Server umschließen und COM verwenden, um Aufrufe an einen und aus einem 64-Bit-Prozess zu marshallen.

In-Process-Server werden derzeit mithilfe des **Registrierungseintrags InprocServer** registriert. Auf 64-Bit-Windows sollten 64- und 32-Bit-Prozessserver den Eintrag **InprocServer32** verwenden.

Verwenden Sie anstelle des **INT \_ PTR-** oder **DWORD \_ PTR-Typs** den **HANDLE \_ PTR-Typ,** um Handles zu portieren, die ihrer Natur nach lokal auf dem Computer sind und niemals über die 32-Bit- bis 64-Bit-Grenze hinweg verwendet werden. Dies schließt das Portieren von RPC-Schnittstellen ein, die Handles wie **DWORD-Werte** übergeben. Der **64-Bit-HANDLE-PTR \_** ist 64 Bits im Kabel (nicht abgeschnitten) und muss daher nicht zugeordnet werden. (Der **32-Bit-HANDLE-PTR \_** ist 32 Bits im Kabel.)

Weitere Informationen finden Sie unter [Entwerfen von 64-Bit-kompatiblen Schnittstellen.](designing-64-bit-compatible-interfaces.md)

 

 




