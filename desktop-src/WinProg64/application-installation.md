---
title: Anwendungs Installation auf 64-Bit-Systemen
description: Der 64-Bit-Windows Installer kann auf 64-Bit-Windows-Anwendungen nahtlos auf 32-Bit-MSI-basierten Anwendungen installieren.
ms.assetid: fb9c5720-9906-4827-9daf-d7caa453e818
keywords:
- Anwendungs Installation 64-Bit-Windows-Programmierung
- Installation 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13a5f8f623776ffa637718fc0d565f2c71a7b8e6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101906"
---
# <a name="application-installation-on-64-bit-systems"></a>Anwendungs Installation auf 64-Bit-Systemen

Der [64-Bit-Windows Installer](/windows/desktop/Msi/windows-installer-on-64-bit-operating-systems) kann auf 64-Bit-Windows-Anwendungen nahtlos auf 32-Bit-MSI-basierten Anwendungen installieren. Bei älteren Anwendungen, die einen 16-Bit-Stub zum Starten eines 32-Bit-Installations Moduls verwenden, erkennt das 64-Bit-Windows bestimmte Programme mit 16-Bit-Installer und ersetzt eine portierte 32-Bit-Version.

16-Bit-DOS-, Windows-oder OS/2-Anwendungen verwenden häufig einen 16-Bit-Stub, um den Computertyp zu überprüfen, und starten dann eine 32-Bit-Installations-Engine, um die Installation tatsächlich auszuführen. Um die Installation von Anwendungen zu ermöglichen, die diese Technik verwenden, ersetzt 64-Bit-Windows 32-Bit-Versionen für die folgenden 16-Bit-Installer-Programme:

* Microsoft Setup für Windows 1,2  
* Microsoft Setup für Windows 2,6  
* Microsoft Setup für Windows 3,0  
* Microsoft Setup für Windows 3,01  
* InstallShield 5. x  

Die Liste der Substitutionen wird in der Registrierung unter folgendem Schlüssel gespeichert: **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ NtVdm64**.

> [!Note]  
> Dieser Mechanismus wird nur für die Kompatibilität mit 32-Bit-Anwendungen bereitgestellt, die die in diesem Thema aufgeführten 16-Bit-Microsoft Installer-Programme verwenden. Das Hinzufügen von Installationsprogrammen von Drittanbietern wird nicht unterstützt.

 

> [!Note]  
> Dieser Mechanismus ist nicht unter Windows 10 auf Arm enthalten.

 

 

 