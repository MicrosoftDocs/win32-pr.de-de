---
description: Ab Windows 8 ist die AppInit- \_ DLLs-Infrastruktur deaktiviert, wenn der sichere Start aktiviert ist.
ms.assetid: 3ADE71C7-7113-4D26-8D6D-5609CAF13397
title: AppInit-DLLs und sicherer Start
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2915dda53959f2a403a62112385fe80e735cbfd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359515"
---
# <a name="appinit-dlls-and-secure-boot"></a>AppInit-DLLs und sicherer Start

Ab Windows 8 ist die AppInit- \_ DLLs-Infrastruktur deaktiviert, wenn der sichere Start aktiviert ist.

## <a name="about-appinit_dlls"></a>Informationen zu AppInit- \_ DLLs

Die AppInit- \_ DLLs-Infrastruktur bietet eine einfache Möglichkeit, um System-APIs zu verbinden, indem Sie zulässt, dass benutzerdefinierte DLLs in den Adressraum der einzelnen interaktiven Anwendungen geladen werden. Anwendungen und Schadsoftware verwenden beide AppInit-DLLs aus demselben Grund, d. h. mit Hook-APIs. Nachdem die benutzerdefinierte DLL geladen wurde, kann Sie eine bekannte System-API anschließen und alternative Funktionen implementieren. Nur ein kleiner Satz moderner legitimer Anwendungen verwendet diesen Mechanismus zum Laden von DLLs, während ein großer Satz Schadsoftware diesen Mechanismus verwendet, um Systeme zu gefährden. Selbst legitime AppInit \_ -DLLs können versehentlich zu System Deadlocks und Leistungsproblemen führen, weshalb die Verwendung von AppInit- \_ DLLs nicht empfohlen wird.

## <a name="appinit_dlls-and-secure-boot"></a>AppInit \_ -DLLs und sicherer Start

Windows 8 hat UEFI und sicheren Start eingesetzt, um die allgemeine Systemintegrität zu verbessern und einen starken Schutz vor anspruchsvollen Bedrohungen zu bieten. Wenn der sichere Start aktiviert ist, wird der AppInit- \_ DLLs-Mechanismus als Teil eines nicht kompromittierten Ansatzes deaktiviert, um Kunden vor Schadsoftware und Bedrohungen zu schützen.

Beachten Sie, dass der sichere Start ein UEFI-Protokoll und kein Windows 8-Feature ist. Weitere Informationen zu UEFI und der Secure Boot Protocol-Spezifikation finden Sie unter [https://www.uefi.org](https://www.uefi.org/) .

## <a name="appinit_dlls-certification-requirement-for-windows-8-desktop-apps"></a>AppInit \_ -DLLs-Zertifizierungs Anforderung für Windows 8-Desktop-Apps

Eine der Zertifizierungsanforderungen für Windows 8-Desktop-Apps besteht darin, dass die APP keine beliebigen DLLs laden darf, um Win32-API-Aufrufe mithilfe des AppInit- \_ DLLs-Mechanismus abzufangen. Ausführlichere Informationen zu den Zertifizierungsanforderungen finden Sie im Abschnitt 1,1 der [Zertifizierungsanforderungen für Windows 8-Desktop-Apps](../win_cert/certification-requirements-for-windows-desktop-apps.md).

## <a name="summary"></a>Zusammenfassung

-   Der AppInit \_ -DLLs-Mechanismus ist keine empfohlene Vorgehensweise für legitime Anwendungen, da dies zu System Deadlocks und Leistungsproblemen führen kann.
-   Der AppInit- \_ DLLs-Mechanismus ist standardmäßig deaktiviert, wenn der sichere Start aktiviert ist.
-   Die Verwendung von AppInit- \_ DLLs in einer Windows 8-Desktop-App ist ein Zertifizierungs Fehler bei der Windows-Desktop-App

Im folgenden Whitepaper finden Sie Informationen zu AppInit \_ -DLLs unter Windows 7 und Windows Server 2008 R2: [AppInit-DLLs in Windows 7 und Windows Server 2008 R2](/previous-versions/windows/hardware/download/dn550976(v=vs.85)).

 

 
