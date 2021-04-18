---
title: Prozess Interoperabilität
description: Sie können Win32-basierte Anwendungen auf 64-Bit-Windows mithilfe einer Emulations Schicht ausführen. Windows 10 auf ARM umfasst eine x86-on-ARM64-Emulations Schicht. Weitere Informationen finden Sie unter Ausführen von 32-Bit-Anwendungen.
ms.assetid: a573f26c-7577-4ff0-b314-ae0a33274738
keywords:
- Prozess Interoperabilität 64-Bit-Windows-Programmierung
- Interoperabilität 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 023be0dafabfa8b17cf460542ae06467db517c11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338391"
---
# <a name="process-interoperability"></a>Prozess Interoperabilität

Sie können Win32-basierte Anwendungen auf 64-Bit-Windows mithilfe einer Emulations Schicht ausführen. Windows 10 auf ARM umfasst eine x86-on-ARM64-Emulations Schicht. Weitere Informationen finden Sie unter [Ausführen von 32-Bit-Anwendungen](running-32-bit-applications.md).

Bei 64-Bit-Fenstern kann ein 64-Bit-Prozess keine 32-Bit-DLL (Dynamic-Link Library) laden. Außerdem kann ein 32-Bit-Prozess keine 64-Bit-DLL laden. 64-Bit-Windows unterstützt jedoch remote Prozedur Aufrufe (Remote Procedure Calls, RPC) zwischen 64-Bit-und 32-Bit-Prozessen (auf demselben Computer und Computer übergreifend). Auf 64-Bit-Fenstern kann ein Prozess interner 32-Bit-COM-Server mit einem 64-Bit-Client kommunizieren, und ein Prozess interner 64-Bit-COM-Server kann mit einem 32-Bit-Client kommunizieren. Wenn Sie also über eine 32-Bit-DLL verfügen, die nicht com-fähig ist, können Sie Sie in einem Prozess externen COM-Server einschließen und com verwenden, um Aufrufe von und von einem 64-Bit-Prozess zu Mars Hallen.

Prozess interne Server werden zurzeit mit dem Registrierungs Eintrag **InprocServer** registriert. Auf 64-Bit-Windows-Servern sollten 64-und 32-Bit-Prozess interne Server den Eintrag **InProcServer32** verwenden.

Verwenden Sie zum Portieren von Handles, die in ihrer Art lokal auf dem Computer sind und nie über die 32-Bit-zu-64-Bit-Grenze verwendet werden, den **handle- \_ ptr** -Typ anstelle des **int- \_ ptr** -oder **DWORD- \_ ptr** -Typs. Dies umfasst das Portieren von RPC-Schnittstellen, die solche Handles als **DWORD** -Werte übergeben Das 64-Bit- **handle " \_ ptr** " ist im Netzwerk 64 Bits (nicht abgeschnitten) und benötigt daher keine Zuordnung. (Das 32-Bit- **handle \_ ptr** ist 32 Bits.)

Weitere Informationen finden Sie unter [Entwerfen von 64-Bit-kompatiblen Schnittstellen](designing-64-bit-compatible-interfaces.md).

 

 




