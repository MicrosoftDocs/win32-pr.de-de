---
title: 32-Bit-und 64-Bit-Interoperabilität
description: Hilfstechnologieanwendungen müssen über Prozess Grenzen hinweg kommunizieren, um Benutzeroberflächen Informationen von Microsoft Active Accessibility-Servern und Microsoft UI Automation-Anbietern zu erhalten.
ms.assetid: 8b46daed-4fd9-430c-bb4d-24be9c8015b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6897082db00e27d77d90e5fc72d5f229834ce760
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728440"
---
# <a name="32-bit-and-64-bit-interoperability"></a>32-Bit-und 64-Bit-Interoperabilität

Hilfstechnologieanwendungen müssen über Prozess Grenzen hinweg kommunizieren, um Benutzeroberflächen Informationen von Microsoft Active Accessibility-Servern und Microsoft UI Automation-Anbietern zu erhalten. In diesem Thema werden die Hauptprobleme bei der prozessübergreifenden Kommunikation beschrieben, die Sie beim Entwickeln von Windows-Anwendungen für die Barrierefreiheit berücksichtigen müssen.

Wenn Anwendungen die Windows Automation-API verwenden, behandeln die Laufzeitkomponenten von Microsoft Active Accessibility und Benutzeroberflächen Automatisierung automatisch alle Probleme und Komplexitäten, die bei der Durchführung der prozessübergreifenden Kommunikation (Multiprocess Communications, IPC) auftreten, einschließlich der Interoperabilitätsprobleme, wenn ein Prozess 32 Bits und der andere 64 Bits ist. Microsoft erkennt, dass es Fälle gibt, in denen eine hilfstechnologieanwendung möglicherweise eine Form von IPC anstelle der Windows-Automatisierungs-API verwenden muss, um mit einem Microsoft Active Accessibility Server oder Benutzeroberflächenautomatisierungs-Anbieter zu kommunizieren. In diesen Fällen empfiehlt Microsoft die Verwendung von DCOM-oder Windows-Nachrichten (mit Werten, die kleiner als der **WM- \_ Benutzer** sind) für die Kommunikation mit anderen Prozessen. Ebenso wie die Windows Automation-API behandeln DCOM-und Windows-Nachrichten automatisch alle IPC-Probleme, einschließlich der 32-Bit-zu-64-Bit-Interoperabilität.

Wenn die Windows-Automatisierungs-API, DCOM und Windows-Meldungen keine Option sind, sollten Sie bei der Implementierung der gewählten IPC-Methode folgende Punkte beachten:

-   Shared Memory – Wenn Sie gemeinsam genutzten Speicher verwenden, beachten Sie, dass eine Struktur in einem 32-Bit-Prozess möglicherweise eine andere Größe und ein anderes Layout als dieselbe Struktur in einem 64-Bit-Prozess hat. Dies gilt insbesondere für Strukturen, die Zeiger oder Handles enthalten.
-   Zeiger Abschneiden – obwohl eine 32-Bit-Anwendung den **Longlong** -Datentyp verwenden kann, um einen 64-Bit-Wert zu speichern, gibt es Instanzen, in denen kein Windows-API-Element vorhanden ist, das es der 32-Bit-Anwendung ermöglicht, einen 64-Bit-Wert von einem 64-Bit-Prozess zu erhalten oder einen 64-Bit-Wert an einen 64 Die Funktionen " [**getwindowlongptr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra) " und " [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) " Schneiden beispielsweise alle Zeiger Werte ab und belassen die 32-Bit-Anwendung mit einem nutzlosen Wert.
-   Handles – da Kernel32-und User32-Handles in 32-Bit-und 64-Bit-Prozessen nur 32 Bit groß sind, können Sie ohne Probleme zwischen Prozessen übertragen werden. Einige Elemente, die von Windows als Handles definiert werden, sind jedoch wirklich einfach umschließende Zeiger (z. b. **HTREEITEM**). Diese "Handles" werden abgeschnitten, wenn Sie von einem 64-Bit-Prozess an einen 32-Bit-Prozess übermittelt werden.
-   [WinEvent](winevents-infrastructure.md) Hook-Funktionen – um eine kontextbasierte Hook-Funktion mit einem 32-Bit-Server Prozess zu registrieren, muss sich die Hook-Funktion in einer 32-Bit-DLL befinden. Ebenso muss sich die Hook-Funktion in einer 64-Bit-DLL befinden, um eine kontextbasierte Hook-Funktion mit einem 64-Bit-Server Prozess zu registrieren. Wenn eine hilfstechnologieanwendung versucht, eine kontextbasierte Hook-Funktion bei einem Server zu registrieren, der über eine andere Bittiefe verfügt, werden Ereignisse weiterhin an die Hook-Funktion übermittelt, aber Sie werden außerhalb des Kontexts bereitgestellt. Weitere Informationen finden Sie unter WinEvents und Kontext- [und Out-of-Context-Hook-Funktionen](in-context-and-out-of-context-hook-functions.md).

Weitere Informationen zur 32-Bit-und 64-Bit-Interoperabilität finden Sie unter [Prozess Interoperabilität](/windows/desktop/WinProg64/process-interoperability).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über die Windows Automation-API](windows-automation-api-overview.md)
</dt> </dl>

 

 