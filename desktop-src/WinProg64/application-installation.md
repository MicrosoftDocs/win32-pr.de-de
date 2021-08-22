---
title: Anwendungsinstallation auf 64-Bit-Systemen
description: Der 64-Bit-Windows Installer kann nahtlos 32-Bit-MSI-basierte Anwendungen auf 64-Bit-Windows installieren.
ms.assetid: fb9c5720-9906-4827-9daf-d7caa453e818
keywords:
- 64-Bit-Windows-Programmierung für die Anwendungsinstallation
- Installation von 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26f06eaa527142145791e4ed29e2420d16b1d7a2f4fbe9a77801857a844ed7b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119643600"
---
# <a name="application-installation-on-64-bit-systems"></a>Anwendungsinstallation auf 64-Bit-Systemen

Der [64-Bit-Windows Installer](/windows/desktop/Msi/windows-installer-on-64-bit-operating-systems) kann 32-Bit-MSI-basierte Anwendungen nahtlos auf 64-Bit-Windows installieren. Bei älteren Anwendungen, die einen 16-Bit-Stub zum Starten einer 32-Bit-Installations-Engine verwenden, erkennt 64-Bit-Windows bestimmte 16-Bit-Installationsprogrammprogramme und ersetzt eine portierte 32-Bit-Version.

16-Bit-DOS-, Windows- oder OS/2-Anwendungen verwenden häufig einen 16-Bit-Stub, um den Computertyp zu überprüfen, und starten dann eine 32-Bit-Installations-Engine, um die Installation durchzuführen. Um die Installation von Anwendungen zu ermöglichen, die dieses Verfahren verwenden, ersetzt 64-Bit-Windows 32-Bit-Versionen durch die folgenden 16-Bit-Installationsprogramme:

* Microsoft Setup für Windows 1.2  
* Microsoft Setup für Windows 2.6  
* Microsoft Setup für Windows 3.0  
* Microsoft Setup für Windows 3.01  
* InstallShield 5.x  

Die Liste der Ersetzungen wird in der Registrierung unter dem folgenden Schlüssel gespeichert: **HKEY \_ LOCAL MACHINE Software Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion \\ NtVdm64**.

> [!Note]  
> Dieser Mechanismus wird nur für die Kompatibilität mit 32-Bit-Anwendungen bereitgestellt, die die in diesem Thema aufgeführten 16-Bit-Installationsprogramm von Microsoft verwenden. Das Hinzufügen von Installationsprogrammprogrammen von Drittanbietern wird nicht unterstützt.

 

> [!Note]  
> Dieser Mechanismus ist für Windows 10 auf ARM nicht enthalten.

 

 

 