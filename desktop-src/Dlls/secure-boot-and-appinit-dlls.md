---
description: Ab Windows 8 ist die \_ AppInit-DLLs-Infrastruktur deaktiviert, wenn der sichere Start aktiviert ist.
ms.assetid: 3ADE71C7-7113-4D26-8D6D-5609CAF13397
title: AppInit-DLLs und sicherer Start
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67db758eebbccd1916b5c2611c20598c3f4d25cc80cd2910be22a65b4222bbae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119256020"
---
# <a name="appinit-dlls-and-secure-boot"></a>AppInit-DLLs und sicherer Start

Ab Windows 8 ist die \_ AppInit-DLLs-Infrastruktur deaktiviert, wenn der sichere Start aktiviert ist.

## <a name="about-appinit_dlls"></a>Informationen zu \_ AppInit-DLLs

Die \_ AppInit-DLLs-Infrastruktur bietet eine einfache Möglichkeit zum Verknüpfen von System-APIs, da benutzerdefinierte DLLs in den Adressraum jeder interaktiven Anwendung geladen werden können. Sowohl Anwendungen als auch Schadsoftware verwenden AppInit-DLLs aus demselben grundlegenden Grund, d.h. apIs zu verknüpfen. Nachdem die benutzerdefinierte DLL geladen wurde, kann sie eine bekannte System-API einbinden und alternative Funktionen implementieren. Nur ein kleiner Satz moderner legitimer Anwendungen verwendet diesen Mechanismus, um DLLs zu laden, während ein großer Satz von Schadsoftware diesen Mechanismus verwendet, um Systeme zu gefährden. Selbst legitime \_ AppInit-DLLs können unbeabsichtigt zu System-Deadlocks und Leistungsproblemen führen. Daher wird die Verwendung von AppInit-DLLs \_ nicht empfohlen.

## <a name="appinit_dlls-and-secure-boot"></a>\_AppInit-DLLs und sicherer Start

Windows 8 UEFI und den sicheren Start eingeführt, um die allgemeine Systemintegrität zu verbessern und einen starken Schutz vor komplexen Bedrohungen zu bieten. Wenn der sichere Start aktiviert ist, wird der \_ AppInit-DLLs-Mechanismus im Rahmen eines kompromissfreien Ansatzes deaktiviert, um Kunden vor Schadsoftware und Bedrohungen zu schützen.

Beachten Sie, dass der sichere Start ein UEFI-Protokoll und kein Windows 8 Feature ist. Weitere Informationen zu UEFI und zur Spezifikation des sicheren Startprotokolls finden Sie unter [https://www.uefi.org](https://www.uefi.org/) .

## <a name="appinit_dlls-certification-requirement-for-windows-8-desktop-apps"></a>\_Zertifizierungsanforderung für AppInit-DLLs für Windows 8 Desktop-Apps

Eine der Zertifizierungsanforderungen für Windows 8 Desktop-Apps ist, dass die App keine beliebigen DLLs laden darf, um Win32-API-Aufrufe mithilfe des \_ AppInit-DLLs-Mechanismus abzufangen. Ausführlichere Informationen zu den Zertifizierungsanforderungen finden Sie in Abschnitt 1.1 der [Zertifizierungsanforderungen für Windows 8 Desktop-Apps.](../win_cert/certification-requirements-for-windows-desktop-apps.md)

## <a name="summary"></a>Zusammenfassung

-   Der \_ AppInit-DLLs-Mechanismus ist kein empfohlener Ansatz für legitime Anwendungen, da er zu Systemde deadlocks und Leistungsproblemen führen kann.
-   Der \_ AppInit-DLLs-Mechanismus ist standardmäßig deaktiviert, wenn der sichere Start aktiviert ist.
-   Die Verwendung von AppInit-DLLs \_ in einer Windows 8 Desktop-App ist ein Windows Fehler bei der Zertifizierung von Desktop-Apps.

Im folgenden Whitepaper finden Sie Informationen zu \_ AppInit-DLLs auf Windows 7 und Windows Server 2008 R2: [AppInit-DLLs in Windows 7 und Windows Server 2008 R2](/previous-versions/windows/hardware/download/dn550976(v=vs.85)).

 

 
